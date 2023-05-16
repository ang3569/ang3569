- 👋 Hi, I’m @ang3569
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
ang3569/ang3569 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->cd packer

packer init -upgrade .

packer build -only=release.proxmox.talos -var-file="vars/local.pkrvars.hcl" -var proxmox_username="${PROXMOX_TOKEN_ID}" \

-var proxmox_token="${PROXMOX_TOKEN_SECRET}" -var proxmox_nodename="${PROXMOX_NODE_NAME}" -var proxmox_url="${PROXMOX_HOST}" .
export PROXMOX_HOST="https://px.host.com:8006/api2/json"

export PROXMOX_TOKEN_ID='root@pam!fire'

export PROXMOX_TOKEN_SECRET="secret"

export PROXMOX_NODE_NAME="proxmox"

export CLUSTER_NAME="mgmt-cluster"
