# setup-ossutil

配置 ossutil 命令行工具

# Usage

See [action.yml](action.yml)

用例:

```yaml
steps:
  - uses: actions/checkout@master
  - uses: manyuanrong/setup-ossutil@v2.0
    with:
      endpoint: "oss.aliyuncs.com"
      access-key-id: "your_key_id"
      access-key-secret: "your_key_secret"
      sts-token: "sts_token"
  - run: ossutil cp -rf test.txt oss://bucket/path
```

参数

- **endpoint**：填写 Bucket 所在地域的域名信息，可参考访问域名和数据中心。
- **access-key-id**：查看方式请参考创建 AccessKey。
- **access-key-secret**：查看方式请参考创建 AccessKey。
- **sts-token**：非必配项，若采用 STS 临时授权方式访问 OSS 需要配置该项，否则置空即可。stsToken 生成方式参考临时访问凭证。

[详细用法参考，阿里云 ossutil 帮助文档](https://help.aliyun.com/document_detail/50452.html)

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
