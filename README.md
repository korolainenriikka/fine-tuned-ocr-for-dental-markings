README

you need python (v 3.12>) & pip

tee imagefolder
imagefolder needs to have train and val directories
laita experiments.jsoniin task (imagefolderin alla olevan dirin nimi)
laita experiments.jsoniin missä sun imagefolder sijaitsee
testaa eri juttuja

Create a virtual environment:
python -m venv venv

Install requirements
pip install -r requirements.txt

(Installation will take a while)

Run experiments
python experiment.py <config json filename, defaults to experiments.json>

chmod u+x run_tracking_server.sh
./run_tracking_server.sh

navigate to http:localhost:8080. You see your experiments in the UI and pretrained models are downloadable
on each run's artifacts: click on the run and then artifacts.