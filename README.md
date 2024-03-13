# Cognitive Distillation – detecting backdoor attacks on deep models

Result replication of the following paper: [Distilling cognitive backdoor patterns within an image](https://openreview.net/pdf?id=S3D9NLzjnQ5).

The project is set up as a Jupyter notebook in the projekt.ipynb file.

The idea is to extract a minimal necessary part of the picture responsible for the model's prediction, and make conclusions about backdoor trigger patterns accordingly.

Technologies and concepts used are: PyTorch, ResNet18 architecture, CIFAR10 dataset, BadNets attack.

Steps of the implementation are:
1. Cognitive Distillation algorithm is executed on clean dataset
2. BadNets attack is executed upon the dataset, creating a poisoned dataset
3. ResNet18 is trained on the poisoned dataset, for visual extraction of the inserted malign triggers
4. Cognitive Distillation is executed on poisoned dataset
5. Accuracy and AUROC metrics are calculated on clean and modified datasets
