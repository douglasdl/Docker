# Docker

## Windows

Install the WSL2
```sh
wsl --install
```

```sh
NAME                                   FRIENDLY NAME
Ubuntu                                 Ubuntu
Debian                                 Debian GNU/Linux
kali-linux                             Kali Linux Rolling
Ubuntu-18.04                           Ubuntu 18.04 LTS
Ubuntu-20.04                           Ubuntu 20.04 LTS
Ubuntu-22.04                           Ubuntu 22.04 LTS
OracleLinux_7_9                        Oracle Linux 7.9
OracleLinux_8_7                        Oracle Linux 8.7
OracleLinux_9_1                        Oracle Linux 9.1
openSUSE-Leap-15.5                     openSUSE Leap 15.5
SUSE-Linux-Enterprise-Server-15-SP4    SUSE Linux Enterprise Server 15 SP4
SUSE-Linux-Enterprise-15-SP5           SUSE Linux Enterprise 15 SP5
openSUSE-Tumbleweed                    openSUSE Tumbleweed
```

Install the WSL2 Ubuntu image:
```sh
wsl --install -d Ubuntu
```

Update the Linux packages:
```sh
sudo apt update
```

Install the packages:
```sh
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Add Docker-Ubuntu's repository key to APT's trusted package sources:
```sh
curl --fail --silent --show-error --location https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Install manager for software repositories:
```sh
sudo apt-get install software-properties-common
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
```

Check availability of the docker-ce package:
```sh
apt-cache policy docker-ce
```

Install the docker-ce package:
```sh
sudo apt-get install -y docker-ce
```

Check Docker is running:
```sh
sudo systemctl status docker
```

Add your user to the docker group:
```sh
sudo usermod -aG docker ${USER}
```

Check Docker is installed:
```sh
docker --version
```

Check Docker compose is installed:
```sh
docker-compose --version
```

