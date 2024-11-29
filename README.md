# Fine-tuned Optical Character Recognition For Dental Fossil Markings

Experiment files and pretrained models from the Data Science MSc thesis 'Fine-tuned Optical Character Recognition For Dental Fossil Markings'.

## Usage of the pretrained models

See demo notebook in `pretrained_models/demo.ipynb` 

## Run experiments on your own data

Requirements:

- Python v. 3.12>, pip
- Images to classify in a data directory in [TorchVision ImageFolder format](https://pytorch.org/vision/stable/generated/torchvision.datasets.ImageFolder.html?highlight=imagefolder#torchvision.datasets.ImageFolder). Program expects you to have in your data directory a classification task named folder, eg 'upper/lower' and under that directories 'train' and 'val', inside which examples: 'train/upper/1.png, train/upper/2.png, train/lower/3.png ...' for both training and validation data. Target class count is automatically detected from the number of class directories; they should equal in name and amount in train and validation directories.

1. Insert to desired .json file the name of the classification task and the absolute path to your data directory (one level above classification task directory).

2. Create a virtual environment:
```
python -m venv venv
``` 

3. Install requirements
```
pip install -r requirements.txt
```
(Installation will take a while)

4. Run your experiments
```
python experiment.py [configfile].json
```

5. Inspect experiment results in MLflow tracking server

```
chmod u+x run_tracking_server.sh
./run_tracking_server.sh
```

Navigate to [MLflow local UI](http:localhost:8080). You see your experiments in the UI and pretrained models are downloadable
on each run's artifacts by selecting the experiment, clicking on a run and scrolling down to 'artifacts'.
