步骤一：
修改dockerimages/hmall/DockerFile，加上要拉取的镜像，镜像地址去到“https://hub.docker.com/”上查。

步骤二：
登录aliyun服务器“容器镜像服务-》实例列表（个人版）-》镜像仓库（找一个能构建的仓库，或者新建一个仓库）-》构建”

步骤三：
添加规则
  - 类型： Branch
  - Branch/tags: main
  - 构建的上下文目录： github上的Dockerfile文件存放地点（填文件夹、跳过github仓库名）
  - Dockerfile文件名：Dockerfile
  - 镜像版本
确定

步骤四：
“立即构建”并等待，成功后查看日志“Building Artifact: registry.cn-wulanchabu.aliyuncs.com/yuanfangs/XXXXXXX：XXXXX”
复制，使用docker pull 拉取到虚拟机

docker images 查看镜像名

docker tag oldname:oldtag newname:newtag 修改镜像名

docker rmi oldname:oldtag 删除旧镜像名
