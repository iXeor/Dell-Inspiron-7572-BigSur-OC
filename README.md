# 适用于Dell Inspiron 7572笔记本安装与运行macOS Big Sur的OpenCore EFI配置
  * 更新：2021年2月15日
  * 更新内容：
  * OpenCore 0.6.5 =====> OpenCore 0.6.6
  * 部分驱动更新
# 注意：该EFI文件只适用于Big Sur版本。
# 本EFI配置思路基于[@ic005k](https://github.com/ic005k)的[Dell Inspiron 7472 OC配置文件](https://github.com/ic005k/DELL7472)
* 如需运行Catalina版本，请使用 [@Lyn](https://github.com/lyngogogog)的 [EFI](https://github.com/lyngogogog/Dell-7472-7572-Hackintosh-EFI)配置文件。
* 如若安装更低版本的macOS，可以使用[@黑果小兵](https://github.com/daliansky)的[CLOVER配置文件](https://github.com/daliansky/Dell-Inspiron-7560-Hackintosh)
# >>>[点击此处下载EFI配置文件(Github)](https://github.com/iXeor/Dell-Inspiron-7572-BigSur-OC/releases/download/Ins7572-BigSur-OC-6.5/Ins7572-OC-6.5-BigSur.zip)<<<
# >>>[点击此处下载EFI配置文件(Gitee)](https://gitee.com/Shirakage/Dell-Inspiron-7572-BigSur-OC/attach_files/577203/download/EFI.zip)<<<
## 电脑配置

| 规格     | 详细信息                                                     |
| -------- | ------------------------------------------------------------ |
| 电脑型号 | 戴尔 Inspiron 7572 笔记本电脑                                |
| BIOS版本 | Inspiron_7472_7572_1.6.1                               |
| 操作系统 | macOS Big Sur 11.2.1/Windows 10 专业工作站版Insider Preview Build 21301.1010/Ubuntu 20.10       |
| 处理器   | Intel Core i5-8250U @ 1.80GHz 四核八线程                          |
| 内存     | 16 GB ( 科赋 DDR4 2400MHz )                                |
| 硬盘1     | 三星 970 EVO (250 GB / 固态硬盘 )                          |
| 硬盘2     | HGST HTS541010B7E610 (1 TB / 机械硬盘 )                          |
| 显卡1     | 英特尔 HD Graphics 620 （保留2 GB显存）             |
| 显卡2     | NVIDIA MX 150 4G（未使用）              |
| 显示器   | BOE(京东方) NV156FHM-H61 FHD 1920x1080 (15.6 英寸)                       |
| 声卡     | ALC256 (layout-id:2/56)                                      |
| 网卡     | Intel Wi-Fi 6 AX200 160MHz                      |
| OpenCore版本     | OpenCore-0.6.6-RELEASE                      |

## 特性

* 集成[OpenIntelWireless](https://github.com/OpenIntelWireless)的[itlwm](https://github.com/OpenIntelWireless/itlwm)、[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)和[AirportItlwm](https://github.com/OpenIntelWireless/itlwm/tree/master/AirportItlwm)，可以使用一部分Intel品牌的无线网卡
* 支持将macOS Big Sur安装到机械硬盘

## 目前已知问题与解决方法：

* 如OC 0.6.6不能进行安装，请先使用OC 0.6.5安装，待安装安装完成后替换OC 0.6.6
* 耳机插口失效问题：安装[ComboJack](https://github.com/hackintosh-stuff/ComboJack)以解决
* SD卡卡槽暂时不能读取SD卡（待解决）
* 如出现实装EFI后不能正常关机、时间错误的情况，可以通过安装Linux解决
* 在安装第二、三阶段出现偶发性花屏属正常现象，待其自动重启即可
* 使用本EFI配置不能启动低版本的macOS（会出现禁止符号），暂无解决办法
* CPU原生支持，变频正常
* 显示器亮度调节正常；
* 使用博通（Boardcom）品牌的网卡的大佬麻烦禁用'itlwm.kext'和'AirportItlwm.kext',并在'boot-args'中添加'brcmfx-country=#a brcmfx-driver=2'
