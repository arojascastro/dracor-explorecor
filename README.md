# CLS INFRA Training School: ExploreCor – Using Programmable Corpora in Computational Literary Studies

Vienna 10-14 June 2024

https://clsinfra.io/events/training-school/

This repository contains the teaching material used for the **DraCor-related sessions** of the CLS INFRA Training School: *ExploreCor – Using Programmable Corpora in Computational Literary Studies*.

The following sessions are covered by this material:

- Introduction to Programmable Corpora [Session 1]
- Corpora in CLS Research. User Perspectives [Session 2]
- Exploring Programmable Corpora (Focus: Network Analysis) [Session 5]
- Reproducibility in CLS Research [Session 6]
- Open Topics [Session 7]

## Setup of a Local DraCor Environment
You can setup a local DraCor infrastructure and run the provided Jupyter notebooks in your local Jupyter Lab instance. We provide a Docker Compose File that can be used to start the services. It is necessary to have Git and [Docker (Desktop)](https://www.docker.com/products/docker-desktop) installed. If you are working on Windows use the Windows [Powershell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell?view=powershell-7.4) or any other shell that allows you to use UNIX commands on Windows to execute the commands below:

1. In your Terminal clone this repository with the command `git clone https://github.com/dracor-org/dracor-explorecor.git`. Alternatively you can [download](https://github.com/dracor-org/dracor-explorecor/archive/refs/heads/main.zip) and unpack the ZIP file. 
2. Change into the folder `dracor-explorecor` with the command `cd dracor-explorecor`
3. Use the command `docker compose up` to start the Docker container
4. Navigate to [http://localhost:8889](http://localhost:8889) to access your local Jupyter Lab instance containing the materials. A HTML version can be accessed at [http://localhost:9980](http://localhost:9980) .

If you encouter problems setting up your environment you can join us for virtual trouble shooting session before the Training School. Please refer to the E-Mail you recieved containing the the Zoom-Link. 

## Build a Jupyter Book (optional)
You can build a HTML version of the teaching materials: Inside the Docker Container (e.g. from a Terminal Tab in Jupyter Lab) navigate to the `notebooks` folder and build the book with `jupyter-book build .`. You will find a directory `_build` containing the HTML version in the `dracor-explorecor` folder on your machine.

## Some problems in the Trouble Shooting Session

### On Windows: Docker Desktop can't be started

Error Message: 
> An unexpected error occurred [...] connect ENOENT \\.\pipe\errorReporter" or similar.

If you have full access to your system, you test running Docker Desktop with Administrator account. If that works and you only have troubles starting Docker with your other local non-administrator account you should add your local user to the Windows group `docker-users`. 

- Go to "Computer Management" 
- Under "System Tools" select "Local Users and Groups" (in the left pannel)
- Open "Users" and select the user you want to edit
- In the "Member Of" tab click on "Add", add `docker-users` in the input box and click "Check Names"
- Log out of you Administrator account and test with you local account if you can now launch Docker Desktop 
