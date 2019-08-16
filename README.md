# Dog Breed





## Deploy (Google Cloud Run)

Google Cloud Run is a managed serverless docker hosting solution.


```
GCP_PROJECT=...
APP_NAME=dog-breed
REGION="us-east1"
MEMORY=1G
gcloud builds submit --tag gcr.io/$GCP_PROJECT/$APP_NAME



gcloud beta run deploy $APP_NAME --image gcr.io/$GCP_PROJECT/$APP_NAME --region $REGION --memory $MEMORY --allow-unauthenticated --platform managed
```