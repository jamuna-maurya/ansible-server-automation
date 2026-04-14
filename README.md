# ansible-server-automation

##  Objective

Automate the configuration of a remote Linux server using Ansible playbooks.

---

## 🛠️ Tools & Technologies

* Ansible
* AWS EC2 (Ubuntu)
* SSH
* Git & GitHub

---

## 📂 Project Structure

```
ansible-project/
│
├── inventory.ini        # Target server details
├── setup.yml            # Ansible playbook
└── README.md            # Project documentation
```

---

## ⚙️ Tasks Performed

* Installed Ansible on control node
* Created inventory file for target server
* Wrote Ansible playbook to automate setup
* Installed and configured:

  * Nginx (Web Server)
  * Git
* Enabled and started services automatically

---

## 🔐 Security Note

> ⚠️ Private key (.pem) is not included in this repository for security reasons.

---

## 🧾 Inventory File Example

```
[servers]
<server-ip> ansible_user=ubuntu ansible_ssh_private_key_file=/home/ubuntu/mykey.pem
```
<img width="1678" height="346" alt="image" src="https://github.com/user-attachments/assets/5f358442-8d54-4a7a-9b0f-0bd25f01de6a" />

---

## 📜 Playbook Overview

The playbook performs:

* System package update
* Installation of Nginx
* Starting and enabling Nginx service
* Installation of Git

<img width="2304" height="872" alt="image" src="https://github.com/user-attachments/assets/066642c0-424f-4503-a2c9-ef7fb2a812c7" />

---

## ▶️ How to Run

### 1️⃣ Test Connection

```
ansible -i inventory.ini servers -m ping
```

### 2️⃣ Run Playbook

```
ansible-playbook -i inventory.ini setup.yml
```

---

## ✅ Expected Output

* Nginx installed and running
* Git installed
* Server configured automatically

---

## 🌐 Verification

Open in browser:

```
http://<server-ip>
```

👉 You should see the Nginx welcome page

<img width="1572" height="886" alt="image" src="https://github.com/user-attachments/assets/3ff70550-9836-43f9-bea2-4d50bd69349f" />


---

## 📚 Learning Outcomes

* Understanding of Ansible architecture
* Writing and executing playbooks
* Automating server configuration
* SSH-based remote management

---

##  Author

**Jeny**

---


