# DART实现七牛云分片上传

### 项目背景
我们的团队在开发Flutter短视频录制模块的过程中，发现七牛云没有兼容flutter的上传模块，并且原生Java/OC模块经过重写后依然存在体积过大的问题，于是产生了这个项目，实现轻量化上传。

基于七牛云的对象存储块文档，我们可以将flutter或dart服务器上的二进制文件进行切割上传，并在云端调用命令整合即可。

七牛云文档： https://developer.qiniu.com/kodo/api/1286/mkblk

上传时需要调用自身的服务器获取七牛云的授权Token链接，安全交互算法可以自行编写。

经过测试，媒体文件上传后可正常播放。
