# BPB-CF-PAGES

**注意**: 在创建 `worker` 或 `pages` 时，项目名称禁止出现 `bpb,vless,vmess,trojan` 等字符，因为这可能会触发 Cloudflare 的检测并导致1101错误。

---

## 创建 `KV`

- 登录Cloudflare，在主页找到 **`存储和数据库`**，点击右边的小三角，找到 **`KV`**，点击右上角的 **`Create`** 创建空间，空间名称随意。

---

## 绑定自定义域名，因为CF默认提供的域名在中国大陆是阻断的。

---

## Cloudflare worker and pages

#### 变量和机密的配置

| 变量名称 | 值 | 说明 |
| :-------------: | :-------------: | :-------------: |
| **UUID**  | VLESS UUID | vless的UUID |
| **TR_PASS**  | Trojan Password | trojan的密码 |
| **PROXY_IP**  | Proxy IP or domain (VLESS, Trojan) | ProxyIP域名 |
| **SUB_PATH**  | Subscriptions' URI | 订阅链接路径 |
| **FALLBACK**  | Fallback domain (VLESS, Trojan) | 故障转移 |
| **DOH_URL**  | Core DOH | DNS over HTTPS 解析服务 |

#### 绑定 KV 空间

- **`设置-->绑定-->添加-->KV命名空间`**

| 变量名称 | KV 命名空间 |
| :-------------: | :-------------: |
| **`kv`**(小写字母)  | 创建`KV`空间的名称  |

---

## 访问面板

- 上面的步骤操作完成后，复制自定义域名加 `/panel`，例如：https://xyz.bpb.com/panel， 然后访问面板，首次进入需要设置密码。

---
