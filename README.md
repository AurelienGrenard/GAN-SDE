## Notebook Structure

This repository is organized around a collection of notebooks dedicated to the evaluation, comparison, and analysis of GAN-trained generators for various financial models. The notebooks are grouped into three main categories, described below.

### 1. Validation of GAN generators by model

The first five notebooks focus on the evaluation of neural generators trained via GANs for different native stochastic models:

 `Test_GAN_Heston`  
 `Test_GAN_VG`  
 `Test_GAN_NIG`  
 `Test_GAN_rBergomi`  
 `Test_GAN_CIR`  

Each notebook assesses a generator trained on a specific model. The evaluation relies on several quantitative metrics, and the generated outputs are systematically compared to the distributions produced by the corresponding native model used during training. In particular, the analysis emphasizes the ability of the generators to accurately reproduce marginal densities at various maturities and parameters.

### 2. Pathwise comparison of generated trajectories

The notebook,

`Test_GAN_Heston_Path`

is dedicated to compare paths produced by GAN-based generators trained on the Heston and CIR models with trajectories obtained directly from the corresponding native model. 

### 3. Sobolev versus classical training

The final notebook,

`Test_Sobolev_(Heston model)`

presents a comparison between two training strategies for the Heston model. It contrasts a classical L2-based training approach with a Sobolev-type training, which incorporates explicit gradient supervision within the GAN framework.

---

## `utils` Directory Overview

The notebooks rely on a shared `utils` directory, which contains the core building blocks required for model loading, evaluation, and testing. This directory is organized as follows.

### `utils/models`

This folder contains the neural network architectures used throughout the project. It includes both neural generators, obtained from GAN training, and neural pricers associated with the GAN-based Heston models.

### `utils/Sobolev_Test_Dataset`

This folder contains the test datasets used in the Sobolev training experiments. 

### `utils/Heston+CIR_generators`

This folder contains trained neural generators dedicated to path generation for the Heston and CIR models.




```python

```
