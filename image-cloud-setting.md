# 图床配置

## 1. 环境配置

### 1.1 node 安装

### 1.2 npm 全局安装picgo

```shell
npm install picgo -g
```

有可能会因为代理问题安装报错

**解决方法：**

- 1.查看npm镜像设置

  `npm config get registry`

- 2.将npm镜像改为淘宝镜像

  `npm config set registry https://registry.npm.taobao.org`

- 3.重新进行全局安装

  `npm install picgo -g`

> picgo 全局安装成功后，需要安装对应的上传插件
>
> gitee: `picgo install picgo-plugin-gitee-uploader`
>
> github: `picgo install github-plus`
>
> 重命名插件：`picgo install rename-file`

## 1.3 安装成功后，进行配置

安装成功后，查看 picgo 所在的目录（一般是在 node 所在的目录，可以通过 `npm root -g` 查看）

需要注意：全局安装后，picgo 的默认配置文件是在 `C:\Users\%USERNAME%\.picgo\config.json` (linux 和 macOS 均为 `~/.picgo/config.json`)

**config.json 详细配置：(使用gitee)**

```json
{
  "picBed": {
    "uploader": "github",
    "current": "github",
    "github": {
      "repo": "cloudinwind/images",
      "branch": "main",
      "origin": "github",
      "token": "xxx",
      "path": "markdown_images",
      "customUrl": "https://raw.githubusercontent.com/cloudinwind/images/main/"
    },
    "gitee": {
      "repo": "huihuangshijian/images",
      "branch": "master",
      "token": "355b7d4e7f14aa8a1e294d436efd13ac",
      "path": "markdown_images",
      "customPath": "",
      "customUrl": ""
    }
  },
  "picgoPlugins": {
    "picgo-plugin-gitee-uploader": true,
    "picgo-plugin-super-prefix": true,
    "picgo-plugin-github-plus": true
  },
  "picgo-plugin-gitee-uploader": {
    "lastSync": "2023-12-09 12:45:03"
  }
}
```

**config.json 详细配置：(使用github)**

```json
{
  "picBed": {
    "uploader": "github",
    "current": "github",
    "github": {
      "repo": "cloudinwind/images",
      "branch": "main",
      "origin": "github",
      "token": "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",
      "path": "markdown_images",
      "customUrl": "https://raw.githubusercontent.com/cloudinwind/images/main/"
    },
    "gitee": {
      "repo": "huihuangshijian/images",
      "branch": "master",
      "token": "355b7d4e7f14aa8a1e294d436efd13ac",
      "path": "markdown_images",
      "customPath": "",
      "customUrl": ""
    }
  },
  "picgoPlugins": {
    "picgo-plugin-gitee-uploader": true,
    "picgo-plugin-super-prefix": true,
    "picgo-plugin-github-plus": true
  },
  "picgo-plugin-gitee-uploader": {
    "lastSync": "2023-12-09 12:45:03"
  }
}
```
