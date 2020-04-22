# Packer: 'packer_nodejs.json'


## Explanation of what Packer is?

- A 'Packer' is an open source tool maintained by Hashicorp which allows you to create
duplicate machine images using just a single source file.
- This directory contains a file called 'packer_nodejs.json. The packer was created using Chef 
and its a config management tool that provisions packages onto the machine.

## How to use the repo to create AMI for environments:

STEP 1: To download this repo you'll need to run the following:
- git@github.com:CamileM/packer_nodejs.git

STEP 2: You will then need to run the following commands 'berks vendor' and that
will pull the required Chef cookbooks from Github.

STEP 3: To validate that this was a success you'll need to type:
- 'packer validate packer_nodejs.json'

STEP 4: To build the packer:
- 'packer build packer_nodejs.json'

WARNING: Any errors that you come across when attempting to build the packer, you'll need
delete the 'berks-cookbooks' folder and 'Berksfile.lock' and run berks vendor again.

## Pre-requisites:
- GitHub
- Chef
- Packer (packer.json)
- AWS
