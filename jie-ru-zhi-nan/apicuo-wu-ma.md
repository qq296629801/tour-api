#### 直播 {#2）认证方式}

客户端向httpgw发起请求时，需要在HTTP头部中增加字段Authorization。

##### 设备认证 {#设备认证}

###### Authorization {#authorization}

设备认证方式中的Authorization内容格式如下：

```
version={version};time={time};sign={sign};key={key};device_type_id={device_type_id};device_id={device_id};service={service}

```

###### Signature {#signature}

Authorization中的sign字段是签名串，是对下列组合的字符串（UTF-8编码）做MD5计算

```
key={key}
&
device_type_id={device_type_id}
&
device_id={device_id}
&
service={service}
&
version={version}
&
time={time}
&
secret={secret}

```

###### 字段说明 {#字段说明}

| 字段名称 | 意义 |
| :--- | :--- |
| version | 版本，当前为1.0 |
| time | UNIX时间 |
| sign | 签名串，具体生成方式见下文 |
| key | 授权KEY，从[开发者平台](https://developer.rokid.com/voice/#/)获取 |
| device\_type\_id | 设备类型ID，同样从开发者平台获取 |
| device\_id | 设备ID，客户端自己维护 |
| service | 服务类型，自定义，建议与请求的服务名保持一致 |
| secret | 密钥，从开发者平台获取 |



