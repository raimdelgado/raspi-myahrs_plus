 raspi-myahrs_plus
===================

##raspberry pi 3 i2c slave - Myahrs+
device site : http://www.withrobot.com/myahrs_plus/

device repository : https://github.com/withrobot/myAHRS_plus

##Connectivity myahrs+ & raspberry pi3  
myahrs +        //  raspberry pi3  

j3-3(I2C_SCL)    --  pin 3(Physical)  

j3-4(I2C_SDA)    --  pin 5(physical)    

j4-1(VDD)        --  pin 2,4(physical)   

j4-10(GND)       --  pin 6,9,14,20,25,30,34(physical)
  
  
##How to enable i2c bus on raspeberry pi3

(raspberrypi) $ sudo raspi-consig

>enter 5.interfacing option

>>enter 5.I2C

>>>enable

(raspberrypi) $ sudo echo i2c-dev >> /etc/modules

(raspberrypi) $ reboot

after reboot,

(raspberrypi) $ lsmod

>check i2c_dev

(raspberrypi) $ ls /dev/i2c*

>check i2c-1

(raspberrypi) $ i2cdetect -y 1

>check 0x20
