## Learning Image Restoration

Pytorch implementation of *[On learning optimized reaction diffusion processes for effective image restoration](https://arxiv.org/abs/1503.05768)* by Yunjin Chen, Wei Yu and Thomas Pock.

---
You can train your own model on a given type of noise, there are 2 available types : Gaussian noise and Poisson noise:
```bash
python train.py --noise Gaussian models/new_model.pt
```

Or test an already trained model on one of those two types of noises :
```bash
python test.py --noise Poisson models/joint7.pt
```

### Trained models

The models available at ./models folder are pretrained models :


Greedy5 : Trained using greedy methods with a filter size of 5x5 on a gaussian noise of variance 25

Greedy7 : Trained using greedy methods with a filter size of 7x7 on a gaussian noise of variance 25

joint5 : Trained using the greedy method first then fine tuned with a joint training. The kernel size is 5x5 and the variance of the gaussian noise is 25

joint7 : Trained using the greedy method first then fine tuned with a joint training. The kernel size is 7x7 and the variance of the gaussian noise is 25

new_joint7_gaussian25 : Trained using only a joint training with a filter size of 7x7 on a gaussian noise of variance 25

new_joint7_poisson : Trained using only a joint training with a filter size of 7x7 on a poisson noise
