# Java_for_beginner
# Java 全景课堂
一套面向初学者的**交互式 Java** 完整课程：17 章、15 个可视化实验、51 道章节自测、108 个代码示例（其中 56 个可一键在本机编译运行），覆盖从语法基础、面向对象、集合与 Stream，到并发、JVM、测试与完整项目。

课程首页
<img width="1440" height="1100" alt="preview-home-light" src="https://github.com/user-attachments/assets/18b8bb5d-8bf5-45ea-be70-7a74fd22688e" />


运行代码需要：

- **JDK 17+**（课程示例兼容 17 / 21 / 25；虚拟线程示例需要 21+）
- **Node.js 18+**（只用于本地静态服务与调用 `javac` / `java`；复跑验收脚本建议 Node 22+，脚本使用全局 `WebSocket`）

`javac` 和 `java` 需要在 PATH 中，或正确配置 `JAVA_HOME`。

## 课程内容

| 章节                  | 主题               | 关键内容                                                     |
| --------------------- | ------------------ | ------------------------------------------------------------ |
| [01](index.html#ch01) | 认识 Java          | JDK / JRE / JVM、字节码、第一个程序、包与命名、Scanner、排错 |
| [02](index.html#ch02) | 变量、类型与运算   | 八种基本类型、转换与溢出、运算符、浮点陷阱、BigDecimal、包装类 |
| [03](index.html#ch03) | 流程控制           | if / switch 箭头语法、for / while / do-while、break / continue / 标签 |
| [04](index.html#ch04) | 方法与递归         | 方法设计、值传递、重载、可变参数、调用栈、递归与记忆化       |
| [05](index.html#ch05) | 数组与字符串       | 数组、二维数组、复制、String 不可变、StringBuilder、文本块、正则 |
| [06](index.html#ch06) | 类与对象           | 构造器、封装、static、对象内存、record                       |
| [07](index.html#ch07) | 继承与多态         | extends / super、重写、动态分派、Object 契约、抽象类、组合   |
| [08](index.html#ch08) | 接口、枚举与设计   | 接口、default、枚举、策略模式、依赖注入、SOLID、注解         |
| [09](index.html#ch09) | 异常处理           | 异常体系、try / catch / finally、try-with-resources、自定义异常、反模式 |
| [10](index.html#ch10) | 集合与泛型         | List / Set / Map、ArrayList、HashMap 原理、泛型、类型擦除、PECS |
| [11](index.html#ch11) | Lambda 与 Stream   | 函数式接口、方法引用、Stream 流水线、Collectors、Optional、并行流 |
| [12](index.html#ch12) | 日期时间与 IO      | java.time、时区、Path / Files、字符流、CSV 处理、编码        |
| [13](index.html#ch13) | 并发编程           | 线程、竞态条件、synchronized、volatile、Atomic、线程池、虚拟线程 |
| [14](index.html#ch14) | JVM、内存与性能    | 运行时数据区、类加载、GC、G1 / ZGC、JIT、jstack / jmap / JFR |
| [15](index.html#ch15) | 测试、构建与工程化 | JUnit 5、TDD、Maven、日志、Git、调试、CI                     |
| [16](index.html#ch16) | 综合项目           | 图书借阅系统：需求、分层、完整源码、测试、扩展路线           |
| [17](index.html#ch17) | 知识全景与进阶     | 版本演进、后端 / Android / 大数据路线、30 天计划、自检清单   |

## 15 个可视化实验

每个实验都可以点击、单步或切换参数，而不是静态截图：

1. **JVM 流水线**：源码 → javac → 字节码 → JVM → 操作系统
2. **类型与溢出**：8 种基本类型的宽度、范围、包装类；byte 127 + 1 回绕
3. **for 循环单步**：逐行高亮、变量观察、循环轮次
4. **数组索引**：线性查找、修改元素、越界异常
5. **String 不可变**：拼接时旧对象与新对象的引用变化
6. **调用栈**：factorial(4) 的压栈、返回、弹栈
7. **堆与引用**：栈变量、堆对象、null、GC 可达性
8. **动态分派**：编译时类型 vs 运行时类型
9. **策略模式**：支付接口的三种实现与多态调用
10. **异常栈展开**：异常从抛出点逐层向外传播
11. **ArrayList vs LinkedList**：随机访问、头插、尾插、查找成本
12. **HashMap 桶**：哈希定位、冲突链、负载因子
13. **Stream 流水线**：filter / map / sorted / collect 每步的元素变化
14. **线程竞争**：无锁丢失更新 vs 加锁结果
15. **GC 标记清除**：从 GC Roots 做可达性分析

![代码运行](preview-run.png)

## 功能

- **17 章完整正文**：不是 API 罗列，而是“概念 → 代码 → 实验 → 测验”的闭环。
- **真实代码运行**：带 `运行` 按钮的示例由本地 JDK 编译执行，编译错误与运行输出直接显示。
- **51 道即时自测**：选错立刻标出正确答案与解析，可重试。
- **学习进度**：章节完成状态、侧栏进度、首页继续学习，保存在 `localStorage`。
- **全局搜索**：`Ctrl/Cmd + K` 或 `/`，搜索章节、小节和知识点。
- **深色 / 浅色主题**：跟随系统，或手动切换；`?theme=light` / `?theme=dark` 可强制。
- **响应式**：桌面三栏（目录 / 正文 / 本页目录）、移动端抽屉导航。
- **打印 / PDF**：右上角打印按钮，打印样式会展开全部章节、隐藏交互控件。
- **零前端依赖**：没有 React / Vue / 构建框架，原生 HTML / CSS / JavaScript，离线可用。

![移动端实验](preview-mobile-lab.png)

## 目录结构

```text
java-course/
├─ index.html            # 构建产物：直接用浏览器打开
├─ run.bat               # Windows 启动器：本地服务 + 自动打开浏览器
├─ server.js             # 静态服务 + /api/run Java 运行器
├─ build.js              # 拼接 src/ 并转义代码块
├─ src/
│  ├─ shell.html         # 页面骨架、侧栏、搜索层
│  ├─ home.html          # 首页
│  └─ ch01.html … ch17.html
├─ assets/
│  ├─ course.css         # 视觉系统、排版、响应式、打印
│  ├─ course.js          # 路由、进度、搜索、测验、代码高亮/运行
│  └─ labs.js            # 15 个可视化实验
├─ tools/
│  ├─ visual-test.js     # 无依赖 CDP 验收（Node 22+；截图 + 交互）
│  ├─ output-audit.js    # 逐段运行示例并对比预期输出
│  └─ tag-audit.js       # HTML 标签闭合检查
├─ preview-*.png         # 预览截图
└─ README.md
```

## 二次开发

课程正文在 `src/`，修改后重新构建：

```bash
node build.js
```

`build.js` 会：

1. 按 `home → ch01 … ch17` 顺序拼接；
2. 把 `<pre class="code">` 中的原始代码安全转义；
3. 为代码块生成标题栏、复制按钮和可选的运行按钮；
4. 输出单文件 `index.html`。

新增一个可运行示例：

```html
<pre class="code" data-run data-title="Demo.java"><code class="language-java">public class Demo {
    public static void main(String[] args) {
        System.out.println("Hello");
    }
}</code></pre>
```

带标准输入的示例加 `data-stdin="..."`。需要 Java 21 的示例请明确标注。

## 本地运行器说明

`server.js` 的 `/api/run`：

- 只监听 `127.0.0.1`；
- 代码写入 `.runs/` 下的临时目录，运行后自动清理；
- 编译超时 12 秒，运行超时 8 秒，输出上限约 64 KB；
- 拒绝启动外部进程的代码（`Runtime.exec` / `ProcessBuilder`）；
- 编译诊断使用 UTF-8，中文错误信息不会乱码；
- 捕获 `Scanner` 所需的 stdin。

这不是沙箱级安全隔离。它适合运行你自己写的学习代码，**不要运行来源不明的代码**。

## 验收记录

本项目已用真实 Chrome（CDP）完成以下检查：

- 18 个视图全部可路由；
- 15 个实验全部初始化，核心控件点击无 JS 异常；
- 51 道测验可作答、显示解析、重试；
- 56 个可运行代码块全部通过 `javac` 编译并执行；
- 有“预期输出”的代码块逐行比对通过；
- 代码运行面板正确显示输出；
- 搜索、主题切换、移动端抽屉、横向溢出检查通过；
- 控制台无错误。

复跑：

```bash
node server.js --no-open
node tools/visual-test.js
```

> `visual-test.js` 会启动 headless Chrome 并截图，需要本机安装 Chrome，且允许浏览器启动。

## 课程边界

“完整”指**本科 Java 核心课程 + 初级工程实践主干**：语言、OOP、集合、Stream、IO、并发、JVM、测试、构建与一个完整项目。Java 生态没有边界，JDBC、Spring Boot、Android、大数据等方向在[第 17 章](index.html#ch17)给出学习地图，而不是假装在一门课里全部讲完。

适合：

- 软件工程 / 计算机专业大二学生；
- 正在准备期末、课程设计或初级面试；
- 已会一点语法，但说不清“内存里发生了什么”的学习者。

不适合：

- 已经能独立开发 Spring Boot 项目、想学分布式架构的开发者；
- 想系统学习 Android / 大数据平台的人（请把本课程当作 Java 语言基础）。

---

课程内容、图形与代码均为本项目原创生成，可自由用于个人学习与教学。Java 是 Oracle 的商标；本项目与 Oracle 无关联。
