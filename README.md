
## 简介
Spring Boot API Project Seed 是一个基于Spring Boot & MyBatis的种子项目，用于快速构建中小型API、RESTful API项目，该种子项目已经有过多个真实项目的实践，稳定、简单、快速，使我们摆脱那些重复劳动，专注于业务代码的编写，减少加班。

## 采用主要组件版本
- Spring Boot： `1.5.6.RELEASE`
- 通用Mapper插件 mapper-spring-boot-starter: `1.1.3`
- 分页插件 pagehelper-spring-boot-starter: `1.2.0`

## 特性
- 统一响应结果封装及生成工具
- 统一异常处理
- 简单的接口签名认证
- 常用基础方法抽象封装
- 使用Druid Spring Boot Starter 集成Druid数据库连接池与监控
- 使用FastJsonHttpMessageConverter，提高JSON序列化速度
- 集成MyBatis、通用Mapper插件、PageHelper分页插件，实现单表业务零SQL
- 提供代码生成器根据表名生成对应的Model、Mapper、MapperXML、Service、ServiceImpl、Controller等基础代码，其中Controller模板默认提供POST和RESTful两套，根据需求在```CodeGenerator.genController(tableName)```方法中自己选择，默认使用RESTful模板。代码模板可根据实际项目的需求来扩展，由于每个公司业务都不太一样，所以只提供了一些比较基础、通用的模板，主要是提供一个思路来减少重复代码的编写，我在实际项目的使用中，其实根据公司业务的抽象编写了大量的模板。另外，使用模板也有助于保持团队代码风格的统一
- model继承支持，添加类com.company.project.core.Model, 目的是简化每个表都含有同样几个字段时的冗余，比如每个表可能都含有id, create_time, update_time。

## 注意事项
- 修改该常量 `ProjectConstant.BASE_PACKAGE `前请将种子项目的包结构也修改成要修改的包结构

## TODO

- Response规范及格式制定
- 认证方式确定
- 集成及开发其他插件
    - 表单验证 spring-boot-starter-validation 
    - 任务调度 spring-boot-starter-quartz
    - API文档 swagger2-spring-boot-starter
    - 权限认证 shiro-spring-boot-starter

## 感谢

更多信息参考 [原始README](README-ORIGINAL.md)
或原始项目 [lihengming/spring-boot-api-project-seed](https://github.com/lihengming/spring-boot-api-project-seed)
