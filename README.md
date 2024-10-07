## Helm Charts Repository

This is self hosted cadence charts repository as a back up for the official Banzai Cloud Helm Charts repository.

## Build Packages

1. On a seperate folder, checkout the official repo `git clone git@github.com:banzaicloud/banzai-charts.git official-banzai-charts`
1. Go to `official-banzai-charts`
1. Checkout a tagged version: `git checkout <release tag>`
1. Run the following command to build cadence chart package 
    ```
    helm dependency update cadence
    helm package cadence
    ```
1. Copy the created tgz file back to the root folder
1. Run `helm repo index .` to update the index file
1. Push the changes to git to publish the package
