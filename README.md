# peachy-mascots

PeachyPet 桌宠资源中心。应用读取本仓库的 `catalog.json`，从对应 Release 下载桌宠包，校验 SHA-256 后导入。

## 包格式

一个 zip，根目录下：

- `pet.json`：PeachyPet 动画配置，媒体路径相对于包根目录
- `media/`：视频与图片

## 发布一只桌宠

在 peachy-code 仓库里：

```bash
scripts/publish-pet.sh "<桌宠名>" <pack-id> --version <N> --upload
```

脚本打包、上传到 Release `<pack-id>-v<N>`，并打印清单条目；把条目写进 `catalog.json` 后提交。
