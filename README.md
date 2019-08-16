# Dog Breed




GCP_PROJECT=np-training
APP_NAME=dog-breed
REGION="us-central1"
MEMORY=1G
gcloud builds submit --tag gcr.io/$GCP_PROJECT/$APP_NAME


gcloud beta run deploy $APP_NAME --image gcr.io/$GCP_PROJECT/$APP_NAME --region $REGION --memory $MEMORY --allow-unauthenticated
