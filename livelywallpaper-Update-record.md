# LivelyWallpaper 版更新日志

## beta1
- 新增 `beta1.html`，作为 Lively Wallpaper 适配版本
- 新增 `LivelyProperties.json`，提供自定义面板入口
- 支持面板控制“定时换图”间隔，不触发立即换图
- 保留“随机壁纸”按钮，手动触发随机接口
- 首次加载使用“每日壁纸”，定时换图使用“随机壁纸”

## beta2
- 新增 `beta2.html`，适配 Lively 2.2.1.0 自定义面板格式
- 修正 `LivelyProperties.json` 为根对象结构，dropdown 使用索引值
- “随机壁纸”改为 checkbox 触发，兼容无 button 控件版本
- 新增“壁纸分辨率”切换（1080P/UHD），切换后立即刷新壁纸
- 移除页面内定时选择框，改为显示“定时换图：N 分钟”并跟随面板配置
- 优化分辨率标签显示，按当前分辨率模式展示 1080P/UHD

## beta3
- `beta2.html` 改为多源加载策略，默认继续使用 `bing.img.run`
- 主源连续失败 5 次后，自动切换到第三方 4K 随机接口
- 新增两个备用源：`bing.biturl.top` 和 `bingw.jasonzeng.dev`
- 备用源失败时会在备用源池之间轮换，并保持 5 秒重试节奏
- `LivelyInfo.json` 更新标题与描述，方便区分新版导入包
