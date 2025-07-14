# Harbor Local Installation Guide

Follow these steps to install Harbor locally on your VM:

## 1. Prerequisites
- Ensure Docker is installed and running on your VM.

## 2. Download and Extract Harbor Installer
```
wget https://github.com/goharbor/harbor/releases/download/v2.10.0/harbor-online-installer-v2.10.0.tgz
tar xvf harbor-online-installer-v2.10.0.tgz
```

## 3. Prepare Harbor Configuration
- Change directory to the extracted `harbor` folder:
  ```
  cd harbor
  ```
- Edit the `harbor.yml` file to suit your environment and requirements.

## 4. Install Harbor
- To install Harbor with Trivy scanner:
  ```
  ./install.sh --with-trivy
  ```
- Or, to install Harbor with Clair scanner:
  ```
  ./install.sh --clair
  ```

The installation will generate all necessary Harbor service bundles and configuration files, including the Docker Compose YAML for Harbor services.

---
For more details, see the [official Harbor documentation](https://goharbor.io/docs/).
