Creamos un entorno con python 3.11.4, e instalamos las dependencias necesarias.

conda create -n cruzverde
conda activate cruzverde
conda install python=3.11.4
pip install -r requirements.txt
streamlit run app.py

Inicia sesión en Google Cloud:
gcloud auth login

Configura el proyecto:
gcloud config set project sbsegurosprod

Configura Docker para autenticación con Artifact Registry:
gcloud auth configure-docker us-central1-docker.pkg.dev

Intenta nuevamente realizar el docker push:
docker push us-central1-docker.pkg.dev/sbsegurosprod/sbsegurosprod/cruzverde/cruzverde:sbspro4