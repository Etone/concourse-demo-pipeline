# Concourse Demo of Features in Version 7

This repo includes a demo pipeline as well as a config for a second one. The pipeline showcases how the features of concourse, namely set-pipeline, load-var, across and instanced pipelines can be used to automate pipelines

## How to use

1. clone the repo
2. let a local instance of concourse run. The docker-compose file in this repo has all the features active.  
```docker-compose up```
3. Create a pipeline based of the [provided pipeline file](pipeline.yaml) file  
```fly -t local sp -p demo -c pipeline.yaml```
4. The pipeline create two pipeline instances with two values. One value is the one [provided in the message file](message.json), the other provided by the across step