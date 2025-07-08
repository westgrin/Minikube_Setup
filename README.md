# # Mini Project - Setting Up Minikube (Local Setup)

## Project Overview
This project installs and configures Minikube on WSL Ubuntu, sets up a local Kubernetes cluster with Docker as the driver, and deploys a sample Node.js application. It uses GitHub Actions to automate Docker image building. Executed on WSL Ubuntu with VS Code and Git Bash.

## Setup
- Initiated on Jul 08, 2025, 3:32 AM WAT.
- Used WSL Ubuntu, VS Code, and Git Bash in `C:\Users\Abraham\Documents\Workspace\Minikube_Setup`.
- System: 2 CPUs, 2GB free memory, 20GB free disk space.

## Execution Steps
1. **Install Docker**:
   - Installed Docker CE and verified with `systemctl status docker`.
   - [Screenshot: `docker_install_output_local.png` - Shows Docker version and status.]
2. **Install Minikube**:
   - Downloaded and installed Minikube using `dpkg`.
   - [Screenshot: `minikube_version_local.png` - Shows Minikube version.]
3. **Install kubectl**:
   - Installed `kubectl` using snap.
   - [Screenshot: `kubectl_version_local.png` - Shows kubectl version.]
4. **Start Minikube**:
   - Started Minikube with Docker driver and verified cluster status.
   - [Screenshot: `minikube_status_output_local.png` - Shows Minikube status and nodes.]
5. **Deploy Sample Application**:
   - Created a Node.js app, built a Docker image, and deployed it to Minikube.
   - [Screenshot: `docker_build_output_local.png` - Shows Docker build output.]
   - [Screenshot: `minikube_app_output_local.png` - Shows deployed app output.]
6. **Side Hustle Task**:
   - Added GitHub Actions workflow to build Docker image.
   - Pushed to `https://github.com/westgrin/minikube-setup`.
   - [Screenshot: `github_repo_files_local.png` - Shows repository files.]
   - [Screenshot: `github_actions_run_local.png` - Shows workflow run.]

## Learning Summary
This project provided hands-on experience with Kubernetes, Minikube, Docker, and `kubectl`, reinforcing container orchestration concepts. The GitHub Actions workflow enhanced my automation skills, aligning with my DevOps goals (June 16, 2025) for scalable containerized deployments.

## Tools Used
- **WSL Ubuntu Terminal**: For Docker, Minikube, and Git commands.
- **VS Code**: For editing code and `README.md`.
- **Git Bash**: For GitHub operations.
- **GitHub Actions**: For Docker build automation.
- **Minikube**: For local Kubernetes cluster.
- **Docker**: For containerization.

## Project Deliverables
- **Documentation**: This `README.md` with steps and learning summary.
- **Screenshots**:
  - `docker_install_output_local.png`
  - `minikube_version_local.png`
  - `kubectl_version_local.png`
  - `minikube_status_output_local.png`
  - `docker_build_output_local.png`
  - `minikube_app_output_local.png`
  - `github_repo_files_local.png`
  - `github_actions_run_local.png`
- **Script Link**: [GitHub Repository](https://github.com/westgrin/minikube-setup)

## Local Development Instructions
1. Clone repository: `git clone https://github.com/westgrin/minikube-setup.git`
2. Install Docker, Minikube, and kubectl as shown in Steps 2-4.
3. Start Minikube: `minikube start --driver=docker`
4. Deploy app: `kubectl apply -f app/deployment.yaml`, `kubectl apply -f app/service.yaml`
5. Access app: `minikube service minikube-app-service --url`

## Troubleshooting
- Fixed network errors by retrying `curl` with `--retry 5`.
- Ensured Docker was running with `sudo systemctl start docker`.
- Verified system requirements (2 CPUs, 2GB memory, 20GB disk).

## Conclusion
This project successfully set up a Minikube cluster and deployed a containerized application, enhancing my Kubernetes and automation skills. The side hustle task prepared me for advanced container orchestration practices.