#Raspberry PI3PI2/B+LCD Directions for use：
---
##**_(a)_**.the quickly way is that use the complied os image to install on your sd card.（click [rpi_35_v5_jessie8_kernel_4_1_19](https://mega.nz/#!EohikbAJ!TbvPnGggEZfaBsw_6Y49WpAsIb6h4-7MmNgw9Ux5SHY) to download the OS image.）


---
##**_(b)_**.install the driver as following steps:（click [LCD_show_v5](https://mega.nz/#!chgnDLoA!OIVu199nFAUL9_1i8scDd0gKNcBtEi3NlzxCPVLuDy4) to download the driver file.）

 1.Burn write your os image to the SD card, and then reboot the Raspberry Pi

 2.make sure that your network state is ok

 3.make sure that your lcd connected to raspberry pi is correct

 4.copy the driver file to rapspberry pi(use ssh or mount)

 5.unzip the driver file and install as following steps:

      ##expand sd card capacity:                   
      
      sudo  raspi-config</font>
      
      ##choose expand_roofts then: 
      sudo reboot

      ##after reboot the execute the following steps:

      ##unzip file               
      tar -xzvf LCD_show_v5.tar.gz

      ##cd to dest dir            
      cd  LCD_show_v5

      ##update:
      sudo apt-get update

      ##back data:                         
      sudo ./LCD_backup

      ##install driver:                
      sudo ./LCD35_v5

      ##wait a minute os will install the driver and automatic restart
 
      ##if you want to use the previous os ,you can execute:
      sudo ./LCD_restore

      ##note: before you update your os,you must execute this command:
      
      sudo apt-mark hold raspberrypi-bootloader
    
      ##and execute the following commands:
    
      sudo apt-get update 
      sudo apt-get upgrade

otherwise the operation may fail after reboot


Pins Definition：

1   ----> 3v

2   ----> 5v

3   ----> NC

4   ----> 5V

19 ----> MOSI

20 ----> GND

21 ----> MISO

22 ----> TP_IRQ

23 ----> SCLK

24 ----> TP_CS

25 ----> GND

26 ----> LCD_CS

Others are NC！
