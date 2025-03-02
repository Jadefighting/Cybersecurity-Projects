# TryHackMe 进攻型安全实战 - 银行转账漏洞复现  
**时间**：2025年3月1日  
**目标**：模拟攻击银行网站，发现逻辑漏洞  
![87583c31fc6caa933317d97a3218057](https://github.com/user-attachments/assets/ec64999c-15cd-458e-a2e3-43e118165341)


## 步骤与工具  
1. **目录扫描**  
   - 使用`gobuster`扫描目标网站，发现隐藏页面`/bank_transfer`  
   - 命令：`gobuster -u http://fakebank.thm -w wordlisttxt dir`
![c2cc778b88cfa1b39ec8f1be67c6aef](https://github.com/user-attachments/assets/d273e148-b9f1-404a-aefd-d330abfb3584)

2. **漏洞利用**  
   - 通过转账，将资金转移到测试账户
![bdb81bbc2853f15080bebc75d7332a7](https://github.com/user-attachments/assets/1dbd00af-0567-45d8-b9d0-ce70c06f3d80)
![5c81eb356c426043f30e9508109dc32](https://github.com/user-attachments/assets/408190ee-6678-4361-969e-554e95c52e64)
![abcc9b0beccc154d52dbfc5b0911ac5](https://github.com/user-attachments/assets/f84491f7-499c-4235-b5f8-baaeab2e5938)


   - 漏洞类型：**业务逻辑缺陷**（未验证用户权限）  
3. **修复建议**  
   - 增加会话身份验证  
   - 对敏感操作添加二次确认（如短信验证码）

   **技术收获**：熟悉OWASP Top 10漏洞场景，掌握基础Web渗透测试流程。
