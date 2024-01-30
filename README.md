# Ch2i_RAK3172_Phy_PingPong with display
Made on the basis of the [Ch2i_RAK3172_Phy_PingPong](https://github.com/osnatos/Ch2i_RAK3172_Phy_PingPong) project to which a display has been added.

**Motivation:**

When using two Ping-Pong devices  in experiments with the reception range depending on various factors, It is useful, at least on one of them, to have an indication of communication quality parameters (Rssi, Snr, etc).

**Hardware:**

1. [Hallard's RAK3172 breakout board](https://github.com/hallard/RAK3172-Breakout).

2. Display [0.96" OLED LCD](https://www.aliexpress.com/item/32639731302.html?spm=a2g0o.cart.0.0.3cfc38davjhG6V&mp=1&gatewayAdapt=glo2isr).

​       128*64 LED display module

​       Interface: I2C

​       Driver IC: SSD1306

​       Pin Definition: GND, VCC ,SCL, SDA

​       Pin Connection:

​       GND ->GND, VCC->3.3V, SCL->SCL, SDA->SDA.

​       Connect SCL and SDA pins to the PulUp resistors 5.1k, connected to 3.3V.

3. Power and communication unit.

   For this unit I chose [USB-to-Serial adapter](https://www.aliexpress.com/item/1005002967540364.html?spm=a2g0o.order_detail.order_detail_item.5.5137f19c1TsAGS) and [AMS1117-3.3V Power Supply Module](https://www.aliexpress.com/item/32588261370.html?spm=a2g0o.productlist.main.7.42fa40d0BRPrej&algo_pvid=23550f80-46c5-4aae-ae04-c17b4f9743f5&aem_p4p_detail=202309080848275266674755863170000668337&algo_exp_id=23550f80-46c5-4aae-ae04-c17b4f9743f5-3&pdp_npi=4%40dis%21USD%211.32%211.19%21%21%211.32%21%21%40211b600416941881075516364ef64b%2112000028511462099%21sea%21IL%21190886090%21&curPageLogUid=X5XFrAF0wRsc&search_p4p_id=202309080848275266674755863170000668337_4) for conversion VBUS (+5V) to +3.3V for RAK3172 VDD. 

   When connected to a PC  via a USB cable, the unit provides Rx, Tx signals and 3.3V (from supply module but not from serial adapter).
   The signals level from serial adapter is 5V, but the Rx (PA3) and Tx (PA2) signals of the RAK3172 module, which uses [STM32WLE5CCUx](https://www.st.com/resource/en/datasheet/stm32wle5c8.pdf), are 5V tolerant (see tables 19 and 20 pages 52 and 54).

   

   When the device operates without connecting to a PС, you can use a [Power Bank](https://www.aliexpress.com/item/32992537707.html?spm=a2g0o.order_list.order_list_main.425.34d61802qL87i8) and a short (25 cm) [USB cable](https://www.aliexpress.com/item/1005004407881570.html?spm=a2g0o.order_list.order_list_main.59.21ef1802UW1LtL) to power it.

   

   **Photo:**
   
   ![](https://github.com/osnatos/Ch2i_RAK3172_Phy_PingPong_with_display/blob/master/Ch2i_RAK3172_Phy_PingPong_with_display.jpg)
   The photo shows the mock-up of the device in the experiment.
   
   
   The device on the right is **[Feather_RAK3172_Phy_PingPong](https://github.com/osnatos/Feather_RAK3172_Phy_PingPong)** device.
   
   
   Both devices are powered by Power Bank (Power Bank of the second device is not shown).
   
   
   
   
   
   
