# 如何连接并同步mysql数据库

1. 如果prisma没有初始化则先初始化。 初始化命令 `npx prisma init --datasource-provider mysql`
2. 根据生成的模板文件或者修改原配置文件 `schema.prisma` 内容如下，不需要有 model

```
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "mysql"
  url      = env("DATABASE_URL")
}

```

  env 中配置的数据库格式 `mysql://userName:password@address:port/databaseName`

3. 执行 `npx prisma db pull`
之后会将对应数据库内的模型同步到 `schema.prisma` 内


> [Quick Start](https://www.prisma.io/docs/getting-started/quickstart)
> 
> [MySQL](https://www.prisma.io/docs/concepts/database-connectors/mysql)
