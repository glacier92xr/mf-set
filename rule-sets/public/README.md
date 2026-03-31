# 项目公共维护列表

欢迎提交PR！您可以通过在线编辑功能并提交PR，以维护此处列表！

- fake-ip-filter.yaml————用于fake-ip地址过滤

> [!tip]
> 修改时：
>
> - 请遵循列表内的文件格式，使用LF换行符及UTF8编码！
> - 请勿删除列表末尾的空行！

## 使用方法

- 请将fake-ip-filter.yaml文件添加到您的规则集中，以启用fake-ip地址过滤功能。

```yaml
rule-providers:
  fake-ip-filter:
    format: yaml
    behavior: domain
    url: >-
      https://gh-proxy.com/https://raw.githubusercontent.com/glacier92xr/mf-set/refs/heads/main/rule-sets/public/fake-ip-filter.yaml
    path: "./rule_provider/fake-ip-filter.yaml"
    type: http
    interval: 86400

dns:
  enable: true

  fake-ip-filter:
    # fakeip-filter 为 rule-providers 中的名为 fakeip-filter 规则订阅，
    # 且 behavior 必须为 domain/classical，当为 classical 时仅会生效域名类规则
    - rule-set:fake-ip-filter
```
