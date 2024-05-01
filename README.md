FRSKD
Official implementation for Refine Myself by Teaching Myself : Feature Refinement via Self-Knowledge Distillation (CVPR-2021)

Requirements
- Python3
- Pytorch (>1.4.0)
- torchvision
- numpy
- Pillow
- tqdm

Classification Training
In this code, you can reproduce the experiment results of classification task in the paper. The datasets are all open-sourced, so it is easy to download. Example training settings are for ResNet18 on CIFAR100. Detailed hyperparameter settings are enumerated in the paper.
- Training with FRSKD
```
python main.py --data_dir PATH_TO_DATASET \
--data CIFAR100 --batch_size 128 --alpha 2 --beta $100 \backslash$
--aux none --aux_lamb $\theta$--aug none --aug_a $\theta$
```
- Training with FRSKD + SLA
```
python main.py --data_dir PATH_TO_DATASET \
--data CIFAR100 --batch_size 128 --alpha 2 --beta $100 \backslash$
--aux sla --aux_lamb 1 --aug none --aug_a $\theta$
```
- Training with FRSKD + Mixup
```
python main.py --data_dir PATH_TO_DATASET \
--data CIFAR100 --batch_size 128 --alpha 2 --beta $100 \backslash$
--aux none --aux_lamb $\theta$--aug mixup --aug_a $\theta .2$
- Training with FRSKD + CutMix
python main.py --data_dir PATH_TO_DATASET \
--data CIFAR100 --batch_size 128 --alpha 2 --beta 100 \
--aux none --aux_lamb $\theta$--aug cutmix --aug_a 1.0
```
Segmentation Training

You can reproduce the experiment results in FRSKD paper.
- Training with FRSKD (efficientdet-b0)
python main.py --data_dir PATH_TO_DATASET --batch_size 16 --alpha 1 --beta 50
