# GCR Docker Push

Github action to push a docker image to GCR

## Prerequisites

* Create Service Account with Role `Storage Admin` and export a new JSON key.


## Github Action Inputs

| Variable                         | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `service_account`                          | ***Required*** Service Account JSON Key (not base64 encoded)                |
| `source_image`                            | ***Required*** Source Image                                                 |
| `destination_image`                            | ***Required*** Destination Image                                            |
| `registry`                       |  Registry host name (must match destination image), default: "gcr.io"       |


## Example Usage

```
uses: dchinchure/gcr-upload-action@1.2
with:
  service_account: ${{ secrets.GCP_SERVICE_ACCOUNT }}
  source_image: local-image:tag
  destination_image: gcr.io/my-project/new-image:tag
```
