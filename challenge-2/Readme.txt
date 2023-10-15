# Execution Commands
```
gcloud auth login #using named account
or
gcloud auth activate-service-account SERVICE_ACCOUNT@DOMAIN.COM --key-file=/path/key.json --project=PROJECT_ID    #using service account

gcloud compute instances create nareshvm --zone=us-east1-b \
--machine-type=n1-highmem-8 \
--image=centos-7-v20210817 \
--image-project=centos-cloud \
--boot-disk-size="50GB"

gcloud compute instances add-metadata nareshvm --metadata=important-data="2 plus 2 equals 4"


$ gcloud compute instances describe nareshvm --zone=us-east1-b --format="json(metadata)"

$ gcloud compute instances describe nareshvm --zone=us-east1-b --format="json(metadata)"
{
  "metadata": {
    "fingerprint": "6XsNCqncpxo=",
    "items": [
      {
        "key": "important-data",
        "value": "2 plus 2 equals 4"
      }
    ],
    "kind": "compute#metadata"
  }
}
```
