# Requirements Document

## Introduction

医患问卷指导系统旨在建立一个高效的医患沟通平台，使医生能够接收患者提交的健康问卷，查看问卷回答和体检报告，并基于这些信息提供个性化的健康指导。同时，患者可以接收医生的健康指导，并查看与指导相关的问卷内容，从而更好地理解医生的建议。

## Requirements

### Requirement 1: 医生端消息通知与问卷查看

**User Story:** 作为一名医生，我希望能够接收到患者提交问卷的消息提醒，并能够查看问卷详情，以便及时了解患者的健康状况。

#### Acceptance Criteria

2. WHEN 医生点击消息提醒 THEN 系统SHALL展示该患者提交的问卷详情
3. WHEN 医生查看问卷详情 THEN 系统SHALL显示问卷的所有问题和患者的回答
4. WHEN 医生查看问卷详情 THEN 系统SHALL提供进入健康指导编辑界面的入口

### Requirement 2: 体检报告查看与提醒

**User Story:** 作为一名医生，我希望能够查看患者的体检报告，如果患者未上传体检报告，我希望能够提醒患者上传，以便我能够基于更全面的信息提供健康指导。

#### Acceptance Criteria

1. WHEN 医生查看患者问卷详情 THEN 系统SHALL同时显示该患者的体检报告（如有）
2. WHEN 患者未上传体检报告 THEN 系统SHALL显示"无体检报告"的提示
3. WHEN 医生点击"提醒上传体检报告"按钮 THEN 系统SHALL向患者发送上传体检报告的提醒

### Requirement 3: 健康指导编辑与发送

**User Story:** 作为一名医生，我希望能够基于患者的问卷回答和体检报告，编辑并发送个性化的健康指导，以便为患者提供专业的健康建议。

#### Acceptance Criteria

1. WHEN 医生点击"提供健康指导"按钮 THEN 系统SHALL打开健康指导编辑界面
2. WHEN 医生进入健康指导编辑界面 THEN 系统SHALL显示健康指导模板列表
3. WHEN 医生选择健康指导模板 THEN 系统SHALL自动填充模板内容到编辑区
4. WHEN 医生在编辑区修改内容 THEN 系统SHALL实时保存修改
5. WHEN 医生勾选健康指导建议 THEN 系统SHALL将勾选的建议添加到指导内容中
6. WHEN 医生点击"发送"按钮 THEN 系统SHALL将健康指导发送给患者
7. WHEN 健康指导发送成功 THEN 系统SHALL更新该问卷的状态为"已指导"

### Requirement 4: 患者端健康指导接收

**User Story:** 作为一名患者，我希望能够接收到医生发送的健康指导消息，以便及时了解医生的建议。

#### Acceptance Criteria

1. WHEN 医生发送健康指导 THEN 系统SHALL在患者端显示新消息提醒
2. WHEN 患者点击消息提醒 THEN 系统SHALL显示健康指导消息列表
3. WHEN 患者端收到新的健康指导 THEN 系统SHALL在消息列表中显示未读标记
4. WHEN 患者点击健康指导消息 THEN 系统SHALL打开健康指导详情页面

### Requirement 5: 健康指导详情查看

**User Story:** 作为一名患者，我希望能够查看医生发送的健康指导详情，并了解指导与问卷的关联，以便更好地理解医生的建议。

#### Acceptance Criteria

1. WHEN 患者打开健康指导详情页面 THEN 系统SHALL显示医生的健康指导内容
2. WHEN 患者查看健康指导详情 THEN 系统SHALL显示与该指导相关联的问卷信息
3. WHEN 患者点击"查看相关问卷"按钮 THEN 系统SHALL显示问卷的问题和自己的回答