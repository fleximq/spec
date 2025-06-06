<div align="center">
    <img width="120" src="icon.svg" alt="logo">
  <h1 id="fleximq">fleximq 规范</h1>
</div>

本仓库托管 fleximq 协议的官方规范。fleximq 是一种为高性能和高可靠性而设计的灵活消息队列协议。

## 协议概述

fleximq 旨在为应用程序通过消息进行异步通信提供一种标准化的方式。详细的协议规范可以在本仓库的相应文档中找到。

> 注意：本协议中所有多字节数值均采用网络字节序（大端序）编码。
> 所有结构化数据（Header 和 Payload）均使用 MessagePack 格式进行序列化。

### 主要设计目标

fleximq 旨在提供一个通用的、编程语言无关的、跨平台的消息传递协议。它支持多种通信模式，如请求/响应、发布/订阅和通知，可运行于多种传输层之上。该协议注重效率和清晰的语义定义，使其适用于分布式系统、插件系统，并为物联网（IoT）应用进行了优化。与 MQTT 等协议相比，fleximq 支持更广泛也更复杂的通信模式。

### 编码约定

- **数值**: 所有多字节数值均采用网络字节序（大端序）编码。
- **结构化数据**: Header 和 Payload 部分使用 MessagePack 格式进行序列化。
- **字符串**: 所有字符串必须使用 UTF-8 编码。

* [草案](./draft/)
* RFCs (提议征集) 在一个独立的仓库中进行管理: [fleximq/rfcs](https://github.com/fleximq/rfcs)
* [正式规范](./official/)

## 贡献流程

我们欢迎对 fleximq 规范做出贡献。该流程旨在透明和协作：

1.  **RFC (Request for Comments) 提交**：

    - 在专门的 RFCs 仓库中提交 RFC 来提议新功能、更改或改进: [fleximq/rfcs](https://github.com/fleximq/rfcs)。
    - RFC 应详细说明提议的动机、设计和潜在影响。
    - 社区将在其仓库中对 RFC 进行讨论和反馈。

2.  **草案阶段**：

    - 如果 RFC 在审查和讨论后被接受，其内容将用于在本 (`spec`) 仓库的 `draft` 目录中创建或更新草案规范。
    - 在此阶段，该提议被视为工作草案，可能会在此处进行进一步的完善。

3.  **正式规范**：
    - 一旦草案被主流的 fleximq 兼容系统实现，并被证明是稳定和有益的，它就可以被提升为正式规范。
    - 正式规范将从本仓库的 `draft` 目录移至 `official/` 目录。

## 版本控制

fleximq 协议规范遵循语义化版本 2.0.0 (Semantic Versioning 2.0.0)。每个正式版本的规范都将被明确标记和记录。

## 如何贡献

1.  对于规范文档的更改（草案、正式规范）：
    - Fork 本 (`spec`) 仓库。
    - 为您的更改创建一个新的分支。
    - 向本仓库提交一个 Pull Request 以供审查。
2.  对于新的提议或讨论，请参考 RFCs 仓库: [fleximq/rfcs](https://github.com/fleximq/rfcs)。

## 许可证

fleximq 规范采用 [Unlicense 许可证](./LICENSE)授权。
