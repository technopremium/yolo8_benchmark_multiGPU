# Automated mode 
```bash
/bin/bash -c "$(curl -fsSL https://bizon-vm.s3.amazonaws.com/Install_yolo_training.sh)"
```


# Installing the conda environment, downloading dataset and running the code `Manually`
```bash
cd /home/bizon/
git clone https://github.com/technopremium/yolo8_benchmark_multiGPU.git
cd yolo8_benchmark_multiGPU
conda env create -f environment.yml
conda activate testenv 
cp healthcheck.zip /home/bizon/
cd /home/bizon/
unzip healthcheck.zip
cd /home/bizon/healthcheck/ultralytics
```

# Parameters to run the training 
```bash
python train_test.py --batch 8 --device 0 --epochs 60
```
# IPMI tool monitoring installation
```bash
sudo apt install ipmitool
sudo modprobe ipmi_si
sudo ipmitool sdr
chmod +x monitor.sh
```





