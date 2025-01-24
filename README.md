# devSupportCompare
json数据提取并比较

远端：目前正在使用的云端的support配置文件，dev_support.json

本地：Android和iOS各57个设备型号，每个型号对应各自的json文件即support文件

Android的目录为：devices/{model}/res/raw/device_local_support_model.json

iOS对应的目录为：iOS_Devices/{model}/device_support.json


# 原有的 remote support key，雷达、配网WiFi频段、存储卡信息、供电模式、视频清晰度、压缩格式二维码、太阳能板、低功耗设备、夜视、卡录播放速度
# Android不包含video共9项，iOS包含video共10项，每项固定，是远端的优化点
remoteSupportKeyOfAndroid = ['radar', 'wifi', 'storage', 'power', 'compressedQrCode', 'equipSolarPanel', 'lowpowerdevice', 'nightVision', 'cardRecordSpeed']
remoteSupportKeyOfiOS = ['radar', 'wifi', 'storage', 'power', 'video', 'compressedQrCode', 'equipSolarPanel', 'lowpowerdevice', 'nightVision', 'cardRecordSpeed']


# 下沉后的 local support key，Android一共9项（不包含video），iOS一共10项（包含video），每项固定，为此次优化点
localSupportKeyOfAndroid = ['spRadar', 'spWifiBand', 'spStorage', 'spPower', 'spCompressedQrCode', 'spEquipSolarPanel', 'spLowPowerDevice', 'spNightVision', 'spCardRecordSpeed']
localSupportKeyOfiOS = ['spRadar', 'spWifi', 'spStorage', 'spPower', 'spVideo', 'spCompressedQrCode', 'spEquipSolarPanel', 'spLowPowerDevice', 'spNightVision', 'spCardRecordSpeed']


通过方法openLocalSupportFile获取本地的support项，放入excel中

通过方法getRemoteData获取远端的support项，放入excel中

通过方法compareOfRemoteAndLocal比较远端和本地的support项，把结果放入最后一列


结果文件展示如下：

![image](https://github.com/user-attachments/assets/dd45590c-b8d3-48af-bcc5-f904630f56af)















![image](https://github.com/user-attachments/assets/d8974347-ae13-42c7-95ac-e4427026bc01)
