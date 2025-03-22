# 🚗 Autoware UTAR Docker Image

This repository provides a pre-built Docker image for the Autoware UTAR setup, enabling an easy and consistent development environment for autonomous vehicle projects.

---


**🛠️ Prerequisites**

Ensure Docker is installed and running on your machine.
If required, log in to GitHub Container Registry using:
```
docker login ghcr.io
```
A GitHub personal access token may be required with read:packages scope.


Make sure you download the map refer the link:
```
https://github.com/TUMFTM/Carla-Autoware-Bridge.git
```
---




## 📥 How to Pull the Image

You can pull the Docker image directly from the GitHub Container Registry using the command below:

```bash
docker pull ghcr.io/limzq99/autoware_utar:latest

```
---


**🚀 How to Run the Container**

After pulling the image, you can run it with:
```
docker run -it ghcr.io/limzq99/autoware_utar:latest
```
**If you need to run the container with volume mounting or specific port mappings, for example:**
```
docker run -it --network=host -v /your/local/path:/workspace ghcr.io/limzq99/autoware_utar:latest

```
---


**🚘 Run Autoware (inside container) **

After enter the container, you can run autoware with:
```
ros2 launch autoware_launch e2e_simulator.launch.xml vehicle_model:=carla_t2_vehicle sensor_model:=carla_t2_sensor_kit map_path:=<path to /wsp/map>
```

The map can be show in the workspace, select the Town10 map for the demo.

---



**🗺️ Project workspce in Container**

Path to the workspoace:
```
cd /home/limziquan/Desktop/FYP
```
---


**📚 About This Image**

This Docker image includes:

A complete Autoware setup for UTAR research and development.

Preconfigured environment to support simulation, testing, and autonomous driving research.

Simplified setup, eliminating environment configuration errors.

---


**💡 Useful Tips**

Keep your Docker engine updated for the best performance and compatibility.

If running on WSL2 or Docker Desktop, ensure resources (CPU/RAM) are sufficient for simulation tasks.

Use docker ps to check running containers and docker stop <container_id> to stop them.
---


