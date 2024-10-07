## Helm Charts Repository

This is self hosted cadence charts repository as a back up for the official Banzai Cloud Helm Charts repository.

## Build Packages

1. On a seperate folder, checkout https://github.com/banzaicloud/banzai-charts
1. `git checkout <release tag>`
1. Go to `banzai-charts`
1. Run the following command to build cadence chart package 
    ```
    helm dependency update cadence
    helm package cadence
    ```
1. Copy the created tgz file to this project
1. Run `helm repo index .` to update the index file
