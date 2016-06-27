# 设备开发指导-MTK

DotlinkCloud不提供联网固件，提供了MTK的设备SDK。 硬件厂商可以集成SDK到联网固件（WIFI, GPRS）模块中，实现和云端连接。

* 云端控制台提供了数据点的定义，可以定义硬件的功能。
* 联网固件和云端按照数据点协议进行加密通信，而MCU通过串口和联网固件进行通信。
* 厂商只需要在MCU上开发自己的设备控制逻辑，不用开发相关的联网控制逻辑，所有的联网控制逻辑都由设备SDK来实现。
* 厂商只要按照协议要求，进行通信控制即可。


## 系统架构
![Markdown](system.png)

## 集成到MTK环境
### 1. 在Option.Mak添加
```
ifdef USE_MQTT_TASK_SERVER
```

### 2. 在App_task_config.h添加

```
#ifdef __USE_MQTT_TASK_SERVER__

```

```
#ifdef __USE_MQTT_TASK_SERVER__
```

### 3. 放置mqtttask目录到plutommi目录下
  * mqtttask.c是task的入口

## 云端通信

### 1.设备接收
```

```

### 2.设备上报

```
void publish_msg(){
```