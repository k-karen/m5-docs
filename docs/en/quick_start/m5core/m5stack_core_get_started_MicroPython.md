# UIFlow Quick Start

?>This tutorial applies to BASIC / GRAY / M5GO / FIRE / FACES kit

## Driver Installation

> Before the program is burned, M5Core host (including BASIC / GRAY / M5GO / FIRE / FACES) users please download the corresponding CP210X driver package according to the operating system you use. After decompressing the package，select the corresponding installation package base on your operating system digits.

* __Download CP2104 driver__

<div class="files_download">
   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/drivers/CP210x_VCP_Windows.zip">
      <img src="/image/base/Windows_logo.webp" width="50">
      <span class="item-title">Windows10</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/drivers/CP210x_VCP_MacOS.zip">
      <img src="/image/base/MacOS_logo.webp" width="50"> 
      <span class="item-title">MacOS</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/drivers/CP210x_VCP_Linux.zip">
      <img src="/image/base/Linux_logo.webp" width="50"> 
      <span class="item-title">Linux</span>
      </a>
   </p>
</div>

><img src="/image/base/CP210X_install.gif " width="70%">

?> For Mac OS, make sure System preferences - > Security & Privacy - > General before installing, and allow the apps to be installed from the App Store and ident
ified developers

><img src="/image/base/System_preferences.webp" width="50%">


## M5Burner

> Please click the button below to download the corresponding M5Burner firmware burning tool according to your operating system. Unzip and open the application.

<div class="files_download">
   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/M5Burner.zip">
      <img src="/image/base/Windows_logo.webp" width="50">
      <span class="item-title">Windows10</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/M5Burner_MacOS.zip">
      <img src="/image/base/MacOS_logo.webp" width="50"> 
      <span class="item-title">MacOS</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/M5Burner_Linux.zip">
      <img src="/image/base/Linux_logo.webp" width="50"> 
      <span class="item-title">Linux</span>
      </a>
   </p>
</div>


<img src="assets/img/getting_started_pics/how_to_burn_firmware/M5Burner/M5Burner_01.webp">

?>Note: MacOS users please put M5Burner App in the Application folder after the installation as shown in the figure below.

><img src="/image/base/application.webp" width="70%"> 

## Firmware burning

> 1. Double-click the Burner burning tool and click the download button in the left menu according to the firmware version you need. Then,  connect the M5 device to the computer via a Type-C data cable, select the corresponding COM, baud rate , as well as the type of your programming device.

?>Note: M5Burner includes different UIFlow firmware versions from different M5Stack products. Therefore, you need to select the correct device type before proceeding with the burning process to obtain the firmware that matches the device, as shown in the figure below. (The default burning rate of the configuration can be chosen. In special cases like malfunction of the burning process, you can try to reduce the burning rate to 115200).

<img src="/image/base/device_select.webp" width="70%"> 

> 2. Select the firmware version you want to burn, connect the device to the computer via Type-C data cable, select the corresponding COM port and device type. Click "Burn" to start burning. When the burning log prompts ' Hard resetting via RTS pin ', it means the firmware has finished burning already.

?> When first burning or the firmware program runs abnormally, you can click "Erase" to erase the flash memory so that there is no need to erase again in the subsequent firmware update. Otherwise, the Wi-Fi information which is saved already will be deleted and the API Key will be refreshed.

<img src="/image/base/Burner_user.gif " width="70%">

## Configure WIFI

> UIFlow provides both offline and web version of the programmer. When using the web version, we need to configure a WiFi connection for the device. The following describes two ways to configure WiFi connection for the device (Burn configuration and AP hotspot configuration).

### Burn configuration WiFi

?> UIFlow-1.4.5 and the above versions are in support of the pre-burning configuration under WIFI connnection. All users need to do is to fill in WIFI configuration box before setting your firmware to burn. After the configuration of WIFI, clicking 'Burn' to start firmware burning so that the WIFI infomation you filled in together with your firmware will be burned and stored into your M5 device.

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\m5burner_wifi.webp " width="70%">

### AP hotspot configuration WiFi

> 1. Click the red power button on the left side of the device to turn it on, press button A once the UIFlow Logo appears on the screen, and use a mobile phone to connect to the wifi hotspot displayed on the device screen

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\uiflow_wifi_setup1.webp ">

> 2. After successfully connecting to the hotspot with your mobile phone, open the mobile phone browser to scan the QR code on the screen or directly access __192.168.4.1__, enter the page to fill in your personal WIFI information, and click Configure to record your WiFi information. The device will restart automatically after successful configuration and enter programming mode.

?> Note: Special characters such as "space" are not allowed in the configured WiFi information.

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\uiflow_wifi_setup2.webp ">

## Network Programming Mode and API KEY

#### Enter network programming mode

?> Network programming mode is a docking mode between M5 device and UIFlow web programming platform. The screen will show the current network connection status of the device. When the indicator is green, it means that you can receive program push at any time. Under default situation, after the first successful WiFi network configuration, the device will automatically restart and enter the network programming mode. If you do not know how to re-enter the programming mode after running other applications, you can refer to the following operations.

> After turning on your device, you can enter the coding mode by pushing the left button on the front surface of the device once the screen shows UIFlow logo. When the indicator on the coding page turns color from red to green, you can visit website [flow.m5stack.com](http://flow.m5stack.com/) in your computer browser to access UIFlow coding page.

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\uiflow_program_mode.webp ">


#### API KEY

> API KEY is the communication credential for M5 devices when using UIFlow web programming. By configuring the corresponding API KEY on UIFlow side, programs can be pushed for the specific devices. The user needs to visit [flow.m5stack.com](http://flow.m5stack.com/) in the computer web browser to enter the UIFlow programming page . Click the setting button in the menu bar at the upper right corner of the page, enter the API Key on the corresponding device, select the hardware for connecting, click OK to save and wait till it prompts successfully connecting

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\uiflow_apikey.webp ">


## Hello M5
 
> With the above steps being settled, you can start programming with UIFlow. The following will show you a simple program that drives the screen to display "Hello M5". (1. Place a label 2. Add a label program block .3 Click the run button in the upper right corner)

<img src="assets\img\getting_started_pics\m5stack_core\get_started_with_uiflow\hello_m5.gif ">


## UIFlow Desktop IDE

> UIFlow Desktop IDE is an offline version of UIFlow programmer which does not require network connection, and can provide you with responsive program push experience. Please click the corresponding version of **UIFlow-Desktop-IDE** to download according to your operating system .

<div class="files_download">
   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/UIFlow-Desktop-IDE.zip">
      <img src="/image/base/Windows_logo.webp" width="50">
      <span class="item-title">Windows10</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/UIFlow-Desktop-IDE_MacOS.zip">
      <img src="/image/base/MacOS_logo.webp" width="50"> 
      <span class="item-title">MacOS</span>
      </a>
   </p>

   <p class="item">
      <a href="https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/software/UIFlow-Desktop-IDE_Linux.zip">
      <img src="/image/base/Linux_logo.webp" width="50"> 
      <span class="item-title">Linux</span>
      </a>
   </p>
</div>


#### USB programming mode

> Unzip the downloaded UIFlow Desktop IDE archive and double-click to run the application.

<img src="assets/img/related_documents/UIFlow_Desktop_IDE/Desktop_IDE_01.webp">

?> After the app starts, it will automatically detect whether your computer has a USB driver (CP210X), click Install, and follow the prompts to finish installation.

<img src="assets/img/related_documents/UIFlow_Desktop_IDE/Desktop_IDE_02.webp">

> After the driver installation is completed, it will automatically enter the UIFlow Desktop IDE with the configuration box popping up. At this time, connect the M5 device to the computer via the Tpye-C data cable.

<img src="assets/img/related_documents/UIFlow_Desktop_IDE/Desktop_IDE_03.webp">

!> Using UIFlow Desktop IDE requires M5 device with UIFlow firmware and enter ** USB programming mode **.

> Click the power button on the left side of the device to restart. Quickly select Setup after entering the menu, enter the configuration page, and select ** USB mode **.

<img src="assets/img/related_documents/UIFlow_Desktop_IDE/Desktop_IDE_04.webp">

> Select the corresponding port, and the programming device, click OK to connect.

<img src="assets/img/related_documents/UIFlow_Desktop_IDE/Desktop_IDE_05.webp">


## Related Videos

-Introduction to UIFlow

<video width="500" controls>
    <source src="https://m5stack.oss-cn-shenzhen.aliyuncs.com/video/LukeVideo/UI%20Flow%20Overview.mp4" type="video/mp4">
</video>

-Video tutorial for developing M5Core in UIFlow

<video width="500" controls>
    <source src="https://m5stack.oss-cn-shenzhen.aliyuncs.com/video/%E6%95%99%E7%A8%8B/UIFlow%20Tutorials/A3%20-%20UIflow%E7%AE%80%E4%BB%8B.mp4" type="video/mp4">
</video>


## Related Links

* [M5GO Programming Tutorial](https://m5stack.oss-cn-shenzhen.aliyuncs.com/resource/docs/UIFlow-Book-zh_cn.pdf)
* [UIFlow Block introduction](en/uiflow/uiflow_home_page)


<script>
   anchor_search();
   scrollFunc();
</script>
