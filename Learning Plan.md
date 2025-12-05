# NestJs 快速开始

author: 胡林森-[Gala-Lin](mailto:gala-lin@qq.com)

每天灵活安排4小时，在三到四天快速上手

## 0-4H

### TypeScript 与 NestJS 核心基础

**理论基础：**

#### [TS](https://www.typescriptlang.org/docs/handbook/intro.html)

1. - [x] 基础类型（`string/number/boolean`、数组、元组、枚举）
2. - [x] 接口（`interface`）、类型别名（`type`）→ 对应 Java 的`interface`/`POJO`
3. - [ ] 类与装饰器（`class`/`@Decorator`）→ NestJS 的核心语法，对应 Java 的注解
4. - [ ] 泛型 → 对应 Java 泛型，ORM / 工具类常用
5. - [ ] 异步编程（`Promise`/`async/await`）→ 替代 Java 的`CompletableFuture`
6. - [ ] 模块系统（`import/export`）→ 对应 Java 的`import/package`

#### [NestJS](https://docs.nestjs.com/providers#scopes)

- [x] 

| NestJS 概念          | 对应 Spring 概念        |
| -------------------- | ----------------------- |
| Module（模块）       | `@Configuration`        |
| Controller（控制器） | `@RestController`       |
| Service（服务）      | `@Service`/`@Component` |
| Provider（提供者）   | Spring Bean             |

**实践操作**

1. - [x] 初始化NestJS项目，了解文件组织结构
2. - [ ] 使用TS实现简单算法题，如[21. 合并两个有序链表 - 力扣（LeetCode）](https://leetcode.cn/problems/merge-two-sorted-lists/)等
3. - [ ] 尝试异步函数

## 4-6H

**理论学习**

- [ ] 控制器（`@Controller`）、路由装饰器（`@Get`/`@Post`）、参数接收（`@Body`/`@Param`）

- [ ] 服务（`@Injectable`）、依赖注入（DI）、模块间导入导出

### demo接口、服务

1. - [ ] 创建`UserController`，实现`GET /users/:id`接口
2. - [ ] 创建`UserService`，注入控制器

## 6-8H

### 数据库集成与简单CRUD（TypeORM+MySQL）

**理论学习**

#### [TypeORM 配置、实体定义、Repository 模式、基础 CRUD](https://typeorm.bootcss.com/#快速开始)



**实践操作**

#### 实体映射、CRUD 操作（用户注册/查询）

1. - [x] 定义.env

```typescript
# 数据库配置
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=041225
DB_NAME=blog_system

# JWT配置
JWT_SECRET=f769c3cf25fc58e8d3a979f8df34e1f9b870dea6bd6c76886ba715d1e50d9fcc
JWT_EXPIRES_IN=7d
```

2. - [ ] 配置 MySQL 连接
3. - [ ] 验证连接
4. - [ ] 用户注册（`save`）、查询（`findOne`）、分页查询(`findAll`)功能

```typescript
可能用到的注解
定义user类：
@Entity
@PrimaryGeneratedColumn()
@Column({ unique: true ... }) 

定义service：
@Injectable()
@InjectRepository
```

## 8-9H 

#### Security

**理论学习**

1. - [ ] Authorization(RBAC)
2. - [ ] CORS

## 9-11H

**理论学习**

#### 注册 / 登录 / JWT 校验 / 权限守卫

1. - [ ] 密码加密、注册接口实现
2. - [ ] JWT 集成、登录接口
3. - [ ] 权限守卫/拦截器

**实践操作**

1. - [ ] 重构注册接口，密码加密
2. - [ ] 配置 JWT密钥、过期时间（.env），实现登录接口，后续集成redis缓存实现多次登陆失败锁定用户一段时间
3. - [ ] 实现 Jwt AuthGuard，保护接口

## 11-14H

#### NestJS中的中间件了解与实现了解

**理论学习**

1. - [ ] [[Redis - 微服务 | NestJS 中文网]](https://docs.nestjs.cn/microservices/redis)
2. - [ ] [RabbitMQ - 微服务 | NestJS 中文网](https://nest.nodejs.cn/microservices/rabbitmq)等MQ微服务
3. - [ ] 部署

**实践操作**

1. - [ ] 配置Redis、简单键值对与逻辑实现
2. - [ ] 配置MQ、生产者、交换机、队列、消费者...
3. - [ ] 简单检验配置结果

## 14-16H

**理论学习**

1. - [ ] 全局异常处理/响应
2. - [ ] 已有项目迁移思路

**实践操作**

1. - [ ] 创建全局处理类
2. - [ ] 已有项目重点接口迁移
3. - [ ] nestjs中接口文档快速实现方法`nestjs swagger`
