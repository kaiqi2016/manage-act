# 抽奖活动数据模型

## Core Tables

### Activities
- id
- name
- type (A/B)
- start_date
- end_date
- status
- themes (relation to Themes)

### Themes
- id
- name (主题1 / 主题2)
- config (JSON - 背景、样式、页面布局)
- activity_id

### Prizes
- id
- name
- probability
- quantity
- activity_id

### Participants
- id
- user_id
- activity_id
- prize_id
- draw_time

## 运营拖拽配置
Budibase 支持拖拽表单和自动化，可实现无代码配置活动。