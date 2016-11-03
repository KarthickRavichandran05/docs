---

copyright:
  years: 2015, 2016

---

{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 外部服务集成
{: #ref-index}
上次更新时间：2016 年 9 月 13 日
{: .last-updated}

通过外部服务集成，可在 {{site.date.keyword.iot_full}} 组织中访问第三方或外部服务中的数据和操作。

## Jasper
{: #jasper}

Jasper 是一款用于 SIM 设备的管理平台。Jasper 集成到 {{site.data.keyword.iot_short_notm}} 仪表板中，从而可通过 {{site.data.keyword.iot_short_notm}} 组织仪表板管理 Jasper 设备。

### Jasper 的受支持操作

我们的平台所提供的内置 Jasper 集成提供了对以下 Jasper 操作的支持：

- 查看总体 Jasper 数据
  - 显示：状态、套餐、本月至今数据使用情况、本月至今 SMS 使用情况、本月至今语音使用情况、超额限制、添加日期和修改日期。
- 更改 SIM 激活状态。
  - 选择：库存、可随时激活、已激活、已取消激活和已废弃。
- 查看 SIM 使用情况
  - 显示：周期开始日期、计费数据和数据总量、计费 SMS 和 SMS 总量、计费语音和语音总量。
  - 可以使用 YYYY-MM-DD 格式设置周期开始日期。
- 将 SMS 发送到 SIM
- 更改套餐

完成以下配置步骤后，可在连接了 Jasper 的设备的设备向下钻取中访问受支持的操作。


### Jasper 的配置

要将 Jasper 服务连接到 {{site.data.keyword.iot_short_notm}} 组织，必须首先完成两个配置阶段。首先，必须将 {{site.data.keyword.iot_short_notm}} 连接到 Jasper 服务，然后必须配置 {{site.data.keyword.iot_short_notm}} 设备。


1. 启用 Jasper 扩展。要启用 Jasper 与 {{site.data.keyword.iot_short_notm}} 组织的集成，请完成以下步骤：
  1. 从 {{site.data.keyword.iot_short_notm}} 仪表板选择**扩展**。
  2. 在**扩展**页面上，单击**添加扩展**。
  3. 单击 AT&T 旁的**添加**。
  4. 输入 AT&T 用户名、密码、访问键和域标识。
  5. 单击**完成**。

2. 配置设备
您可以配置同时连接到您的 {{site.data.keyword.iot_short_notm}} 组织和 Jasper 帐户的设备以在 {{site.data.keyword.iot_short_notm}} 仪表板中显示 Jasper 中的数据。
**重要信息：**在执行“添加设备”过程时，无法应用 Jasper 配置，只有先前连接的设备可使用 Jasper 进行配置。
要配置连接了 Jasper 的设备，请完成以下步骤：
 1. 在 {{site.data.keyword.iot_short_notm}} 仪表板的“设备”选项卡中，找到要配置的连接了 Jasper 的设备。
 2. 选择此设备以打开*设备向下钻取*视图。
 3. 向下滚动到*扩展配置*。
 4. 通过使用以下 JSON 格式输入扩展配置，然后单击**确认更改**以保存配置。  

```json  
    {
        "jasper": {
            "iccid": "string"
        }
    }

```

成功配置组织后，会在*设备向下钻取*视图中*扩展配置*部分下显示*扩展*部分。

## AT&T
{: #att}

### AT&T 的受支持操作

AT&T 扩展支持以下 AT&T 操作：

- 查看总体 AT&T 数据
  - 显示：状态、套餐、本月至今数据使用情况、本月至今 SMS 使用情况、本月至今语音使用情况、超额限制、添加日期和修改日期。
- 更改 SIM 激活状态。
  - 选择：库存、可随时激活、已激活、已取消激活和已废弃。
- 查看 SIM 使用情况
  - 显示：周期开始日期、计费数据和数据总量、计费 SMS 和 SMS 总量、计费语音和语音总量。
  - 可以使用 YYYY-MM-DD 格式设置周期开始日期。
- 将 SMS 发送到 SIM
- 更改套餐

### AT&T 的配置

要将 {{site.data.keyword.iot_short_notm}} 组织连接到 AT&T，必须完成组织配置和设备配置。

要配置 {{site.data.keyword.iot_short_notm}} 平台，请完成以下步骤。

1. 启用 AT&T 扩展。要启用 AT&T 与 {{site.data.keyword.iot_short_notm}} 组织的集成，请完成以下步骤：
  1. 从 {{site.data.keyword.iot_short_notm}} 仪表板选择**扩展**。
  2. 在**扩展**页面上，单击**添加扩展**。
  3. 单击 AT&T 旁的**添加**。
  4. 输入 AT&T 用户名、密码、访问键和域标识。
  5. 单击**完成**。

要将您的 {{site.data.keyword.iot_short_notm}} 组织与 AT&T 帐户相连接，首先必须完成两个配置阶段。完成组织配置，然后配置设备。


2. 配置设备
您可以配置同时连接到您的 {{site.data.keyword.iot_short_notm}} 组织和 AT&T 帐户的设备以在 {{site.data.keyword.iot_short_notm}} 仪表板中显示 AT&T 中的数据。
**重要信息：**在执行“添加设备”过程时，无法应用 AT&T 配置，只有先前连接的设备可使用 AT&T 进行配置。
要配置连接了 AT&T 的设备，请完成以下步骤：
 1. 在 {{site.data.keyword.iot_short_notm}} 仪表板的“设备”选项卡中，找到要配置的连接了 AT&T 的设备。
 2. 选择此设备以打开*设备向下钻取*视图。
 3. 向下滚动到*扩展配置*。
 4. 通过使用以下 JSON 格式输入扩展配置，然后单击**确认更改**以保存配置。  

```json  
    {
        "atnt": {
            "iccid": "string"
        }
    }

```

成功配置组织后，会在*设备向下钻取*视图中*扩展配置*部分下显示*扩展*部分。

<!--
## ARM mbed connector
{: #arm}

The ARM mbed connector is an extension that allows you to connect your ARM mbed device to your {{site.data.keyword.iot_short_notm}}. The ARM mbed extension is allows the ARM mbed portal and the {{site.data.keyword.iot_short_notm}} to send and receive data from the ARM mbed portal.

### Setup Configuration


1. Enable the ARM mbed connector extension. To enable the ARM mbed connector extension complete the following steps:
  1. From the {{site.data.keyword.iot_short_notm}} dashboard, select **Settings** and navigate to **Extensions**.
  2. In the **Extensions** menu, click **Add Extension**.
  3. Click **Add** next to ARM mbed connector extension.
  4. Enter your ARM mbed access key and domain ID. You can find these by using the ARM mbed portal at https://connector.mbed.com.
  5. Check the credentials are correct by clicking the **Check Connection** button.
  6. Click **Done**.

### Payload Format

There are two types of incoming messages from the ARM mbed platform, notifications and asynchronous responses. The {{site.data.keyword.iot_short_notm}} can send commands to devices that are connected to the ARM mbed platform.

#### Notifications

Notifications are generated by changes in device or sensor data. After the {{site.data.keyword.iot_short_notm}} processes the message, it is to the device event topic in the same way as a device connected directly to the {{site.data.keyword.iot_short_notm}}. The event type used for notifications originating on devices connected to the ARM mbed platform is `notify`.

The following code sample shows the payload format for a notification sent by the ARM mbed platform API:

```
{
  "ep":<endpoint/deviceID>,
  "path":<resource path>,
  "ct":<content type>,
  "payload":<Base64 encoded payload>,
  "max-age":<how long the payload is valid, in seconds>
}
```

#### Asynchronous responses

When the {{site.data.keyword.iot_short_notm}} sends a command to a device connected to the ARM mbed platform, the device sends a confirmation message back to the {{site.data.keyword.iot_short_notm}}. This confirmation message is called an _asynchronous response_ and uses the event type `asyncResponse`.

The following code sample shows the payload format for an asynchronous response sent by the ARM mbed cloud service:

```
{
  "id":<transaction id>,
  "status":<200 is command was sucessfully executed. Check other HTTP response codes>,
  "ct":<content type>,
  "max-age":<how long the payload is valid, in seconds>,
  "payload":<base64 encoded payload>,
  "ep":<endpoint/deviceID affected by the command>,
  "path":<resource path affected by the command>
}
```

#### Sending commands to the ARM mbed platform

The {{site.data.keyword.iot_short_notm}} can send commands to devices connected to the ARM mbed platform. Commands sent to the ARM mbed platform it must use the following JSON format.

```
{
  "method":<PUT or POST>,
  "deviceId":<endpoint/deviceId>,
  "resourceId":<resource path>,
  "payload": <Base64 encoded payload>
}
```

The payload should be published to the following topic:

```
iot-2/type/<device_type>/id/<deviceId>/cmd/<command_type>/fmt/<command_format>
```
-->

## Orange
{: #orange}

通过 Orange 扩展，可从连接到 {{site.data.keyword.iot_short_notm}} 且安装了 Orange SIM 卡的设备查看 SIM 卡数据。

https://developer.ibm.com/iotplatform/2016/03/30/watson-iot-platform-integration-with-orange-beta/

### Orange 的受支持操作

如果您的设备连接到 {{site.data.keyword.iot_short_notm}} 服务且具有 Orange SIM 卡，那么可使用 Orange 扩展来查看以下 SIM 卡数据：

- SIM 序列号
- 激活状态
- 上次状态更改
- 上次状态刷新
- 位置状态

### Orange 的配置



要启用 Orange 扩展，请执行以下操作：

1. 从 {{site.data.keyword.iot_short_notm}} 仪表板选择**扩展**。
2. 在**扩展**页面上，单击**添加扩展**。
3. 单击 Orange 扩展旁的**添加**。
4. 输入 Orange 用户名和密码。
6. 单击**完成**。

启用 Orange 扩展后，必须配置具有 Orange SIM 卡的每个设备以显示 Orange SIM 数据。

1. 在 {{site.data.keyword.iot_short_notm}} 仪表板的“设备”选项卡中，找到要配置的 Orange SIM 设备。
2. 选择此设备并向下滚动到*扩展配置*。
3. 通过使用以下 JSON 格式输入扩展配置，然后单击**确认更改**以保存配置。

```  
    {
        "orange": {
            "serialnumber": "<serial number of Orange SIM>"
        }
    }

```
成功配置组织后，会在*设备向下钻取*视图中*扩展配置*部分下显示*扩展*部分。


## 设备管理扩展
{: #device_mgmt}

设备管理是 {{site.data.keyword.iot_short_notm}} 的核心功能，但是，也可以对其进行扩展以开发其他功能。

通过设备管理扩展，可安装用于设备管理的定制功能。有关定制设备管理功能的更多信息，请参阅[设备管理定制扩展](../../devices/device_mgmt/custom_actions.html){: new_window}。

## Blockchain
{: #blockchain}

通过具有 Blockchain 的 {{site.data.keyword.iot_short_notm}}，IoT 设备可为 Blockchain 事务提供数据，这会将数据存储在 Blockchain 的不可变分类帐中，并在智能合同业务规则中使用这些数据。{{site.data.keyword.iot_short_notm}} 将设备数据映射为 Blockchain 的智能合同所需的数据格式，并将其传递到 Blockchain 光纤网以存储在 Blockchain 分类帐中。

### Blockchain 的受支持操作
- 通过设备事件触发智能合同更新。
- 运行智能合同业务逻辑以使用设备事件数据更新分类帐状态。
- 使用监视 UI 来监视 Blockchain、事务和分类帐状态。

### Blockchain 的配置

{{site.data.keyword.iot_short_notm}} Blockchain 集成是一款服务产品，缺省情况下在 {{site.data.keyword.iot_short_notm}} 中未激活。要在您的环境中激活此功能，请完成以下步骤：
 1. 从 {{site.data.keyword.iot_short_notm}} 仪表板，选择**设置**并浏览到**扩展**。
 2. 单击 Blockchain 扩展旁的**更多信息**链接，以转至“IoT Blockchain 服务产品”页面。
 3. 填写并提交服务请求表单。
通常，服务核准需要花费大约一天时间。核准请求后，您会收到一封电子邮件，其中提供了有关如何在 {{site.data.keyword.iot_short_notm}} 组织中激活 Blockchain 集成的指示信息。
 5. 返回到组织的 {{site.data.keyword.iot_short_notm}} 仪表板以完成此设置。有关更多信息，请参阅 [{{site.data.keyword.iot_short_notm}} Blockchain 集成](../../bl_blockchain_integration.html)。