# ctf-tools
放一些自己写以及网上收集的解题脚本
```mermaid
graph TD
    A[测试人员] -->|1. 认证请求| B[服务器]
    A -->|2. 部署Agent| B
    A -->|3. 发送命令| B
    B -->|4. 转发命令| C[Agent]
    B -->|5. 存储数据| D[(数据库)]
    C -->|6. 收集数据| E[目标系统]
    E -->|7. 系统信息/漏洞| C
    C -->|8. 返回数据| B
    B -->|9. 发送结果| A
    subgraph 服务器
        B
        D
    end
    subgraph 目标网络
        C
        E
    end
