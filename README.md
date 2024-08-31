<details>

<summary>1-How to setup MongoDB on Ubuntu</summary>

# How to setup MongoDB Server on Ubuntu22.04 LTS
Step 1: Install Necessary Packages
```bash
sudo apt install software-properties-common gnupg apt-transport-https ca-certificates -y
```
Step 2: Add MongoDB GPG Key
```bash
curl -fsSL https://pgp.mongodb.com/server-7.0.asc |  sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg --dearmor
```

Step 3: Add MongoDB Repository
```bash
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
```

Step 4: (Optional) Confirm the Repository Added
```bash
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse"
```
Step 5: Update Package List
```bash
sudo apt update
```

Install MongoDB
```bash
sudo apt install mongodb-org -y
```

### Relate command for MongoDb
> Start MongoDB service
```bash
sudo systemctl start mongod
```
> Enable MongoDB on Startup
```bash
sudo systemctl enable mongod
```
> Check MongoDB Status
```bash
sudo systemctl status mongod
```
</details>