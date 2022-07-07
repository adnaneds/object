# object
[![Build Status](https://jenkins.indigo-datacloud.eu/buildStatus/icon?job=Pipeline-as-code/DEEP-OC-org/object/master)](https://jenkins.indigo-datacloud.eu/job/Pipeline-as-code/job/DEEP-OC-org/job/object/job/master)

Semantic segmentation with unet, e.g Cercospora

To launch it, first install the package then run [deepaas](https://github.com/indigo-dc/DEEPaaS):
```bash
git clone https://github.com/adnaneds/object
cd object
pip install -e .
deepaas-run --listen-ip 0.0.0.0
```
The associated Docker container for this module can be found in https://github.com/adnaneds/DEEP-OC-object.

## Project structure
```
├── LICENSE                <- License file
│
├── README.md              <- The top-level README for developers using this project.
│
├── requirements.txt       <- The requirements file for reproducing the analysis environment, e.g.
│                             generated with `pip freeze > requirements.txt`
│
├── setup.py, setup.cfg    <- makes project pip installable (pip install -e .) so
│                             object can be imported
│
├── object    <- Source code for use in this project.
│   │
│   ├── __init__.py        <- Makes object a Python module
│   │
│   └── api.py             <- Main script for the integration with DEEP API
│
└── Jenkinsfile            <- Describes basic Jenkins CI/CD pipeline
```
