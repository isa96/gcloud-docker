### Upload remote files to Google Cloud Storage with Google Cloud SDK on Docker

##### Clone this repository and enter the directory
> git clone https://github.com/isa96/gcloud-docker && cd gcloud-docker

##### Modify "key.json" according to your Google service account credentials
> nano key.json

##### Create Google Cloud SDK container with Docker Compose
> sudo docker compose up -d

##### Install required Python packages
> sudo docker exec -it gcloud sh -c "pip install google-cloud-storage && pip install wget"

##### Run the Python script to upload remote files to your Google Cloud Storage
> sudo docker exec -it gcloud sh -c "python3 main.py [URL] [FILENAME] [BUCKET]"

##### Example command
> sudo docker exec -it gcloud sh -c "python3 main.py https://engage.mitre.org/wp-content/uploads/2022/02/EngageHandbook.pdf mitre-engage-handbook.pdf aaa"
