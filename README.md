# Gradient flow check in Pytorch

Check that the gradient flow is proper in the network by recording the average gradients per layer in every training iteration and then plotting them at the end. If the average gradients are zero in the initial layers of the network then probably your network is too deep for the gradient to flow.

## Usage 

```
loss = self.criterion(outputs, labels)  
loss.backward()
plot_grad_flow(model.named_parameters()) # version 1
# OR
plot_grad_flow_v2(model.named_parameters()) # version 2
```

## Result

Bad gradient flow:

![Bad gradient](https://discuss.pytorch.org/uploads/default/original/2X/e/e4b19586eb7b68d94ba02fa9159f141c9f12e106.png)

Good gradient flow:

![Good gradient](https://discuss.pytorch.org/uploads/default/original/2X/5/5af139d68e14dbdd9745952a744f105458d2caa7.png)

Repo based on [this pytorch discuss post](https://discuss.pytorch.org/t/check-gradient-flow-in-network/15063).
