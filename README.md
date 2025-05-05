Nabstract NEF – CNF Deployment & Upgrade Guide
📘 Overview
This repository provides instructions for installing and upgrading the Nabstract NEF (Network Exposure Function) software on an OpenShift environment using a Helm chart.

Nabstract NEF is a Cloud-Native Network Function (CNF) that is packaged and deployed via a Helm chart.

📦 System Requirements
To successfully deploy or upgrade the Nabstract NEF, the following requirements must be met:

OpenShift Cluster (Version 4.17.x or later)
oc CLI installed (v4.14.10 recommended)
Kubernetes cluster access (v1.30.7)
Internet access required for helmchart and Image download
Openshift enviorment Secure shell (SSH) access
Helm CLI installed (v3.7.1) with the Helm Push plugin
Kustomize (v5.0.1)
🚀 Upgrade Instructions
Step 1: Add the Helm Repository
helm repo add nef-nabstract https://nabstractio.github.io/nef-nabstract
Step 2: Upgrade NEF via Helm Chart
Replace <REPOSITORY_DETAILS> and <DOCKER_IMAGE_TAG_VERSION> with your Docker repository and tag details:
helm upgrade nef-nabstract nef-nabstract \
  --install \
  --set image.repository=<REPOSITORY_DETAILS> \
  --set image.tag=<DOCKER_IMAGE_TAG_VERSION> \
  --set namespace=nef-nabstract
✅ Verify Deployment

Run the following command to verify that the NEF pods are running:

oc get pods -n nef-nabstract
🔐 Confidentiality & Trademarks

This project and its documentation are proprietary to Nabstract Technologies Private Limited.

⚠️ No part of this document may be reproduced, stored, or transmitted in any form without prior written permission.
All trademarks mentioned herein are the property of their respective owners.

📄 License

Contact Nabstract Technologies for licensing information.

📬 Contact

For support or feature requests, please contact: 📧 paras.jani@nabstract.io# nef-nabstract
Helm chart repository of NEF.
