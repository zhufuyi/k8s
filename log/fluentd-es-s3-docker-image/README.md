### 说明

这是构建镜像所需的文件，镜像功能是fluent采集k8s集群所有应用和系统级的日志分别发送到aws的es和s3中。

![fluentd-es-s3.png](fluentd-es-s3.png)

<br>

### 构建镜像

> docker build -t your-image-name:tag ./
