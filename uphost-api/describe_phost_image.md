# 获取物理机镜像 - DescribePHostImage

## 简介

获取物理云主机镜像列表





## 使用方法

您可以选择以下方式中的任意一种，发起 API 请求：
- 多语言 OpenSDK（[Python](https://github.com/ucloud/ucloud-sdk-python3) / [Go](https://github.com/ucloud/ucloud-sdk-go) / [Java](https://github.com/ucloud/ucloud-sdk-java)）
- [UAPI 浏览器](https://console.ucloud.cn/uapi/detail?id=DescribePHostImage)
- [工作流引擎 StepFlow](https://console.ucloud.cn/stepflow/manage/)

## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `DescribePHostImage`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Region** | string | 地域。 参见 [地域和可用区列表](api/summary/regionlist) |**Yes**|
| **Zone** | string | 可用区。参见 [可用区列表](api/summary/regionlist) |**Yes**|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](api/summary/get_project_list) |No|
| **ImageType** | string | 镜像类别，枚举为：Base,标准镜像；默认为标准镜像。 |No|
| **ImageId.N** | string | 镜像ID |No|
| **Offset** | int | 数据偏移量，默认为0 |No|
| **Limit** | int | 返回数据长度，默认为20 |No|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **TotalCount** | int | 满足条件的镜像总数 |No|
| **ImageSet** | array[[*PHostImageSet*](#PHostImageSet)] | 镜像列表 PHostImageSet |No|

#### 数据模型


#### PHostImageSet

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **ImageId** | string | 镜像ID |No|
| **ImageName** | string | 镜像名称 |No|
| **OsName** | string | 操作系统名称 |No|
| **OsType** | string | 操作系统类型 |No|

## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=DescribePHostImage
&ProjectId=org1
&Region=cn-bj2
&Zone=cn-bj2-04
```

### 响应示例
    
```json
{
  "Action": "DescribePHostImageResponse",
  "Images": [
    {
      "ImageId": "pimg-yg-f2634b",
      "ImageName": " Ubuntu 12.04 64位",
      "OsName": "Ubuntu 12.04 64位",
      "OsType": "Ubuntu"
    }
  ],
  "RetCode": 0
}
```




