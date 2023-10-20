# esp8266-ir-tv-homekit


## 原生HomeKit红外电视遥控

![HomeKit](https://github.com/hassbian-ABC/esp8266-ir-tv-homekit/blob/main/image/homekit-tv.png)

主芯片为ESP8266，原生HomeKit红外电视遥控，支持市面上大多数遥控协议。



## 主要功能

- 原生HomeKit协议，无需服务器桥接，基于Mixiaoxiao的[Arduino-HomeKit-ESP8266](https://github.com/Mixiaoxiao/Arduino-HomeKit-ESP8266), 更新适配家庭新框架，适配iOS17
- 支持控制电视的开关、输入源、音量、方向、菜单、设置等等
- 支持市面上大多数遥控协议，红外控制基于[IRremoteESP8266](https://github.com/crankyoldgit/IRremoteESP8266)，更新最新版本
- 本固件支持多种esp8266红外控制器，例如：中国移动x12 全橙空调伴侣 涂鸦万能遥控器 自制esp8266红外控制器 等等，其中 中国移动x12 和 全橙空调伴侣 支持电量统计，并支持功率反馈电视真实开关情况，确保万无一失
- 支持mqtt，预留接收和发射红外码的主题，方便使用第三方平台（homeassistant homebridge node-red）控制
## 电视反馈
- 支持功率或者ping ip，两者二选一
- 红外接收红外码作为第一反馈，功率/ping作为补充反馈

## WiFi配网

- ESP8266在未联网时会生成热点，手机连接该热点会自动弹出配网页面，如果未自动弹出可手动访问192.168.4.1
- 扫描WiFi，填写WiFi名称和密码点击发送配置，连接成功后会自动退出配网模式并关闭AP热点

## Web功能

空调红外(IR)设置与控制，访问`http://<esp_ip>`，Web APP型页面，效果见下图

注：`<esp_ip>`为你的ESP8266联网后的IP地址，下同

![web.png](https://github.com/hassbian-ABC/esp8266-ir-tv-homekit/blob/main/image/web.png)

- 学习红外码:使用之前需要学习每一个按键的红外码，学习后会自动保存
- 删除红外码:如果某个按键学习到错误的红外码可以删除后重新学习


## HomeKit家庭添加配件

- 配对设置代码：根据MAC地址计算，同时作为Homekit功能和mqtt功能的激活码
- 获取激活码请加qq群：874918228， 注明github
- 注意，激活码付费，群友价15元/个


![qq.png](https://github.com/hassbian-ABC/esp8266-ir-tv-homekit/blob/main/image/qq.png)
