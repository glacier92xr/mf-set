# 项目私有维护列表

欢迎提交PR！您可以通过在线编辑功能并提交PR，以维护此处列表！

> [!tip]
> 修改时：
>
> - 请遵循列表内的文件格式，使用LF换行符及UTF8编码！
> - 请勿删除列表末尾的空行！

## 使用方法

- 请将fake_ip_filter.yaml文件添加到您的规则集中，以启用fake-ip地址过滤功能。

```yaml
rule-providers:
  glacier:
    format: yaml
    behavior: Classical
    url: >-
      https://gh-proxy.com/https://raw.githubusercontent.com/glacier92xr/mf-set/refs/heads/main/rule-sets/private/glacier.yaml
    path: "./rule_provider/glacier.yaml"
    type: http
    interval: 86400

rules:
  - RULE-SET,glacier,DIRECT
```
