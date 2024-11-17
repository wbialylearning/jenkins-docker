# Install Jenkins using Podman Compose

The below steps has only been tested on mac and are not to used for any production nor commertial purpose.

## Step 1

Install Podman Desktop.


## Step 2

Build the Jenkins Docker image:

```
podman build -t jenkins .
```

## Step 3

Start Jenkins:

```
podman compose up -d
```

## Step 4

Open Jenkins by going to: [http://localhost:8080/](http://localhost:8080/) and finish the installation process.

## Step 5

To stop Jenkins, run:

```
podman compose down
```

# Removing Jenkins

Run the following comand to terminate Jenkins and to remove all volumes and images used:

```
podman compose down --volumes --rmi all 
```
