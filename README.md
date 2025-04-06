# remote-server-deploy
This repository demonstrates the deployment of a backend application on a remote server via SSH using public/private key authentication. It includes an automated deployment process with a shell script and integration with a Git-based workflow.

# SSH Deployment with GitHub Actions

This repository shows how to deploy files to a remote server using SSH and GitHub Actions.

## Files Included

- `Saludo_Brayan.txt`: Greeting file uploaded to the server to confirm successful deployment.
- `.github/workflows/deploy.yml`: GitHub Actions workflow to automate the deployment.

## How It Works

1. Secrets are added in GitHub Actions:
   - `SSH_PRIVATE_KEY`
   - `SSH_HOST`
   - `USER_NAME`
   - `PROJECT_PATH`
   - `GIT_REPO`

2. When code is pushed to the `main` branch:
   - GitHub Actions connects to the server using SSH.
   - The server pulls the latest version of the project.

## Manual SSH Access

You can also connect manually to check:

```bash
ssh -i pemSMacServerEstudiantes ndgserver@201.190.115.29
