## Sheet1

| 广州市星翼电子科技有限公司（ALIENTEK） |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| STM32F407核心板 IO资源分配表 |  |  |  |  |  | 使用提示 | 是否引出 |
| 引脚编号 | GPIO | 连接资源 |  | 完全<br>独立 | 连接关系说明 |  |  |
| 34 | PA0 | WK_UP |  | N | 按键KEY_UP | 普通按键使用、待机模式唤醒 | N |
| 35 | PA1 |  |  | Y |  |  | Y |
| 36 | PA2 | USART2_TX |  | Y |  |  | Y |
| 37 | PA3 | USART2_RX |  | Y |  |  | Y |
| 40 | PA4 | STM_DAC | DCMI_HREF | Y | 1，DAC_OUT1输出脚<br>2，OLED/CAMERA接口的HREF引脚 | 该IO可做DAC输出，同时也连接在OLED/CAMERA接口，如不插外设在OLED/CAMERA接口，则可以完全独立 | Y |
| 41 | PA5 | STM_ADC |  | Y | ADC输入引脚，同时做TPAD检测脚 |  | Y |
| 42 | PA6 | DCMI_PCLK |  | Y | OLED/CAMERA接口的PCLK脚 | 仅连接OLED/CAMERA接口的PCLK，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 43 | PA7 |  |  | Y |  |  | Y |
| 100 | PA8 | DCMI_XCLK |  | Y | OLED/CAMERA接口的XCLK脚 | 摄像头XCLK为输入时钟，通常不使用，该IO完全独立 | Y |
| 101 | PA9 | USART1_TX |  | Y | 串口1 TX脚，连接CH340C的RX(跳帽设置) | 该IO通过跳帽选择是否连接CH340的RXD，如果不连接，则该IO完全独立 | Y |
| 102 | PA10 | USART1_RX |  | Y | 串口1 RX脚，连接CH340C的TX(跳帽设置) | 该IO通过跳帽选择是否连接CH340的TXD，如果不连接，则该IO完全独立 | Y |
| 103 | PA11 | USB_D- |  | Y | USB D-引脚(P11设置) | 不接入USB时，则该IO完全独立 | Y |
| 104 | PA12 | USB_D+ |  | Y | USB D+引脚(P11设置) | 不接入USB时，则该IO完全独立 | Y |
| 105 | PA13 | SWDIO |  | N | SWD仿真接口,没接任何外设 | SWD下载仿真接口，没连外设。如不用仿真，SWDIO和SWDCLK两个信号可以做普通IO用(注意：作普通IO需程序中禁止SWD，禁止后无法再次SWD下载，需按住KEY0上电方可再次下载) | SWD引出 |
| 109 | PA14 | SWDCLK |  | N | SWD仿真接口,没接任何外设 |  | SWD引出 |
| 110 | PA15 |  |  | Y |  |  | Y |
| 46 | PB0 | T_SCK |  | Y | TFTLCD接口触摸屏SCK信号 | 该IO接TFTLCD模块接口的触摸屏SCK信号，当不插TFTLCD模块时，该IO完全独立 | Y |
| 47 | PB1 | T_PEN |  | Y | TFTLCD接口触摸屏PEN信号  | 该IO接TFTLCD模块接口的触摸屏PEN信号(中断)，当不插TFTLCD模块时，该IO完全独立 | Y |
| 48 | PB2 | BOOT1 | T_MISO | N | 1，BOOT1,启动选择配置引脚(仅上电时用)<br>2，TFTLCD接口触摸屏MISO信号 | 该IO在上电时，作BOOT1用(由B1控制上拉/下拉，设置启动模式)，同时作为TFTLCD模块接口的触摸屏MISO信号，如不插TFTLCD模块，则可做普通IO用(有10K上拉/下拉,B0控制) | Y |
| 133 | PB3 | SPI1_SCK |  | N | W25Q128的SCK信号 | SPI1_SCK信号，禁止W25Q128的片选信号，则可以做普通IO用 | Y |
| 134 | PB4 | SPI1_MISO |  | N | W25Q128的MISO信号 | SPI1_MISO信号，禁止W25Q128的片选信号，则可以做普通IO用 | Y |
| 135 | PB5 | SPI1_MOSI |  | N | W25Q128的MOSI信号 | SPI1_MOSI信号，禁止W25Q128的片选信号，则可以做普通IO用 | Y |
| 136 | PB6 | DCMI_D5 |  | Y | OLED/CAMERA接口的D5脚 | 仅连接OLED/CAMERA接口的D5，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 137 | PB7 | DCMI_VSYNC |  | Y | OLED/CAMERA接口的VSYNC脚 | 仅连接OLED/CAMERA接口的VSYNC，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 139 | PB8 | IIC_SCL |  | N | 接24C02的SCL | 该IO连接24C02的SCL信号，有4.7K上拉电阻，不建议作为普通IO使用 | N |
| 140 | PB9 | IIC_SDA |  | N | 接24C02的SDA | 该IO连接24C02的SDA信号，有4.7K上拉电阻，不建议作为普通IO使用 | N |
| 69 | PB10 | USART3_TX |  | Y |  |  | Y |
| 70 | PB11 | USART3_RX |  | Y |  |  | Y |
| 73 | PB12 |  |  | Y |  |  | Y |
| 74 | PB13 |  |  | Y |  |  | Y |
| 75 | PB14 | F_CS |  | N | W25Q128的片选信号 | 该IO接W25Q128的片选信号，不建议做普通IO使用 | N |
| 76 | PB15 | LCD_BL |  | Y | TFTLCD接口背光控制脚  | 该IO接TFTLCD模块接口的背光控制脚(BL)，当不插TFTLCD模块时，该IO完全独立 | Y |
| 26 | PC0 |  |  | Y |  |  | Y |
| 27 | PC1 |  |  | Y |  |  | Y |
| 28 | PC2 |  |  | Y |  |  | Y |
| 29 | PC3 |  |  | Y |  |  | Y |
| 44 | PC4 |  |  | Y |  |  | Y |
| 45 | PC5 |  |  | Y |  |  | Y |
| 96 | PC6 |  | DCMI_D0 | Y | OLED/CAMERA接口的D0脚 | 接OLED/CAMERA接口的D0，当不使OLED/CAMERA接口时，可以做普通IO用 | Y |
| 97 | PC7 |  | DCMI_D1 | Y | OLED/CAMERA接口的D1脚 | 连接OLED/CAMERA接口的D1，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 98 | PC8 | SDIO_D0 | DCMI_D2 | N | 1，SD卡接口的D0<br>2，OLED/CAMERA接口的D2脚 | 接SD卡接口的D0和OLED/CAMERA接口的D2，有47K上拉电阻，当不使用SD卡和OLED/CAMERA接口时，可做普通IO使用 | Y |
| 99 | PC9 | SDIO_D1 | DCMI_D3 | N | 1，SD卡接口的D1<br>2，OLED/CAMERA接口的D3脚 | 接SD卡接口的D1和OLED/CAMERA接口的D3，有47K上拉电阻，当不使用SD卡和OLED/CAMERA接口时，可做普通IO使用 | Y |
| 111 | PC10 | SDIO_D2 |  | N | SD卡接口的D2 | 仅连接SD卡接口的D2，有47K上拉电阻，当不使用SD卡时，可做普通IO使用 | Y |
| 112 | PC11 | SDIO_D3 |  | N | SD卡接口的D3 | 仅连接SD卡接口的D3，有47K上拉电阻，当不使用SD卡时，可做普通IO使用 | Y |
| 113 | PC12 | SDIO_SCK | DCMI_D4 | Y | 1，SD卡接口的SCK<br>2，OLED/CAMERA接口的D4脚 | 接SD卡接口的SCK和OLED/CAMERA接口的D4，当不使用SD卡和OLED/CAMERA接口时，可做普通IO使用 | Y |
| 7 | PC13 | T_CS |  | Y | TFTLCD接口触摸屏CS信号 | 该IO接TFTLCD模块接口的触摸屏CS信号，当不插TFTLCD模块时，该IO完全独立 | Y |
| 8 | PC14 |  | RTC晶振 | N | 接32.768K晶振，不可用做IO | 外接RTC晶振用，不建议做普通IO用 | N |
| 9 | PC15 |  | RTC晶振 | N | 接32.768K晶振，不可用做IO | 外接RTC晶振用，不建议做普通IO用 | N |
| 114 | PD0 | FSMC_D2 |  | N | FSMC总线数据线D2(LCD/SRAM共用) | FSMC_D2，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 115 | PD1 | FSMC_D3 |  | N | FSMC总线数据线D3(LCD/SRAM共用) | FSMC_D3，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 116 | PD2 | SDIO_CMD |  | N | SD卡接口的CMD | 仅连接SD卡接口的CMD，有47K上拉电阻，当不使用SD卡时，可做普通IO使用 | Y |
| 117 | PD3 |  |  | Y |  |  | Y |
| 118 | PD4 | FSMC_NOE |  | N | FSMC总线NOE(RD)(LCD/SRAM共用) | FSMC_NOE，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 119 | PD5 | FSMC_NWE |  | N | FSMC总线NWE(WR)(LCD/SRAM共用) | FSMC_NWE，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 122 | PD6 | DCMI_SCL |  | Y | OLED/CAMERA接口的SCL脚 | 仅连接OLED/CAMERA接口的SCL，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 123 | PD7 | DCMI_SDA |  | Y | OLED/CAMERA接口的SDA脚 | 仅连接OLED/CAMERA接口的SDA，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 77 | PD8 | FSMC_D13 |  | N | FSMC总线数据线D13(LCD/SRAM共用) | FSMC_D13，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 78 | PD9 | FSMC_D14 |  | N | FSMC总线数据线D14(LCD/SRAM共用) | FSMC_D14，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 79 | PD10 | FSMC_D15 |  | N | FSMC总线数据线D15(LCD/SRAM共用) | FSMC_D15，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 80 | PD11 | FSMC_A16 |  | N | FSMC总线地址线A17(SRAM专用) | FSMC_A17，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 81 | PD12 | FSMC_A17 |  | N | FSMC总线地址线A18(SRAM专用) | FSMC_A18，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 82 | PD13 | FSMC_A18 |  | N | FSMC总线地址线A19(SRAM专用) | FSMC_A19，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 85 | PD14 | FSMC_D0 |  | N | FSMC总线数据线D0(LCD/SRAM共用) | FSMC_D0，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 86 | PD15 | FSMC_D1 |  | N | FSMC总线数据线D1(LCD/SRAM共用) | FSMC_D1，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 141 | PE0 | FSMC_NBL0 |  | N | FSMC总线NBL0(SRAM专用) | FSMC_NBL0，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 142 | PE1 | FSMC_NBL1 |  | N | FSMC总线NBL1(SRAM专用) | FSMC_NBL1，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 1 | PE2 |  |  | Y |  |  | Y |
| 2 | PE3 |  |  | Y |  |  | Y |
| 3 | PE4 | KEY0 |  | Y | 接按键KEY0 | 普通按键 | N |
| 4 | PE5 | DCMI_D6 |  | Y | OLED/CAMERA接口的D6脚 | 仅连接OLED/CAMERA接口的D6，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 5 | PE6 | DCMI_D7 |  | Y | OLED/CAMERA接口的D7脚 | 仅连接OLED/CAMERA接口的D7，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
| 58 | PE7 | FSMC_D4 |  | N | FSMC总线数据线D4(LCD/SRAM共用) | FSMC_D4，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 59 | PE8 | FSMC_D5 |  | N | FSMC总线数据线D5(LCD/SRAM共用) | FSMC_D5，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 60 | PE9 | FSMC_D6 |  | N | FSMC总线数据线D6(LCD/SRAM共用) | FSMC_D6，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 63 | PE10 | FSMC_D7 |  | N | FSMC总线数据线D7(LCD/SRAM共用) | FSMC_D7，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 64 | PE11 | FSMC_D8 |  | N | FSMC总线数据线D8(LCD/SRAM共用) | FSMC_D8，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 65 | PE12 | FSMC_D9 |  | N | FSMC总线数据线D9(LCD/SRAM共用) | FSMC_D9，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 66 | PE13 | FSMC_D10 |  | N | FSMC总线数据线D10(LCD/SRAM共用) | FSMC_D10，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 67 | PE14 | FSMC_D11 |  | N | FSMC总线数据线D11(LCD/SRAM共用) | FSMC_D11，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 68 | PE15 | FSMC_D12 |  | N | FSMC总线数据线D12(LCD/SRAM共用) | FSMC_D12，TFTLCD/SRAM等共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 10 | PF0 | FSMC_A0 |  | N | FSMC总线地址线A0(SRAM专用) | FSMC_A0，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 11 | PF1 | FSMC_A1 |  | N | FSMC总线地址线A1(SRAM专用) | FSMC_A1，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 12 | PF2 | FSMC_A2 |  | N | FSMC总线地址线A2(SRAM专用) | FSMC_A2，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 13 | PF3 | FSMC_A3 |  | N | FSMC总线地址线A3(SRAM专用) | FSMC_A3，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 14 | PF4 | FSMC_A4 |  | N | FSMC总线地址线A4(SRAM专用) | FSMC_A4，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 15 | PF5 | FSMC_A5 |  | N | FSMC总线地址线A5(SRAM专用) | FSMC_A5，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 18 | PF6 |  |  | Y |  |  | Y |
| 19 | PF7 |  |  | Y |  |  | Y |
| 20 | PF8 |  |  | Y |  |  | Y |
| 21 | PF9 | LED0 |  | N | 接DS0 LED灯(红色) | 该IO连接DS0，即红色LED灯。如做普通IO用，则DS0也受控制，建议：仅做输出用 | N |
| 22 | PF10 | LED1 |  | N | 接DS1 LED灯(绿色) | 该IO连接DS1，即绿色LED灯。如做普通IO用，则DS1也受控制，建议：仅做输出用 | N |
| 49 | PF11 | T_MOSI |  | Y | TFTLCD接口触摸屏MOSI信号 | 该IO接TFTLCD模块接口的触摸屏MOSI信号，当不插TFTLCD模块时，该IO完全独立 | Y |
| 50 | PF12 | FSMC_A6 |  | N | FSMC总线地址线A10(SRAM/LCD共用) | FSMC_A6，SRAM/TFTLCD共用，如禁止他们的片选，则可做普通IO使用 | Y |
| 53 | PF13 | FSMC_A7 |  | N | FSMC总线地址线A7(SRAM专用) | FSMC_A7，SRAM共用，如禁止SRAM的片选，则可做普通IO使用 | Y |
| 54 | PF14 | FSMC_A8 |  | N | FSMC总线地址线A8(SRAM专用) | FSMC_A8，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 55 | PF15 | FSMC_A9 |  | N | FSMC总线地址线A9(SRAM专用) | FSMC_A9，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 56 | PG0 | FSMC_A10 |  | N | FSMC总线地址线A10(SRAM专用) | FSMC_A10，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 57 | PG1 | FSMC_A11 |  | N | FSMC总线地址线A11(SRAM专用) | FSMC_A11，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 87 | PG2 | FSMC_A12 |  | N | FSMC总线地址线A12(SRAM专用) | FSMC_A12，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 88 | PG3 | FSMC_A13 |  | N | FSMC总线地址线A13(SRAM专用) | FSMC_A13，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 89 | PG4 | FSMC_A14 |  | N | FSMC总线地址线A14(SRAM专用) | FSMC_A14，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 90 | PG5 | FSMC_A15 |  | N | FSMC总线地址线A15(SRAM专用) | FSMC_A15，SRAM专用，如禁止SRAM的片选，则可做普通IO使用 | N |
| 91 | PG6 |  |  | Y |  |  | Y |
| 92 | PG7 |  |  | Y |  |  | Y |
| 93 | PG8 |  |  | Y |  |  | Y |
| 124 | PG9 | DCMI_PWDN |  | N | OLED/CAMERA接口的PWDN脚 | 连接OLED/CAMERA接口的PWDN脚，当不使用OLED/CAMEAR接口和单总线接口的时候，可以做普通IO使用 | Y |
| 125 | PG10 | FSMC_NE3 |  | N | FSMC总线的片选信号3，为外部SRAM片选信号 | FSMC_NE3，接SRAM的片选信号，不建议作为普通IO使用 | Y |
| 126 | PG11 |  |  | Y |  |  | Y |
| 127 | PG12 | FSMC_NE4 |  | Y | FSMC总线的片选信号4，为LCD片选信号 | FSMC_NE4，接TFTLCD接口的片选信号，当不使用TFTLCD接口时，该IO完全独立 | Y |
| 128 | PG13 |  |  | Y |  |  | Y |
| 129 | PG14 |  |  | Y |  |  | Y |
| 132 | PG15 | DCMI_RESET |  | Y | OLED/CAMERA接口的RESET脚 | 仅连接OLED/CAMERA接口的RESET，当不使用OLED/CAMERA接口时，该IO完全独立 | Y |
|    引脚编号：对应STM32F407ZGT6的引脚编号<br>   GPIO：STM32F407ZGT6的IO口<br>   完全独立：指该IO通过一定的方法，可以达到完全悬空的效果（即不接任何其他外设，且不接任何上拉/下拉电阻）<br>   连接关系说明：说明每个IO口与外设的连接关系<br>   使用提示：介绍每个IO的特点和使用方法，方便大家掌握开发板每一个IO口的使用<br>   是否引出：是否通过排针方式引出 |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |


## Sheet2

## Sheet3

