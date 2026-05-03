# -deepseek-bilibili-
这是一款可以用于国内视频平台Bilibili收藏夹整理的油猴插件，经原作者b站up主某不知名的根号三授权进行二次修改及分发
原视频链接:  ( https://www.bilibili.com/video/BV1LifmBgEPZ/)
原项目链接:   https://www.kamiwzw.site/posts/bilibili-favorites-ai-organizer-userscript/
具体使用方法参照于此

该项目使用DeepSeek V4进行二次修改以使其可被用于DeepSeek V4 Flash版API，经原作者授权使用MIT证书二次分发

使用了DeepSeek V4 Flash的版本Token花费大幅减少，我使用其整理了3,400左右个视频于30个以上的收藏夹之内，token花费大约是1.18元，用了1,215,240token

Flash版本虽然有时候会犯蠢，但胜在便宜，更多只会在分类标题等信息都不明确的谜语人视频时才会犯错

### 该二次分发版本有什么改进吗

1. 建议把收藏夹页数的访问间隔延迟从300ms改到1000ms，防止b站系统风控412错误
2. 建议改为以200个视频为单元进行多批量分类，防止ai输出字数限制导致json信息被"腰斩"
3. 针对于ai返回的json格式错误有在控制台里把原文丢出来，以免浪费token
4. 在因为网络问题或apikey问题的访问失败中尝试重复连接3-5次，可在配置区修改

### 使用方法
首先请在 https://platform.deepseek.com/ 中注册或登录账户，充值后在API Keys处申请Key，复制后在code.js中替换为配置区中的有效Key  (通常以sh-开头)

复制到油猴新插件中即可使用，具体方法与原项目大体相同  (https://www.kamiwzw.site/posts/bilibili-favorites-ai-organizer-userscript/)

如果您的网络环境不佳，请尝试适当在配置去中调高 MAX_RETRIES 以提高重复尝试次数

如果ai在某个收藏夹的分类中频频犯蠢，我们建议您在错误集中的收藏夹中进行二次分类，放心，如果内容于该收藏夹匹配，视频是不会被
移走的

如果您在使用过程中有疑问，我们跟推荐您去寻求AI的帮助，建议复制好控制台输出原文和源代码
