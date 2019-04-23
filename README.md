# ConvGRU
**[This](https://github.com/zlb-ks/ConvGRU/blob/master/ConvGRU.py)** file **contains the implementation of Convolutional GRU in PyTorch** extends [ConvLSTM](https://github.com/ndrplz/ConvLSTM_pytorch/blob/master/convlstm.py).


### How to Use
The `ConvGRU` module derives from `nn.Module` so it can be used as any other PyTorch module.

The ConvGRU class supports an arbitrary number of layers. In this case, it can be specified the hidden dimension (that is, the number of channels) and the kernel size of each layer. In the case more layers are present but a single value is provided, this is replicated for all the layers. For example, in the following snippet each of the three layers has a different hidden dimension but the same kernel size.

Example usage:
```
model = ConvGRU(input_size=(height, width),
                input_dim=channels,
                hidden_dim=[64, 64, 128],
                kernel_size=(3, 3),
                num_layers=3,
                batch_first=True
                bias=True,
                return_all_layers=False)
```


### Disclaimer

This is still a work in progress and is far from being perfect: if you find any bug please don't hesitate to open an issue.