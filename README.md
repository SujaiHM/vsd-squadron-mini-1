# Mahesh CS
# A 4-week Research Internship on RISC-V using VSDSquadron Mini RISC-V Dev Board

[Click here for board link](https://www.vlsisystemdesign.com/vsdsquadronmini/)




BOARD SPECS:

| CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set |
| ------------------------------------------------------------------------- 
| SRAM                                                                       2kb onchip volatile sram     16kb external program memory                                    |
| Processor                                                                  24 MHz                                                                                       |
| Sink Current per I/O Pin                                                   8 mA                                                                                         |
| Source Current per I/O Pin                                                 8 mA                                                                                         |
| Input voltage (nominal)                                                    5 V                                                                                          |
| I/O voltage                                                                3.3 V                                                                                        |
| Programmer/debugger                                                        Onboard RISC-V programmer/debugger, USB to TTL serial port support                           |
| SPI                                                                        1x, PC5(SCK), PC1(NSS), PC6(MOSI), PC7(MISO)                                                 |
| I2C                                                                        1x, PC1(SDA), PC2(SCL)                                                                       |
| USART                                                                      1x, PD6(RX), PD5(TX)                                                                         |
| External interrupts                                                        8 external interrupt edge detectors, but it only maps one external interrupt to 18 I/O ports |
| PWM pins                                                                   14X                                                                                          |
| Analog I/O pins                                                            10-bit ADC, PD0-PD7, PA1, PA2, PC4                                                           |
| Digital I/O pins                                                           15                                                                                           |
| Built-in LED Pin                                                           1X onboard user led (PD6)                                                                    |
| USB 2.0 Type-C                                                            
   

This repo is intended to document the weekly progress.
### The first online meet was held on 16th of Feb 2024 @6PM

<details>
    <summary> TASK 1 </summary>

1) install RISC-V GNU Toolchain 

2) install Yosys 

3) install iverilog 

4) install gtkwave

### CLONING RISC-V GNU TOOLCHAIN

```sudo apt install git-all```   # To install git

```sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev``` *make sure to install the dependencies*

![gnu_dependencies]

```git clone https://github.com/riscv/riscv-gnu-toolchain```

![gnu_toolchain_clone][[Uploading 1.html…]()




## Create a opt dir
```mkdir /opt/riscv```  *try sudo incase of permission denial*

In my case I created a driectory ```mkdir riscv``` and ``` chmod 777 home/nawras/riscv ```

## Config and make inside the risc-v gnu toolchain dir 

```./configure --prefix=/opt/riscv```  

In my case ```./configure --prefix=/home/nawras/riscv```  

Then
```make``` **(Have patience)**


![WhatsApp Image 2024-02-22 at 5 22 13 PM](https://github.com/MAHESH-CS/vsd-squadron-mini/assets/160752185/47e45966-fb1e-4aa8-b11c-9297c767f5fd)

### INSTALLING IVERILOG GTKWAVE & YOSYS

### YOSYS

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys 
sudo apt-get install build-essential clang bison flex \libreadline-dev gawk tcl-dev libffi-dev git \ graphviz xdot pkg-config python3 libboost-system-dev\libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make 
sudo make install
```

![WhatsApp Image 2024-02-22 at 5 22 42 PM](https://github.com/MAHESH-CS/vsd-squadron-mini/assets/160752185/dfecb0b6-f280-470d-a204-6a98452484b6)





### iVerilog

```
sudo apt-get install iverilog
```

![WhatsApp Image 2024-02-22 at 5 23 17 PM](https://github.com/MAHESH-CS/vsd-squadron-mini/assets/160752185/e97246dd-0af8-4271-9a79-d66babaf900e)

### GTkWave
``` sudo apt-get install gtkwave ```

![WhatsApp Image 2024-02-22 at 5 23 48 PM](https://github.com/MAHESH-CS/vsd-squadron-mini/assets/160752185/3aaf14ce-18b8-430b-9b2b-905d27a42307)

</details>

