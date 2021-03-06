# lan-uploader
[![npm](https://img.shields.io/npm/dm/lan-uploader.svg?style=flat-square)](https://www.npmjs.com/package/lan-uploader)  [![npm](https://img.shields.io/npm/v/lan-uploader.svg?style=flat-square)](https://www.npmjs.com/package/lan-uploader)  [![license](https://img.shields.io/github/license/lian-yue/vue-upload-component.svg?style=flat-square)](https://www.npmjs.com/package/vue-upload-component)


> Vue.js file upload component
> The component is just a button


  - [x] Multi-file upload
  - [x] Upload directory
  - [x] Drag upload
  - [x] Drag the directory
  - [x] Upload multiple files at the same time
  - [x] html4 (IE 9)
  - [x] `PUT` method
  - [x] Customize the filter
  - [x] thumbnails
  - [x] Chunk upload

原版本: v2.8.15
本组件使用此版本号: v2.8.42 (只是修改了一些功能)

# Pre
> 此组件是使用 vue-upload-component 根据项目需要修改而来，依然采用Apache 2.0协议。 如有侵权请告知删除 lan6995@gmail.com

1. 添加了总体进度 upload.progress (通过每个文件的progress计算而来)
2. 修改了input-file与input-filter两个事件，添加一个参数`evt` 用以简单识别事件类型 `2018-11-26`:添加错误报告
3. 添加上传成功事件：`single-success` 单文件上传完毕 、 `all-success` 所有文件上传完毕
4. 自定义实现了ChunkUploadHandler
  - 将startBody/uploadBody/finishBody的获取方式修改为`从文件获取`(独立)，原方式: 从chunkOptions中获取(统一)
  - 将updateFileProgress的实现从 this.file.progress = this.progress 修改为 this.uploader.update(this.file, { progress: this.progress }) 以触发事件
5. 添加自动获取文件md5功能: 触发上传时生成并保存至file.md5 注: 文件md5取 chunk_head/chunk_middle/chunk_tail 生成
6. 添加文件秒传功能 (任意方式)
7. 添加断点续传功能 (chunk方式)
8. 将上传按钮与上传组件分离,可简单实现多个按钮选择文件到同一个uploader上.
9. 为 remove / clear / update 添加参数 triggerEvt,可控制是否触发事件(外部调用其实不需要触发事件,影响性能)
10. 添加几个事件 @all-in/@all-done/@file-success/@file-error,分别代表(选择完毕/本次上传完成[成功或者失败]/单个文件上传成功/单个文件上传失败)

其余均与原组件 v2.8.15 无差别

# 原作者仓库

https://lian-yue.github.io/vue-upload-component/

# Installation

``` bash
npm install vue-upload-component --save
```

# Documentation

https://lian-yue.github.io/vue-upload-component/#/documents







> Vue.js 文件上传组建
> 组件只是一个按钮

  - [x] 上传多文件
  - [x] 上传目录
  - [x] 拖拽
  - [x] 拖拽目录
  - [x] 多线程
  - [x] html4(IE 9)
  - [x] `PUT` 方法
  - [x] 自定义过滤器
  - [x] 缩略图

# 演示

https://lian-yue.github.io/vue-upload-component/#/zh-cn/



# 安装

``` bash
npm install vue-upload-component --save
```

# 文档

https://lian-yue.github.io/vue-upload-component/#/zh-cn/documents



# Special thanks (特别感谢)

- [@josec89](https://github.com/josec89)

原作者: 
- [@lian-yue](https://github.com/lian-yue)