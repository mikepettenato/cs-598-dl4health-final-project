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

Additionally, the notebook requires a download of the SpaCy parser model. Please refer to the _Pre-trained Models_ section below for installation instructions.


### Data

For this reproduction, we have opted to use the [Microsoft Research Paraphrase Corpus](https://www.microsoft.com/en-us/download/details.aspx?id=52398). This dataset contains 5800 sentence pairs along with human annotations on the similarity between sentence in the pairs. 

This dataset has already been download and formatted for the notebook. It is available under the `/data/` directory.

### Pre-trained Models

The original paper makes use of a Stanford Parser, so we leveraged the python `stanza` package for this requirement. In the notebook we leverage the default stanza model with the following parameters:

```python
import stanza
stanza.Pipeline(lang='en', processors='tokenize,pos,constituency', download_method=None, use_gpu=True)
```

As part of the ablations performed, we introduced additional models that have been pre-trained for parsing and embedding.

For parsing, the notebook also uses the `spacy` package as a parser. While the package install is part of `requirements.txt`, it is recommended to download the model seperately using the code snippet below.

```shell
python -m spacy download en_core_web_sm
```
*If you work with multiple environments, make sure it is being downloaded to the correct one!*

Additional details on SpaCy can be found on their [website](https://spacy.io/usage).


For embedding, the notebook leverages a pre-trained `Word2Vec` model available from the `gensim` package.

- [google-news-word2vec-model](https://radimrehurek.com/gensim/models/word2vec.html) 

```python
import gensim.downloader as api
model = api.load("word2vec-google-news-300")  # download the model and return as object ready for use
```

## Training & Evaluation

Training and evaluation can be done by opening the jupyter notebook, `main.ipynb` and choosing the _Run All_ option in the __Cell__ menu.

>📋  Describe how to evaluate the trained models on benchmarks reported in the paper, give commands that produce the results (section below).



## Results

Our model achieves the following performance on :

### [Image Classification on ImageNet](https://paperswithcode.com/sota/image-classification-on-imagenet)

| Model name         | Top 1 Accuracy  | Top 5 Accuracy |
| ------------------ |---------------- | -------------- |
| My awesome model   |     85%         |      95%       |

>📋  Include a table of results from your paper, and link back to the leaderboard for clarity and context. If your main result is a figure, include that figure and link to the command or notebook to reproduce it. 


## Contributing

>📋  Pick a licence and describe how to contribute to your code repository. 