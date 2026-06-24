# manage-act - Budibase 抽奖活动管理后台

## 项目目标
支持运营人员拖拽配置抽奖活动A/B + 多主题。

## 技术栈
- **Budibase** 低代码内部工具平台
- 数据模型与 Strapi 同步
- 拖拽表单、自动化工作流、权限管理

## 快速开始
1. 在 Budibase Cloud 或自主家安装 Budibase
2. 新建 App 或 Import 导出的 JSON
3. 创建数据表：
   - Activities (活动)
   - Themes (主题配置)
   - Prizes (奖品)
   - Participants (参与者)
4. 拖拽构建管理面板
5. 设置 Strapi API 数据源

## 数据模型建议
```json
{
  "Activities": {
    "name": "string",
    "type": "A | B",
    "status": "active | draft",
    "themes": "relation"
  },
  "Themes": {
    "name": "主题1 / 主题2",
    "config": "json",
    "activity": "relation"
  }
}
```

## 导出与版本控制
在 Budibase Settings 中 Export App 为 JSON，提交到此仓库保存版本。

## 与 H5-act 集成
后台配置 → Strapi 保存 → H5 前端实时更新