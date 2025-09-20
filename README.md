Got it ✅ I’ll generate a **GitHub-formatted `README.md`** with badges for the tools mentioned in your installation guide. Here’s a clean and professional version:

````markdown
# VLSI Tool Installation Guide 🚀

[![Yosys](https://img.shields.io/badge/Yosys-Open_Source-blue)](https://github.com/YosysHQ/yosys)
[![Icarus Verilog](https://img.shields.io/badge/Icarus_Verilog-iverilog-red)](http://iverilog.icarus.com/)
[![GTKWave](https://img.shields.io/badge/GTKWave-Waveform_Viewer-brightgreen)](http://gtkwave.sourceforge.net/)
[![NGSpice](https://img.shields.io/badge/Ngspice-Circuit_Simulator-orange)](https://sourceforge.net/projects/ngspice/)
[![Magic](https://img.shields.io/badge/Magic-Layout_Tool-yellow)](https://github.com/RTimothyEdwards/magic)
[![OpenLANE](https://img.shields.io/badge/OpenLANE-Digital_Flow-purple)](https://github.com/The-OpenROAD-Project/OpenLane)
[![Docker](https://img.shields.io/badge/Docker-Container_Platform-blue)](https://www.docker.com/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%2B-orange)](https://ubuntu.com/)

---

## 📌 System Requirements

- **RAM**: 6 GB minimum  
- **Disk**: 50 GB HDD  
- **CPU**: 4 vCPU  
- **OS**: Ubuntu 20.04+  

---

## ⚙️ Installation Instructions

### 1️⃣ Yosys
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install
````

---

### 2️⃣ Icarus Verilog (iverilog)

```bash
sudo apt-get update
sudo apt-get install iverilog
```

---

### 3️⃣ GTKWave

```bash
sudo apt-get update
sudo apt install gtkwave
```

---

### 4️⃣ Ngspice

```bash
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release && cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install
```

---

### 5️⃣ Magic

```bash
sudo apt-get install m4 tcsh csh libx11-dev \
    tcl-dev tk-dev libcairo2-dev mesa-common-dev \
    libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```

---

### 6️⃣ OpenLANE

```bash
sudo apt-get update && sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
sudo apt install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o \
/usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world

sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot
```

After reboot:

```bash
docker run hello-world
```

Dependencies check:

```bash
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h
```

Install PDKs and tools:

```bash
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```

---

## 📚 References

* [YosysHQ](https://github.com/YosysHQ/yosys)
* [OpenLANE Project](https://github.com/The-OpenROAD-Project/OpenLane)
* [Magic VLSI](https://github.com/RTimothyEdwards/magic)
* [Ngspice](https://sourceforge.net/projects/ngspice/)

---

## ✅ Tasks

* [x] Create GitHub repo and document tool installation
* [x] Install tools with given configuration
* [ ] Upload tool snapshots to repo

---

🔧 Happy Hacking with Open-Source VLSI Tools!

```

Would you like me to also **include a section with screenshots placeholders** (like `![yosys](docs/images/yosys.png)`) so you can later upload snapshots of installed tools?
```
