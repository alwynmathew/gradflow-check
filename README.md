# Gradient flow check in Pytorch

Check that the gradient flow is proper in the network

## Usage 

loss = self.criterion(outputs, labels)  
loss.backward()
plot_grad_flow(model.named_parameters())

## Result

Bad gradient flow:

![Bad gradient](https://discuss.pytorch.org/uploads/default/original/2X/e/e4b19586eb7b68d94ba02fa9159f141c9f12e106.png)

Good gradient flow:

![Good gradient](https://discuss.pytorch.org/uploads/default/original/2X/5/5af139d68e14dbdd9745952a744f105458d2caa7.png)

Repo based on [this pytorch discuss post](https://discuss.pytorch.org/t/check-gradient-flow-in-network/15063).
