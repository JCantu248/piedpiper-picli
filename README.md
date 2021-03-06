ToDo:
Document more things

# PiCli

PiCli is a python client for PiedPiper, a CI-pipeline validation framework.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Python 3.6
(Optionally) virtualenv
PiedPiper OpenFaaS functions installed. 
ToDo: Document installation of OpenFaaS + functions


### Installing

#### Docker Installation

```
docker build -t picli .
docker run -it picli /bin/sh
```

#### Python installation
```
pip install -r requirements.txt
python setup.py install
```

## Using

To run PiCli:

#### Execute a lint

```
picli --config path/to/your/repo/piedpier.d/pi_global_vars.yml lint
```

#### Execute a validation

```
picli --config path/to/your/repo/piedpier.d/pi_global_vars.yml validate
```

### CLI Arguments

**debug**
```
picli --debug validate
```
Debug will dump PiCli's run_vars to the screen during execution. This allows
the user to validate PiCli's configuration that is being sent to the
various functions. 

## Running the tests

Currently we just have functional tests. These require an OpenFaaS installation. The test script
can be found in tests/functional/run-tests.sh


## Deployment

Add additional notes about how to deploy this on a live system

## Built With

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

TBD

## Acknowledgments

* Inspiration for the CLI framework came from the Ansible Molecule project

