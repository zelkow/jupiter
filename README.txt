gcloud project create prj-jupiter
export PROJECT_ID=prj-jupiter
gcloud config set project prj-jupiter
docker pull jupyter/datascience-notebook
gcloud auth configure-docker 
docker tag jupyter/datascience-notebook eu.gcr.io/prj-jupiter/jupyter:v1
docker push eu.gcr.io/prj-jupiter/jupyter:v1
