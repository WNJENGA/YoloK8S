#**Explanation**

##Choice of the Kubernetes Objects used for deployment##
his project utilizes deployment, services, config maps, and persistent volume. The files are separated into the backend and the client DIR for efficiency.

The services for both client and backend are set to ensure that they are exposed externally.

Storage solutions
This project uses a local Mongo DB connection and a persistent volume size of 5Gi. This volume is linked to the backend deployment since they are interdependent. The config map stores the DB URL to the local Mongo DB.

Git workflow
The Yolo app is cloned and dockerized. With the images pushed to the docker hub, the deployment files call the already stored images. The choice to have separate deployment and services is to ensure efficieny of the app.

NB (Bug alert)
The app has a crashloop error and keeps restarting. This is a bug issue noted even when the app is run locally. This should not hinder the app from running on your environment.