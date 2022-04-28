# docker-gitlab

### 注册 `runner`

#### 进入 `runner` 容器

> {gitlab} 根据env替换

```shell
docker exec -it {gitlab} /bin/bash
```

#### 执行 `runner`命令

```shell
gitlab-runner register
```

##### 1. 输入 gitlab 示例的 url

> {gitlab} = 容器名

```shell
$ Enter the GitLab instance URL (for example, https://gitlab.com/):
$ http://{gitlab}/
```

##### 2. 输入 runner 的 token

> 从gitlab runner管理页获取

```shell
$ Enter the registration token:
$ xxx
```

##### 3. 输入 runner 的 描述

```shell
$ Enter a description for the runner:
$ test
```

##### 4. 输入 runner 的 tag

```shell
$ Enter tags for the runner (comma-separated):
$ test
```

##### 5. 输入 runner 的 执行方式。推荐(docker）

```shell
$ Enter an executor: docker, docker-ssh, ssh, docker+machine, docker-ssh+machine, kubernetes, custom, parallels, shell, virtualbox:
$ docker
```

##### 6. 输入 runner 的 执行方式的镜像

> 基于 step.5选择的docker

```shell
$ Enter the default Docker image (for example, ruby:2.6):
$ alpine:latest
```
