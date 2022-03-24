# 任务描述

----

### 韩宇航

- 熟悉一下```CentOS```操作
- 熟悉一下```spack```，```openmpi```，以及```make```的使用
- 能够使用openmpi编译c语言并行程序,示例代码如下

```CPP
#include <mpi.h>
#include <stdio.h>

int main(int argc, char** argv) {
    // Initialize the MPI environment
    MPI_Init(NULL, NULL);

    // Get the number of processes
    int world_size;
    MPI_Comm_size(MPI_COMM_WORLD, &world_size);

    // Get the rank of the process
    int world_rank;
    MPI_Comm_rank(MPI_COMM_WORLD, &world_rank);

    // Get the name of the processor
    char processor_name[MPI_MAX_PROCESSOR_NAME];
    int name_len;
    MPI_Get_processor_name(processor_name, &name_len);

    // Print off a hello world message
    printf("Hello world from processor %s, rank %d out of %d processors\n",
           processor_name, world_rank, world_size);

    // Finalize the MPI environment.
    MPI_Finalize();
}
```


---

### 杨瑞

- 搭建基础展示页面，基础的```HTML```页面，使用```nginx```或```apache```部署到服务器
- 在[vue-element-admin](https://panjiachen.github.io/vue-element-admin-site/zh/guide/)基础之上构建管理系统
- 将[y-shell](https://github.com/ZhangLe1993/y-shell)功能融入到```vue-element-admin```


---

### 季春晓

- 了解一些企业中常见的问题，如盈利渠道、成本控制、风险规避
- 参考[阿里云文档](https://www.aliyun.com/product/scc)与[腾讯云文档](https://cloud.tencent.com/product/thpc)，撰写```项目介绍```
- 整理问卷结果

