## 安装

```
# grafana-kubegraf用户授予权限
kubectl apple -f kubegraf/

# 安装CRD和prometheus-operator
kubectl apple -f kube-monitor/1_CRD_prometheus-operator

# 安装prometheus
kubectl apple -f kube-monitor/2_prometheus

# 安装k8s组件监控
kubectl apple -f kube-monitor/3_k8s-module

# 安装状态指标监控
kubectl apple -f kube-monitor/4_kube-state-metrics

# 安装节点监控
kubectl apple -f kube-monitor/5_node-exporter

# 安装blackbox(可选)
kubectl apple -f kube-monitor/6_blackbox-exporter

# 安装alert manager(可选)
kubectl apple -f kube-monitor/7_alertmanager

# 安装grafana(可选)
kubectl apple -f kube-monitor/8_grafana

# 查看所有pod是否安装成功
kubectl get pod -n monitoring
```

安装完成后，访问prometheus(例如http://<ip>:30990)，检查所有targets的状态是否都是up

参考：

- https://github.com/devopsprodigy/kubegraf
- https://github.com/prometheus-operator/kube-prometheus

