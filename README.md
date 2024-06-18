# lab2
# *SRE Academy - Lab2*

This repository takes advantage of Github's cloud services to build and deploy a simple app into a Kubernetes basic setup with minikube.

# *Within the repo, there are two CI/CD workflows:*
1. ./github/workflows/ci.yaml: This is the main pipeline, deploys the app to a minikube environment.
2. ./github/workflows/build.yml: This is the pipeline to build and upload the resulting container image to GH registry (Packages)

# *How to execute the workflows:*
The aforementioned pipelines can be executed on demand, simply click on [Actions](https://github.com/estebanfallasf/sre-lab2/actions), pick one on the left column and then click on the "Run workflow" button. Both of these make use of several "actions", which are a way of mimizing the work needed by simply using pre-packaged tasks such as checking out the code, building, tagging and uploading images, install minikube amongst others.
Also, they make use of the repo's secrets, which are hidden values emmployed only during the execution of a pipeline.

Finally, the original app code has been refactored into a multi-stage build, resulting in 10x less footprint than originally conceived, image is now around 60MB in size in contrast to the original 1GB initial version.

Check the pipeline outputs to see the results from all the different steps in action.

*Images built and uploaded from this repo can be found here:*
https://github.com/estebanfallasf?tab=packages&repo_name=sre-lab2

