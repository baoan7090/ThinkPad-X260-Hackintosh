# ThinkPad-X260-Hackintosh

这是两份用于 __ThinkPad X260__ 型号的黑苹果的EFI (Clover+OpenCore)

非常感谢[黑果小兵](https://github.com/daliansky)的[X260EFI](https://github.com/daliansky/ThinkPad-X260-hackintosh) 以及黑苹果社区所有人员

**电脑详细配置**：(直接修改[黑果小兵](https://github.com/daliansky)的[X260EFI](https://github.com/daliansky/ThinkPad-X260-hackintosh)中的描述)

|规格|详细信息|
|---|---|
|电脑型号|联想ThinkPad X260 笔记本电脑|
|操作系统|macOS Big Sur 11.0.1 20B29 / 20B50 /macOS Big Sur 11.2 20D64|
|处理器|Intel(R) Core(TM) i5-6300U CPU @ 2.40GHz|
|内存|8 GB 2133MHz|
|硬盘|KINGSTON SA400S37480G|
|显卡|Intel(R) HD Graphics 520 (platform-id:0x19160000) (黑果小兵原EFI为0x19160002，已更改)|
|显示器|1366x768 (12.5英寸)|
|声卡|ALC293 (OC layout-id:28 / Clover 注入:No)|
|网卡|Intel(R) Dual Band Wireless-AC 8260|

**EFI** : 由于没有技术， __未知__ 制作后会出现什么问题，因此在使用过程中出现任何问题将不负责任

Clover : 使用了[黑果小兵](https://github.com/daliansky)的[X260EFI](https://github.com/daliansky/ThinkPad-X260-hackintosh)进行修改

OpenCore : ~~裁缝的~~  整合了众多大佬的SSDT/补丁(感谢[OC-little](https://github.com/daliansky/oc-little)项目) 驱动 等等 

**电池信息** : Clover 及 OpenCore 的电池信息均可使用

OpenCore中补丁使用的[SSDT-BATX](https://github.com/simprecicchiani/ThinkPad-T460s-macOS-OpenCore/blob/master/EFI/OC/ACPI/SSDT-BATX.aml)

对于Clover，如果你的设备有双电池，可能需要耗尽第一块电池后才会显示第二块电池信息(不确定，自行测试)

对于OpenCore，电池信息将返回平均值(不准确) [没有技术，不会修改SSDT以实现更准确的电池信息]

**苹果服务** : iMessage、iCloud、App Store等均正常使用 (**谨记注入三码(SMBIOS)！！！** **_此EFI已清空三码(SMBIOS)_** )

**休眠** : Clover貌似比OpenCore快一点，未经过精准测试。

SSDT-Lamp.aml用于唤醒后电源LED仍然慢闪问题(国外论坛复制粘贴)(**_不保证使用后万无一失！！！非专业人员制作的！！_**)

**其他** : 

Fn+F5/F6调亮度可能不可用，根据以往做法是接一个外置键盘后，在设置里将亮度快捷键设置为Fn+F5/F6即可(不知道现在还能否使用)

有些SSDT引用的路径是LPCB，不确定LPC使用后会出现什么问题，已将部分SSDT的LPCB更改为LPC(对应DSDT表中路径)

注意，Clover版本为5151，但貌似在安装Big Sur(11.0.1)(11.2未经测试)过程中会出现 __读不到__ macOS安装分区的情况，请尝试自行降到5126后(谨记**替换Drivers！！**)再进行安装

OpenCore由于是在安装后的环境下进行配置， __未知__ 安装过程中会出现什么问题，请自行尝试

两份EFI的无线网卡驱动版本均为AirportItlwm_v2.1.0_stable_BigSur.kext；其他版本请自行替换

**总结** : ~~全都是裁缝。~~  能进系统就行

![Clover](/Clover.png "Clover")	
![OpenCore](/OpenCore.png "OpenCore")	

__感谢所有为黑苹果社区做出贡献的人__

-----------------------------------------------------------

**English** : Google translate yourself.
