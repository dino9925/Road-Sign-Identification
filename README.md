# Developing a neural network to identify traffic signs from a photograph.

## Experimentation Process

We started with a simple convolutional neural network model with the following structure:
- 1 convolutional layer, learning 32 filters using a 3x3 kernel
- 1 max-pooling layer, using a 2x2 pool size
- 1 hidden layer with 128 nodes
- 0.5 dropout rate
- output layer with output units for all traffic sign categories


## Experiment Results

| #  | Modification                                                                                   | Testing accuracy | Validation accuracy |
| :--| :-------------------------------------------------------------------------------------------  | :--------------- | :------------------ |
| 1  | Base model                                                                                    | `0.5446`         |                     |
| 2  | Add second convolutional layer, identical to the first                                         | `0.9708`         |                     |
| 3  | Add second max-pooling layer (after the second convolutional layer), identical to the first    | `0.9503`         |                     |
| 4  | Remove second max-pooling layer, increase kernel size in second convolutional layer to (4, 4) | `0.9480`         |                     |
| 5  | Double number of filters (to 64) in second convolutional layer                                 | `0.9684`         |                     |
| 6  | Double number of nodes in hidden layer to 256                                                 | `0.9528`         |                     |
| 7  | Add second hidden layer (both layers with 128 nodes)                                          | `0.9511`         |                     |
| 8  | Remove dropout                                                                                | `0.9486`         |                     |
| 9  | Increase dropout rate to 0.7                                                                  | `0.9022`         |                     |

- 1 convolutional layer, learning 32 filters using a 3x3 kernel
- 1 max-pooling layer, using a 3x3 pool size
- 1 hidden layer with 43*32 nodes
- 0.2 dropout rate
- 1 hidden layer with 43*16 nodes
- 1 hidden layer with 43*8 nodes
- 1 output layer with 43 nodes