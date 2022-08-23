# Google Cloud Container Registry Docker Push

Github action to push a docker image to [Google Cloud's Container Registry](https://cloud.google.com/container-registry). 

## Prerequisites

Set up the following resources manually in the Cloud Console 
or use a tool like [Terraform](https://www.terraform.io).

* Enable Container Registry API
* Create Service Account with Role `Storage Admin` and export a new JSON key.


## Github Action Inputs

| Variable                         | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `creds`                          | ***Required*** Service Account JSON Key (not base64 encoded)                |
| `src`                            | ***Required*** Source Image                                                 |
| `dst`                            | ***Required*** Destination Image                                            |
| `registry`                       |  Registry host name (must match destination image), default: "gcr.io"       |


## Example Usage

```
uses: dchinchure/gcr-upload-action@master
with:
  service_account: ${{ secrets.GCP_SERVICE_ACCOUNT }}
  source_image: local-image:tag
  destination_image: gcr.io/my-project/new-image:tag
```
