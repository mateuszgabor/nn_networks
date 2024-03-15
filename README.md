# Fixed points of nonnegative neural networks

Official PyTorch repository for an experimental section of the paper [Fixed points of nonnegative neural networks](https://arxiv.org/pdf/2106.16239.pdf)

## Requirements
* `pip install -r requirements`

## Training
To train autoencoders used in paper, use the following command

```shell##
python train.py -net <net_name> -lr <lr_rate> -epochs <epochs> -wd <weight_decay> -b <batch> 
```
where:
* `<net_name>` - the name of the pcDEQ model, one from the following list:
  * `nn_sigmoid` - autoencoder from Section 6.1
  * `nn_tanh` - autoencoder from section 6.2
  * `pn_tanh` - autoencoder from section 6.3
  * `nn_relu` - autoencoder from section 6.4
  * `pn_relu` - autoencoder from section 6.5
  * `nn_tanh_swish` - autoencoder from section 6.6
  * `nr_relu_sigmoid` - autoencoder from section 6.7
  *  `rr_relu_sigmoid` - autoencoder from section 6.8
* `<lr_rate>` - learning rate 
* `<epochs>` - number of epochs 
* `<wd>` - weight decay
* `<b>` - batch size

The following command shows the example of training autoencoder from section 6.1
```shell
python train.py -net nn_sigmoid -lr 5e-3 -epochs 30 -wd 0 -b 64 
```
