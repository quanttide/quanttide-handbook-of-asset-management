# 飞书知识库资产

## 资产目录

飞书知识库资产以 JSON 格式存储，按知识库（space）和节点（node）层级组织。每个知识库对应一个目录，包含知识库资产元数据文件和节点列表；每个节点对应一个 JSON 文件，包含节点资产元数据和文档详情。

```
feishu_wiki/
├── metadata.json          # 整体元数据（知识库列表、统计）
└── spaces/
    ├── space_{space_id}/
    │   ├── metadata.json  # 知识库信息（name, space_id, description）
    │   └── nodes/
    │       ├── node_{node_token}.json   # 节点详情（node + detail）
    │       └── ...
    └── ...
```

## 资产发现

### 授权

需要使用用户 Token（`user_access_token`）而非应用 Token（`token_access_token`），通过 本地登陆`lark-cli`访问飞书知识库资产。

### 步骤

1. `/open-apis/wiki/v2/spaces` - 获取知识库列表：`lark-cli api GET`
2. `/open-apis/wiki/v2/spaces/{id}/nodes` - 获取节点列表：`lark-cli api GET` + 递归
3. `wiki spaces get_node` - 获取节点详情：`lark-cli wiki spaces get_node`
