#### 3）接口 {#3）接口}

##### 地址 {#地址}

```
https://apigwrest.open.rokid.com

```

##### 绑定接口 （POST） {#绑定接口-（post）}

```
/v1/device/deviceManager/bindMaster

```

###### 参数说明： {#参数说明：}

| 参数名称 | 意义 |
| :--- | :--- |
| Authorization | 认证信息，http请求时，放置在header中 |
| body | 传入json类型的字符串 例：{"userId":"xxxx"} userId是rokid账户id |
| Content-Type | application/json;charset=utf-8 |

###### 返回结果： {#返回结果：}

```
{
    "resultCode": 0,
    "message": "success"
}

```

##### 解绑接口 （POST） {#解绑接口-（post）}

```
/v1/device/deviceManager/unBindMaster

```

###### 参数说明： {#参数说明：_1}

| 参数名称 | 意义 |
| :--- | :--- |
| Authorization | 认证信息，http请求时，放置在header中 |
| body | 传入json类型的字符串 例：{"userId":"xxxx"} userId是rokid账户id |
| Content-Type | application/json;charset=utf-8 |

###### 返回结果： {#返回结果：_1}

```
{
    "resultCode": 0,
    "message": "success"
}
```



