# ActorCloud

## 介绍


**ActorCloud**是一个物联网平台，可为具有低功耗物联网网络的企业提供一站式平台服务。它在安全可靠的基础上为设备提供多种协议访问，消息流管理，数据解析和数据处理功能。

该平台提供基本的设备管理功能，以连接和管理大型设备，实现设备的消息通信和数据收集持久性，集成规则引擎和数据可视化管理，灵活地开放多个特权级管理和控制API，通过API快速开发上层以及实现多端访问和设备远程控制。

- 多协议访问：支持低功耗标准协议，例如MQTT，CoAP，LoRaWAN和Websocket，并适应低功耗场景中的主流Wi-Fi模块，NB-IoT模块，LoRa网关和各种工业网关；
- 设备管理：终端注册开放和生命周期管理，提供状态，故障和报告数据的连续监控；
- 数据解析：无需更改设备的数据报告格式，并支持编写解码插件在云中解析；
- 规则引擎：基于Pulsar，内置灵活的SQL表达式和丰富的处理功能，实现终端消息的实时解析，高速持久性，规则处理和不同类型的动作触发；
- 应用程序支持：开放的丰富REST API接口，具有灵活和可配置的应用程序权限，可帮助企业快速构建各种上层应用程序；
- 租户管理：支持多租户，并且租户之间的数据完全隔离。可以为租户中的用户配置不同的权限和管理域。

## 在线演示和安装
- 访问[https://demo.actorcloud.io](https://demo.actorcloud.io/)以在线试用** ActorCloud **的全部功能。
- 访问[Actorcloud部署文档](https://docs.actorcloud.io/en/installation/base.html)以在本地部署ActorCloud以供使用。

## 文档

See the [Quick Start](https://docs.actorcloud.io/en/getting_started/quick_start.html) 使用文档

## Device Access

### Device Quick Access Guide
For the steps of Accessing Devices to ActorCloud, please see the [Device quick access guide](<https://docs.actorcloud.io/en/getting_started/access_guide.html>).

### Device Access Method

Although the device messages in any access mode under the same account are interoperable, the appropriate access method needs to be selected according to the product requirements.

The use of SSL/TLS generally results in higher security while reducing connection performance. Some devices are limited in performance and can only run lightweight CoAP clients, while WebSocket is recommended for real-time communication on the browser.

##### Attached:  Access protocol supported by ActorCloud

| Name                             | Access address                 | Description                              |
| -------------------------------- | ------------------------------ | ---------------------------------------- |
| MQTT                             | broker.actorcloud.io:1883      | Normal MQTT access                       |
| MQTT/SSL                         | broker.actorcloud.io:8883      | SSL MQTT Access (one-way authentication) |
| MQTT/SSL                         | broker.actorcloud.io:8884      | SSL MQTT Access (two-way authentication) |
| CoAP(LwM2M)                      | broker.actorcloud.io:5683/mqtt | CoAP/LwM2M Access                        |
| CoAP(LwM2M)/DTLS                 | broker.actorcloud.io:5684/mqtt | DTLS CoAP/LwM2M Access                   |
| MQTT/WebSocket                   | broker.actorcloud.io:8083/mqtt | WebSocket Access                         |
| MQTT/WebSocket/SSL               | broker.actorcloud.io:8084/mqtt | SSL WebSocket Access                     |
| Private TCP transparent protocol | custom made                    | Private TCP transparent protocol         |



## License

ActorCloud is released under [Apache 2.0 License](https://github.com/actorcloud/ActorCloud/blob/master/LICENSE).
