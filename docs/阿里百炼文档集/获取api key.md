# 获取api key

> Ref: [大模型服务平台百炼控制台](https://bailian.console.aliyun.com/cn-beijing/?spm=5176.29597918.J_SEsSjsNv72yRuRFS2VknO.2.3f38133crv6HKa&tab=api#/api/?type=model&url=2712195
>
> 消化api文档，防止每次需要打开网页， 仅此而已 。 文档参考自阿里云百炼 /api参考/获取api key

使用阿里云百炼大模型或者应用前，请先获取api key作为鉴权凭证。

## 获取api key

1. 前往[API Key（北京）](https://bailian.console.aliyun.com/?tab=model#/api-key)、[API Key（新加坡）](https://modelstudio.console.aliyun.com/?tab=model#/api-key)或[API Key（弗吉尼亚）](https://modelstudio.console.aliyun.com/us-east-1?tab=model#/api-key)页面，单击**创建API KEY**。

2. 在弹窗中配置以下信息，并单击**确定**：

   - **归属账号**：建议选择主账号（**账号**列内容为纯数字账号ID）。
   - **归属业务空间**：建议选择默认业务空间。

3. 点击API Key旁的![image](https://help-static-aliyun-doc.aliyuncs.com/assets/img/zh-CN/8412544571/p994217.png)图标获取该API Key。

   > 主账号可以查看全部API Key，子账号仅能查看自己创建的API Key。

   ![2026-02-11_11-56-27](./imgs/p1054137.jpg)

## 使用api key

- **方式一：在**[**第三方工具**](https://help.aliyun.com/zh/model-studio/use-chat-client-or-development-tool/)**中调用模型**

  如果在Chatbox等工具或平台中调用模型，您可能需要输入三个信息：

  - 本文获取的API Key
  - API Key所属地域的Base URL：
    - **华北2（北京）**：`https://dashscope.aliyuncs.com/compatible-mode/v1`
    - **新加坡**：`https://dashscope-intl.aliyuncs.com/compatible-mode/v1`
    - **美国（弗吉尼亚）**：`https://dashscope-us.aliyuncs.com/compatible-mode/v1`
  - 模型名称，如qwen-plus

  常用工具配置：[Chatbox](https://help.aliyun.com/zh/model-studio/chatbox)、[Cline](https://help.aliyun.com/zh/model-studio/cline)、[Claude Code](https://help.aliyun.com/zh/model-studio/claude-code)、[Dify](https://help.aliyun.com/zh/model-studio/dify)、[OpenClaw（原 Clawdbot/Moltbot）](https://help.aliyun.com/zh/model-studio/openclaw)、[Postman](https://help.aliyun.com/zh/model-studio/first-call-to-image-and-video-api)、[Qwen Code](https://help.aliyun.com/zh/model-studio/qwen-code)。

- **方式二：通过代码调用模型**

  通过代码[首次调用千问API](https://help.aliyun.com/zh/model-studio/first-api-call-to-qwen)，建议[配置API Key到环境变量](https://help.aliyun.com/zh/model-studio/configure-api-key-through-environment-variables)，以避免硬编码在代码中导致泄露风险。

请勿以任何方式公开API Key，避免因未经授权的使用导致安全风险或资金损失。

## API Key权限说明

API Key的调用权限完全由其**归属业务空间**决定。**同一空间内的API Key权限相同**，无需为不同模型（如文生文、文生图、语音合成）创建不同的API Key。

- **默认业务空间下的API Key：**可调用所有[标准模型](https://help.aliyun.com/zh/model-studio/models)，以及默认业务空间内的[应用](https://help.aliyun.com/zh/model-studio/application-introduction)。
- **子业务空间下的API Key：**可调用该子业务空间已获得[授权](https://help.aliyun.com/zh/model-studio/use-workspace#f2e68d7ba7ubk)的标准模型，以及该子业务空间内的应用。

**调用在阿里云百炼**[**调优后的模型**](https://help.aliyun.com/zh/model-studio/model-training-overview)**：**此类模型部署成功后，仅能用其所在业务空间的API Key调用，无需[授权](https://help.aliyun.com/zh/model-studio/use-workspace#f2e68d7ba7ubk)。

## **API Key时效性说明**

创建的API Key永久有效，手动删除后即失效。

若需为第三方应用或用户提供临时访问权限，或需严格控制敏感数据访问、删除等高风险操作，可[生成临时 API Key](https://help.aliyun.com/zh/model-studio/generate-temporary-api-key)（有效期60秒），避免暴露长期有效的API Key，降低泄露风险。

## **常见问题**

**Q：单个主账号下最多能创建多少个API Key？**

A：每个主账号下最多可创建20个业务空间（包括默认业务空间），每个业务空间下最多可创建20个API Key。

**Q：RAM用户被删除后，其创建的API Key是否依然可用？**

A：在RAM控制台中[禁用或删除RAM用户](https://help.aliyun.com/zh/ram/user-guide/delete-a-ram-user)后，其创建的所有API Key均将失效，无法再用于模型调用。





