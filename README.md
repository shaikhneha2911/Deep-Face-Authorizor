# Face Authentication System

This is a present-day face authentication system with cutting-edge algorithms for face detection and face embedding. Depending on the needs, endpoints in this system can be integrated into any kind of device. 

## Project Architecture
<img width="773" alt="image" src="https://user-images.githubusercontent.com/57321948/210045920-cc545886-1053-44f2-a491-e2ce8a3d18ce.png">

<img width="716" alt="image" src="https://user-images.githubusercontent.com/57321948/209801055-d2b2b882-b6a3-45ec-80e4-d794b021200b.png">


## Run the Application
Before you run the project, make sure that you have MongoDB in your local system, with Compass since we are using MongoDB for data storage. You also need an Azure account to access services like ACS and App services.

### Step 1-: Clone the Repository
```
git clone https://github.com/Rishav-hub/face_auth_dev.git
```

### Step 2-: Creat conda environment
```
conda create -p ./env python=3.8.13 -y
```

### Step 3-: Activate Conda environment
```
conda activate face_auth
```

### Step 4-: Install requirements
```
pip install -r requirements.txt
```

### Step 5-: Export the environment variable
```
export SECRET_KEY=<SECRET_KEY>

export ALGORITHM=<ALGORITHM>

export MONGODB_URL_KEY=<MONGODB_URL_KEY>

export DATABASE_NAME=<DATABASE_NAME>

export USER_COLLECTION_NAME=<USER_COLLECTION_NAME>

export EMBEDDING_COLLECTION_NAME=<EMBEDDING_COLLECTION_NAME>
```

### Step 6-: Run the application server
```
python app.py
```

## Run Locally

### Build the Docker Image
```
docker build -t face_auth --build-arg SECRET_KEY=<SECRET_KEY> --build-arg ALGORITHM=<ALGORITHM> --build-arg MONGODB_URL_KEY=<MONGODB_URL_KEY> --build-arg DATABASE_NAME=<DATABASE_NAME> --build-arg USER_COLLECTION_NAME=<USER_COLLECTION_NAME> --build-arg EMBEDDING_COLLECTION_NAME=<EMBEDDING_COLLECTION_NAME> . 
```

### Run the Docker Image

```
docker run -d -p 8000:8000 <IMAGEID OR IMAGENAME>
```
## Deployment to Azure

### Services used
- Azure container Registry (ACR) for the Docker image of the project is stored
- Azure App Services for deploying the application
- GitHub Actions for CI/CD


