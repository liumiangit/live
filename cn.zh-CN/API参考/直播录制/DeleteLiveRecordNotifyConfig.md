# DeleteLiveRecordNotifyConfig {#reference926 .reference}

删除域名级别录制回调配置。

## 请求参数 {#section_k4f_qm1_dfb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|Action|String|是|DeleteLiveRecordNotifyConfig|系统规定参数。取值：DeleteLiveRecordNotifyConfig|
|DomainName|String|是|www.yourdomain.com|您的加速域名。|

## 返回参数 {#section_p4f_qm1_dfb .section}

|名称|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|16A96B9A-F203-4EC5-8E43-CB92E68F4CD8|该条任务请求 ID。|

## 示例 {#section_zcx_4j1_dfb .section}

请求示例

```
https://live.aliyuncs.com/?Action=DeleteLiveRecordNotifyConfig&DomainName=test101.cdnpe.com<公共请求参数> 
```

**说明：** 关于公共请求参数详细内容，参见 [公共请求参数](cn.zh-CN/API参考/调用方式/公共参数.md#)。

正常返回示例

JSON格式

```
{
    "RequestId":"16A96B9A-F203-4EC5-8E43-CB92E68F4CD8"
}
```

异常返回示例

JSON格式

```
{
    "Code":"InternalError",
    "HostId":"live.aliyuncs.com",
    "Message":"The request processing has failed due to some unknown error.",
    "RequestId":"6EBD1AC4-C34D-4AE1-963E-B688A228BE31"
}
```

## 错误码 {#section_h3y_jkc_dfb .section}

 [查看本产品错误码](https://error-center.aliyun.com/status/product/live) 

