# BPB-CF-PAGES

**注意**: 在创建 `worker` 或 `pages` 时，项目名称禁止出现 `bpb,vless,vmess,trojan` 等字符，因为这可能会触发 Cloudflare 的检测并导致1101错误。

---

## 创建 `KV`

- 登录Cloudflare，在主页找到 **存储和数据库**，点击右边的小三角，找到 **KV**，点击右上角的 **Create** 创建空间，空间名称随意。

---

## Cloudflare worker and pages

#### 变量和机密的配置

| 变量名称 | 值 |
| :-------------: | :-------------: |
| **UUID**  | VLESS UUID  |
| **TR_PASS**  | Trojan Password  |
| **PROXY_IP**  | Proxy IP or domain (VLESS, Trojan)  |
| **SUB_PATH**  | Subscriptions' URI  |
| **FALLBACK**  | Fallback domain (VLESS, Trojan) |
| **DOH_URL**  | Core DOH |

#### 绑定 KV 空间

**`设置-->绑定-->添加-->KV命名空间`**

| 变量名称 | KV 命名空间 |
| :-------------: | :-------------: |
| **`kv`**(小写字母)  | 创建`KV`空间的名称  |

---
