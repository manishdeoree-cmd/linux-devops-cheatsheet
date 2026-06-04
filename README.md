# 🐧 Linux & DevOps Commands Cheat Sheet

![Linux](https://img.shields.io/badge/Linux-Commands-blue)
![DevOps](https://img.shields.io/badge/DevOps-Engineer-green)
![AWS](https://img.shields.io/badge/AWS-Cloud-orange)
![Docker](https://img.shields.io/badge/Docker-Containers-blue)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-blue)
![Terraform](https://img.shields.io/badge/Terraform-IaC-purple)
![Ansible](https://img.shields.io/badge/Ansible-Automation-red)

A complete collection of Linux, DevOps, Cloud, Container, Kubernetes, Terraform, Ansible, Git, and AWS CLI commands.

---

## 📑 Table of Contents

1. [Linux Basics](#1-linux-basics)
2. [File Management](#2-file-management)
3. [Text Processing](#3-text-processing)
4. [User Management](#4-user-management)
5. [Permissions](#5-permissions)
6. [Process Management](#6-process-management)
7. [Networking](#7-networking)
8. [Package Management](#8-package-management)
9. [Disk Management](#9-disk-management)
10. [Service Management](#10-service-management)
11. [Logs](#11-logs)
12. [Shell Scripting](#12-shell-scripting)
13. [Git Commands](#13-git-commands)
14. [Docker Commands](#14-docker-commands)
15. [Kubernetes Commands](#15-kubernetes-commands)
16. [AWS CLI Commands](#16-aws-cli-commands)
17. [Terraform Commands](#17-terraform-commands)
18. [Ansible Commands](#18-ansible-commands)
19. [Monitoring Commands](#19-monitoring-commands)
20. [Troubleshooting Commands](#20-troubleshooting-commands)

---

## 1. Linux Basics

| Command | Description |
|---------|-------------|
| `pwd` | Print working directory |
| `ls` | List files |
| `ls -la` | Detailed listing with hidden files |
| `cd /path` | Change directory |
| `history` | Command history |
| `clear` | Clear screen |
| `whoami` | Current user |
| `hostname` | System hostname |
| `uname -a` | System information |
| `date` | Current date and time |

---

## 2. File Management

| Command | Description |
|---------|-------------|
| `touch file.txt` | Create empty file |
| `mkdir test` | Create directory |
| `mkdir -p a/b/c` | Create nested directories |
| `cp file1 file2` | Copy file |
| `cp -r dir1 dir2` | Copy directory recursively |
| `mv file newfile` | Rename file |
| `mv file /tmp` | Move file |
| `rm file` | Delete file |
| `rm -rf dir` | Delete directory forcefully |
| `find . -name "*.txt"` | Find files by name |
| `locate file.txt` | Locate file quickly |
| `tree` | Show directory tree structure |

---

## 3. Text Processing

| Command | Description |
|---------|-------------|
| `cat file` | Display file content |
| `less file` | View file with pagination |
| `head -n 20 file` | Show first 20 lines |
| `tail -n 20 file` | Show last 20 lines |
| `tail -f log` | Follow live log output |
| `grep text file` | Search text in file |
| `grep -r word .` | Recursive text search |
| `awk '{print $1}' file` | Print first column |
| `sed 's/old/new/g' file` | Replace text globally |
| `sort file` | Sort lines alphabetically |
| `uniq file` | Remove duplicate lines |
| `cut -d: -f1 file` | Extract fields by delimiter |
| `wc -l file` | Count lines in file |
| `diff file1 file2` | Show differences between files |

---

## 4. User Management

| Command | Description |
|---------|-------------|
| `useradd john` | Create new user |
| `passwd john` | Set user password |
| `usermod -aG sudo john` | Add user to group |
| `userdel john` | Delete user |
| `userdel -r john` | Delete user and home directory |
| `groupadd devops` | Create new group |
| `groupdel devops` | Delete group |
| `groups john` | Show user groups |
| `id john` | Show user ID and groups |
| `who` | Show logged-in users |
| `last` | Show login history |
| `su - john` | Switch to another user |

---

## 5. Permissions

| Command | Description |
|---------|-------------|
| `chmod 777 file` | Full read/write/execute for all |
| `chmod 755 file` | Owner full, others read/execute |
| `chmod 644 file` | Owner read/write, others read only |
| `chmod +x script.sh` | Make file executable |
| `chmod -R 755 dir` | Recursive permission change |
| `chown user file` | Change file owner |
| `chown user:group file` | Change owner and group |
| `chgrp group file` | Change file group |
| `umask` | Show default permission mask |
| `stat file` | Show detailed file permissions |

---

## 6. Process Management

| Command | Description |
|---------|-------------|
| `ps -ef` | List all processes |
| `ps aux` | Detailed process list |
| `top` | Real-time process monitoring |
| `htop` | Interactive process monitoring |
| `kill PID` | Send SIGTERM to process |
| `kill -9 PID` | Force kill process (SIGKILL) |
| `pkill nginx` | Kill processes by name |
| `killall nginx` | Kill all matching processes |
| `jobs` | Show background jobs |
| `bg %1` | Resume job in background |
| `fg %1` | Bring job to foreground |
| `nohup app &` | Run process detached from terminal |
| `nice -n 10 app` | Run with lower priority |
| `pgrep nginx` | Find PID by process name |

---

## 7. Networking

| Command | Description |
|---------|-------------|
| `ip a` | Show IP addresses |
| `ip route` | Show routing table |
| `ping google.com` | Test connectivity |
| `traceroute google.com` | Trace network route |
| `nslookup google.com` | DNS lookup |
| `dig google.com` | Detailed DNS information |
| `ss -tulnp` | Show open ports and sockets |
| `netstat -tulnp` | Show network ports |
| `curl URL` | Make HTTP request |
| `wget URL` | Download file from URL |
| `scp file user@host:/tmp` | Secure copy to remote host |
| `ssh user@host` | SSH login to remote host |
| `ssh-keygen -t rsa` | Generate SSH key pair |
| `ssh-copy-id user@host` | Copy SSH key to server |
| `iptables -L` | List firewall rules |
| `ufw status` | Check UFW firewall status |

---

## 8. Package Management

| Command | Description |
|---------|-------------|
| `apt update` | Update package lists (Debian/Ubuntu) |
| `apt upgrade` | Upgrade all packages |
| `apt install nginx` | Install a package |
| `apt remove nginx` | Remove a package |
| `apt search nginx` | Search for a package |
| `apt list --installed` | List installed packages |
| `dpkg -l` | List all installed packages |
| `dpkg -i pkg.deb` | Install a .deb package |
| `yum install nginx` | Install package (RHEL/CentOS) |
| `yum update` | Update all packages (RHEL/CentOS) |
| `dnf install nginx` | Install package (Fedora/RHEL8+) |
| `rpm -qa` | List all installed RPM packages |
| `snap install app` | Install a snap package |

---

## 9. Disk Management

| Command | Description |
|---------|-------------|
| `df -h` | Show disk usage (human-readable) |
| `df -hT` | Show disk usage with filesystem type |
| `du -sh *` | Show size of each item in directory |
| `du -sh /var/log` | Show size of a specific directory |
| `lsblk` | List block devices |
| `fdisk -l` | List disk partitions |
| `fdisk /dev/sdb` | Partition a disk |
| `mkfs.ext4 /dev/sdb1` | Format partition as ext4 |
| `mount /dev/sdb1 /mnt` | Mount a partition |
| `umount /mnt` | Unmount a partition |
| `blkid` | Show block device UUIDs |
| `pvs / vgs / lvs` | Show LVM physical/volume/logical |
| `lvcreate -L 10G -n data vg0` | Create logical volume |

---

## 10. Service Management

| Command | Description |
|---------|-------------|
| `systemctl start nginx` | Start a service |
| `systemctl stop nginx` | Stop a service |
| `systemctl restart nginx` | Restart a service |
| `systemctl reload nginx` | Reload service config |
| `systemctl status nginx` | Check service status |
| `systemctl enable nginx` | Enable service at boot |
| `systemctl disable nginx` | Disable service at boot |
| `systemctl is-active nginx` | Check if service is active |
| `systemctl list-units` | List all active units |
| `systemctl daemon-reload` | Reload systemd configuration |

---

## 11. Logs

| Command | Description |
|---------|-------------|
| `journalctl -xe` | Show recent system logs |
| `journalctl -u nginx` | Show logs for a specific service |
| `journalctl -f` | Follow live system logs |
| `journalctl --since '1 hour ago'` | Show logs from past hour |
| `tail -f /var/log/syslog` | Follow syslog |
| `tail -f /var/log/auth.log` | Follow authentication log |
| `cat /var/log/nginx/access.log` | View nginx access logs |
| `grep ERROR /var/log/app.log` | Search for errors in log |
| `dmesg` | Show kernel ring buffer |
| `dmesg -T` | Show kernel logs with timestamps |

---

## 12. Shell Scripting

| Command | Description |
|---------|-------------|
| `#!/bin/bash` | Shebang — declare bash script |
| `echo "Hello $NAME"` | Print variable to stdout |
| `read -p 'Input: ' VAR` | Read user input into variable |
| `export VAR=value` | Export variable to environment |
| `if [ $x -eq 1 ]; then ... fi` | If condition block |
| `for i in {1..5}; do ... done` | For loop |
| `while [ condition ]; do ... done` | While loop |
| `function greet() { ... }` | Define a function |
| `$?` | Check last command exit status |
| `chmod +x script.sh` | Make script executable |
| `./script.sh` | Run a script |
| `bash -x script.sh` | Debug script (trace execution) |
| `$(command)` | Command substitution |
| `2>&1` | Redirect stderr to stdout |
| `>> file` | Append output to file |

---

## 13. Git Commands

| Command | Description |
|---------|-------------|
| `git init` | Initialize a new repository |
| `git clone URL` | Clone remote repository |
| `git status` | Show working tree status |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Commit with message |
| `git push origin main` | Push to remote branch |
| `git pull origin main` | Pull from remote branch |
| `git branch` | List branches |
| `git checkout dev` | Switch to branch |
| `git checkout -b feature` | Create and switch to new branch |
| `git merge dev` | Merge branch into current |
| `git rebase main` | Rebase current branch onto main |
| `git cherry-pick <hash>` | Apply a specific commit |
| `git log --oneline` | Compact commit history |
| `git stash` | Save uncommitted changes |
| `git stash pop` | Restore stashed changes |
| `git diff` | Show unstaged changes |
| `git reset --hard HEAD` | Discard all local changes |
| `git tag v1.0.0` | Create a version tag |

---

## 14. Docker Commands

| Command | Description |
|---------|-------------|
| `docker version` | Show Docker version |
| `docker images` | List local images |
| `docker ps` | Show running containers |
| `docker ps -a` | Show all containers |
| `docker pull nginx` | Pull image from registry |
| `docker build -t app .` | Build image from Dockerfile |
| `docker run nginx` | Run a container |
| `docker run -d -p 80:80 nginx` | Run detached with port mapping |
| `docker exec -it id bash` | Open shell in running container |
| `docker stop id` | Stop a container gracefully |
| `docker start id` | Start a stopped container |
| `docker rm id` | Remove a container |
| `docker rmi image` | Remove an image |
| `docker logs -f id` | Follow container logs |
| `docker inspect id` | Show container metadata |
| `docker network ls` | List Docker networks |
| `docker volume ls` | List Docker volumes |
| `docker compose up -d` | Start services from compose file |
| `docker compose down` | Stop and remove compose services |
| `docker system prune -a` | Remove all unused resources |

---

## 15. Kubernetes Commands

| Command | Description |
|---------|-------------|
| `kubectl cluster-info` | Show cluster info |
| `kubectl get nodes` | List cluster nodes |
| `kubectl get pods` | List pods in default namespace |
| `kubectl get pods -n kube-system` | List pods in a namespace |
| `kubectl get pods -A` | List pods across all namespaces |
| `kubectl get svc` | List services |
| `kubectl get deploy` | List deployments |
| `kubectl describe pod podname` | Show detailed pod information |
| `kubectl logs podname` | Show pod logs |
| `kubectl logs -f podname` | Follow pod logs live |
| `kubectl exec -it pod -- bash` | Open shell in pod |
| `kubectl apply -f app.yaml` | Apply a manifest file |
| `kubectl delete -f app.yaml` | Delete resources from manifest |
| `kubectl scale deploy app --replicas=3` | Scale deployment |
| `kubectl rollout status deploy/app` | Check rollout status |
| `kubectl rollout undo deploy/app` | Rollback a deployment |
| `kubectl top pod` | Show pod resource usage |
| `kubectl get namespaces` | List namespaces |
| `kubectl config view` | View kubeconfig |
| `kubectl config use-context ctx` | Switch cluster context |

---

## 16. AWS CLI Commands

| Command | Description |
|---------|-------------|
| `aws configure` | Configure AWS CLI credentials |
| `aws sts get-caller-identity` | Show current AWS account/user |
| `aws ec2 describe-instances` | List EC2 instances |
| `aws ec2 start-instances --instance-ids i-xxx` | Start EC2 instance |
| `aws ec2 stop-instances --instance-ids i-xxx` | Stop EC2 instance |
| `aws s3 ls` | List S3 buckets |
| `aws s3 cp file s3://bucket/path` | Upload file to S3 |
| `aws s3 sync ./dir s3://bucket` | Sync directory to S3 |
| `aws s3 rm s3://bucket/file` | Delete file from S3 |
| `aws iam list-users` | List IAM users |
| `aws iam create-user --user-name dev` | Create IAM user |
| `aws eks list-clusters` | List EKS clusters |
| `aws eks update-kubeconfig --name cluster` | Update kubeconfig for EKS |
| `aws ecr describe-repositories` | List ECR repositories |
| `aws lambda list-functions` | List Lambda functions |
| `aws cloudformation list-stacks` | List CloudFormation stacks |
| `aws logs tail /aws/lambda/fn` | Tail CloudWatch Logs |

---

## 17. Terraform Commands

| Command | Description |
|---------|-------------|
| `terraform init` | Initialize working directory |
| `terraform validate` | Validate configuration files |
| `terraform fmt` | Format code to standard style |
| `terraform plan` | Preview changes before applying |
| `terraform apply` | Apply infrastructure changes |
| `terraform apply -auto-approve` | Apply without confirmation prompt |
| `terraform destroy` | Destroy all managed resources |
| `terraform state list` | List resources in state |
| `terraform state show res` | Show state for a resource |
| `terraform import addr id` | Import existing resource into state |
| `terraform output` | Show output values |
| `terraform workspace list` | List workspaces |
| `terraform workspace new dev` | Create a new workspace |
| `terraform workspace select dev` | Switch to a workspace |
| `terraform refresh` | Sync state with real infrastructure |

---

## 18. Ansible Commands

| Command | Description |
|---------|-------------|
| `ansible --version` | Show Ansible version |
| `ansible all -m ping` | Ping all hosts in inventory |
| `ansible all -m shell -a 'uptime'` | Run command on all hosts |
| `ansible-playbook site.yml` | Run a playbook |
| `ansible-playbook site.yml --check` | Dry run a playbook |
| `ansible-playbook site.yml -v` | Run playbook with verbose output |
| `ansible-playbook site.yml --tags db` | Run only tagged tasks |
| `ansible-inventory --list` | Show inventory as JSON |
| `ansible-inventory --graph` | Show inventory as a tree |
| `ansible-galaxy install role` | Install a role from Galaxy |
| `ansible-galaxy init myrole` | Create a new role scaffold |
| `ansible-vault create secrets.yml` | Create encrypted vault file |
| `ansible-vault edit secrets.yml` | Edit encrypted vault file |
| `ansible-vault decrypt secrets.yml` | Decrypt a vault file |

---

## 19. Monitoring Commands

| Command | Description |
|---------|-------------|
| `top` | Real-time CPU/memory monitoring |
| `htop` | Interactive process monitoring |
| `free -h` | Show memory usage |
| `vmstat 1` | Virtual memory stats every second |
| `iostat -x 1` | Extended disk I/O stats |
| `sar -u 1 5` | CPU usage over 5 seconds |
| `df -h` | Disk space usage |
| `du -sh *` | Directory sizes |
| `iotop` | Real-time disk I/O per process |
| `nethogs` | Network usage per process |
| `iftop` | Real-time network bandwidth |
| `uptime` | System uptime and load average |
| `lscpu` | CPU architecture information |

---

## 20. Troubleshooting Commands

| Command | Description |
|---------|-------------|
| `journalctl -xe` | View recent system error logs |
| `dmesg \| tail -50` | Recent kernel messages |
| `systemctl status nginx` | Check service status and logs |
| `curl -I localhost:8080` | Test HTTP service response headers |
| `nslookup domain.com` | Check DNS resolution |
| `dig domain.com +short` | Quick DNS lookup |
| `ping -c 4 host` | Test network connectivity |
| `traceroute host` | Trace network path to host |
| `ss -tulnp \| grep 80` | Check what is on port 80 |
| `netstat -rn` | Show routing table |
| `strace -p PID` | Trace system calls of a process |
| `lsof -p PID` | List files opened by process |
| `lsof -i :80` | List processes using port 80 |
| `tcpdump -i eth0 port 80` | Capture packets on port 80 |

---

## 👨‍💻 Author

**Manish Deore**

DevOps Engineer | AWS | Docker | Kubernetes | Terraform | Linux

⭐ Star this repository if it helps your learning journey!
