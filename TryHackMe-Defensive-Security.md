# TryHackMe 防御型安全实战 - SIEM监控与事件响应  
**时间**：2025年3月1日  

## 场景复现  
1. **告警分析**  
   - 在SIEM面板发现未认证可疑IP尝试连接并成功登录事件，定位到IP `143.110.250.149`
     ![9b044833082e8c608e4b42b73c5e2da](https://github.com/user-attachments/assets/d96cae39-1ce4-44ca-b0c0-3466deef9e27)

   - 使用`AbuseIPDB`等网站工具查询该IP历史记录，确认其为恶意扫描源
     ![4026ff01a27e0e398561e11f9a5398c](https://github.com/user-attachments/assets/25145775-2172-4001-9490-6bd91d689715)
   - 提交工单并做相应解决方案措施
     ![acb01ddfff209588fbe6ba08b0bf301](https://github.com/user-attachments/assets/2c9082bf-9745-4754-b1b9-8c92027160ae)

2. **响应措施**  
   - 提交防火墙规则变更申请，拦截该IP所有入站请求
     ![154c319d32b76baf21c5ec578d4c395](https://github.com/user-attachments/assets/fd9bba3e-8173-4d3f-9022-ab517d5a76fe)
     ![072644b45a7e49c096b9fac8011cc78](https://github.com/user-attachments/assets/99deab6d-d2a1-42bf-b3b5-dbce2a1d4145)



## 流程总结  
- **监控** → **分析** → **验证** → **处置**  
- 关键工具：SIEM平台、威胁情报数据库、防火墙  

**技能证明**：掌握基础安全事件响应流程，能独立处理低风险告警。
