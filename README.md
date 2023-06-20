# Amor-Struct-GP-pretrained-weights
Pretrained weights for the method presented in "Amortized Inference for Gaussian Process Hyperparameters of Structured Kernels" (UAI 2023). The model `main_state_dict_paper.pth` is trained on the base symbols SE,LIN and PER and its two-gram multiplications and `main_state_dict_with_matern.pth` is trained on SE,LIN,PER and Matern52 and its two-gram multiplications. The first `.pth` file can be use with the `PaperAmortizedStructuredConfig` config in the main repo and the second file with the `AmortizedStructuredWithMaternConfig` config. 
## Get started
These weights correspond to the main [repo](https://github.com/boschresearch/Amor-Struct-GP). Make sure that you have installed `git lfs`. Clone the repo and then pull in order to download the files
```
git lfs pull
```
## Training summary
Training was conducted as outlined in the paper. Both files are checkpoints after the second training phase (after noise-variance fine-tuning), whereas for the first model the second phase consists of 200.000 datasets and for the second model of 40.000 datasets. The other training parameters were identical except we used a batch size of 32 for the second model instead of 128.

