# CS598 Deep Learning for Healthcare Project

__Team 186__

| Name               | Email                        |
| ------------------ | ---------------------------- |
| Adam Michalsky     | adamwm3@illinois.edu         |
 | Michael Pettatano  | mp34@illinois.edu           |


This repository is an implementation of [CS598 Deep Learning for Healthcare Reproducibility Project](https://www.overleaf.com/project/640b4754b63010e6f4745274) which is our attempt at reproducing the experiments conducted in
[Disease Prediction and Early Intervention System Based on Symptom Similarity Analysis](https://ieeexplore.ieee.org/document/8924757).


>📋  Optional: include a graphic explaining your approach/main result, bibtex entry, link to demos, blog posts and tutorials

## Requirements

### Jupyter Notebook

The reproduction was implemented as a jupyter notebook. For information on how to work with jupyter notebooks please visit the jupyter [website](https://jupyter.org/).

This notebook was implemented and executed using a Python version `3.9` environment. A requirements file is included that documents the specific version of each package used. For more details on package version see [requirements.](https://github.com/mikepettenato/cs-598-dl4health-final-project/blob/main/requirements.txt)

Use the following command to install the required packages in your python environment:

```setup
pip install -r requirements.txt
```

### Data

For this reproduction, we have opted to use the [Microsoft Research Paraphrase Corpus](https://www.microsoft.com/en-us/download/details.aspx?id=52398). This dataset contains 5800 sentence pairs along with human annotations on the similarity between sentence in the pairs. 

This dataset has already been download and formatted for the notebook. It is available under the `/data` directory.


## Training & Evaluation

Training and evaluation can be done by opening the jupyter notebook, `main.ipynb` and choosing the _Run All_ option in the __Cell__ menu.

>📋  Describe how to evaluate the trained models on benchmarks reported in the paper, give commands that produce the results (section below).

## Pre-trained Models

You can download pretrained models here:

- [My awesome model](https://drive.google.com/mymodel.pth) trained on ImageNet using parameters x,y,z. 

>📋  Give a link to where/how the pretrained models can be downloaded and how they were trained (if applicable).  Alternatively you can have an additional column in your results table with a link to the models.

## Results

Our model achieves the following performance on :

### [Image Classification on ImageNet](https://paperswithcode.com/sota/image-classification-on-imagenet)

| Model name         | Top 1 Accuracy  | Top 5 Accuracy |
| ------------------ |---------------- | -------------- |
| My awesome model   |     85%         |      95%       |

>📋  Include a table of results from your paper, and link back to the leaderboard for clarity and context. If your main result is a figure, include that figure and link to the command or notebook to reproduce it. 


## Contributing

>📋  Pick a licence and describe how to contribute to your code repository. 