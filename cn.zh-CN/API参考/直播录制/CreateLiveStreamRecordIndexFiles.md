# CreateLiveStreamRecordIndexFiles {#reference3513 .reference}

创建录制索引文件。

**说明：** 创建录制索引必保证直播流发生过推流行为，如果设置的时间内未发生过直播或流名错误等会导致创建录制索引失败。

## 请求参数 {#section_k4f_qm1_dfb .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|Action|String|是|CreateLiveStreamRecordIndexFiles|系统规定参数。取值：CreateLiveStreamRecordIndexFiles|
|AppName|String|是|testApp|直播流所属应用名称。|
|DomainName|String|是|www.yourdomain.com|您的加速域名。|
|EndTime|String|是|2017-12-22T08:00:00Z| 结束时间。

 -   格式：UTC时间。
-   示例：2015-12-01T17:36:00Z。
-   与 StartTime 间隔时间不能超过 4 天。

 |
|OssBucket|String|是|test123|OSS 存储 bucket 名称。|
|OssEndpoint|String|是|oss-cn-shanghai.aliyuncs.com|OSS endpoint。|
|OssObject|String|是|\{AppName\}/\{StreamName\}/\{Date\}/\{Hour\}/\{Minute\}\_\{Second\}.m3u8|OSS 存储的录制文件名。|
|StartTime|String|是|2017-12-21T08:00:00Z| 开始时间。

 格式：UTC时间。

 示例：2015-12-01T17:36:00Z。

 |
|StreamName|String|是|testStream|直播流名称|

## 返回参数 {#section_p4f_qm1_dfb .section}

|名称|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|550439A3-F8EC-4CA2-BB62-B9DB43EEEF30|请求ID。|
|RecordInfo| | |录制配置。|
|  └RecordUrl|String|[http://xxx.xxx/atestObject.m3u8](http://xxx.xxx/atestObject.m3u8)|索引文件地址。|
|  └DomainName|String|test.com|流所属加速域名。|
|  └AppName|String|test123|流所属应用名称。|
|  └StreamName|String|test123|直播流名称。|
|  └StartTime|String|2015-12-01T17:36:00Z| 开始时间。

 格式：2015-12-01T17:36:00Z。

 |
|  └EndTime|String|2015-12-01T17:36:00Z| 结束时间。

 格式：2015-12-01T17:36:00Z。

 |
|  └Duration|Float|20|录制时长。单位：秒。|
|  └Height|Integer|480|视频高。|
|  └Width|Integer|640|视频宽。|
|  └CreateTime|String|2016-05-27T09:40:56Z|创建时间。|
|  └RecordId|String|c4d7f0a4-b506-43f9-8de3-07732c3f3d82|索引文件 ID。|
|  └OssBucket|String|bucket|OSSBucket名称。|
|  └OssEndpoint|String|oss-cn-hangzhou.aliyuncs.com|OSSEndpoint域名。|
|  └OssObject|String|atestObject.m3u8|OSSObject名称。|

## 示例 {#section_zcx_4j1_dfb .section}

请求示例

```
 https://live.aliyuncs.com/?Action=CreateLiveStreamRecordIndexFiles&DomainName=xxxxx&AppName=aliyuntest&StreamName=xxx&OssEndpoint=oss-cn-hangzhou.aliyuncs.com&OssBucket=xxx&OssObject=atestObject.m3u8&StartTime=xxx&EndTime=xxx&<公共请求参数>
```

**说明：** 关于公共请求参数详细内容，参见 [公共请求参数](intl.zh-CN/API参考/调用方式/公共参数.md#)。

正常返回示例

JSON格式

```
{
    "RecordInfo":{
        "AppName":"xxx",
        "CreateTime":"2016-05-27T09:40:56Z",
        "DomainName":"xxx",
        "Duration":588.849,
        "EndTime":"2016-05-25T05:47:11Z",
        "Height":480,
        "OssBucket":"bucket",
        "OssEndpoint":"oss-cn-hangzhou.aliyuncs.com",
        "OssObject":"atestObject.m3u8",
        "RecordId":"c4d7f0a4-b506-43f9-8de3-07732c3f3d82",
        "RecordUrl":"http://xxx.xxx/atestObject.m3u8",
        "StartTime":"2016-05-25T05:37:11Z",
        "StreamName":"xxx",
        "Width":640
    },
    "RequestId":"550439A3-F8EC-4CA2-BB62-B9DB43EEEF30"
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

## 错误码 {#section_htt_hgc_dfb .section}

 [查看本产品错误码](https://error-center.aliyun.com/status/product/live) 

