# tailscale-android build action
在使用headscale时，如果使用自定义证书, 由于android无法加载自签名证书，tailscale-android无法连接到headscale。因此，需要使用自签名证书构建tailscale-android。

## 用法
在github secret中配置`JKS_PASSWORD`, `JKS_BASE64`, `CERT_BASE64`

|变量|类型|作用|
|---|--------|--------|
|JKS_BASE64|base64|用于签名apk，key别名必须为tailscale|
|JKS_PASSWORD|string|用于签名apk的密码|
|JKS_KEY_ALIAS|string|用于签名apk的key别名|
|CERT_BASE64|base64|headscale证书对应的根证书|
