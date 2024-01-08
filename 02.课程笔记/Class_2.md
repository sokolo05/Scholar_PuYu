# 大模型及 InternLM 模型简介
## 1. 大模型介绍
- 大模型：借助大量数据训练，拥有数十亿甚至数千亿参数的模型
- 产生缘由：海量数据量的增长 + 计庞大计算能力的提升 + 多种AI算法优化发展
- 具体应用：自然语言处理（NLP）、计算机视觉（CV）、语音识别等
- 常用网络结构：Transformer、BERT、GPT（ Generative Pre-trained Transformer ）等
- 优势：捕捉和理解数据中更为复杂、抽象的特征和关系；大规模参数学习，提高应用任务上的泛化能力；多种实验任务上表现能力突出
- 存在问题：计算资源需求较高、训练成本高昂、依赖海量的大规模数据、可解释性差等
- 最新权衡角度：性能、成本、伦理道德
## 2. InternLM 模型全链条开源
- InternLM：支持大模型训练而无需大量的依赖的开源轻量级训练框架，支持在拥有数千个 GPU 的大型集群上进行预训练，并在单个 GPU 上进行微调，同时实现了卓越的性能优化。
- 上海人工智能实验室发布的开源预训练模型：InternLM-7B 和 InternLM-20B
- Lagent：轻量级、开源的基于大语言模型的智能体（agent）框架，支持快速转换大语言模型为多种类型的智能体。Lagent 框架可以更好的发挥 InternLM 的全部性能。
- 浦语·灵笔：基于书生·浦语大语言模型研发的视觉-语言大模型，提供出色的图文理解和创作能力，结合了视觉和语言的先进技术，能够实现图像到文本、文本到图像的双向转换。
# - 本节课共学习了三个模型Demo：
## 1. nternLM-Chat-7B 智能对话 Demo
### 1. 终端窗口Demo
 ![终端窗口Demo](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E6%99%BA%E8%83%BD%E5%AF%B9%E8%AF%9D_Demo_1.png)
- 输入“你认识毛泽东吗”—>他给不出来答复，因为默认我问他的是深度了解毛泽东，所以没有给出正确的答复
### 2. web demo 运行
 ![web demo 运行](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E6%99%BA%E8%83%BD%E5%AF%B9%E8%AF%9D_Demo_3.png)
-   输入“毛泽东是谁”—>他给出了毛泽东的人物简介
-   它还可以实现数学计算：7乘7等于49
 ![小文章生成](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E6%99%BA%E8%83%BD%E5%AF%B9%E8%AF%9D_%E5%B0%8F%E6%95%85%E4%BA%8B2.png)
- 帮忙写一个关于排球的故事—>介绍了一个女孩，打排球过程中遇到的问题，从被人敬佩到因伤病被人质疑，困难面前积极态度赢得一场场比赛胜利，自己也成了球队核心，也显示了排球团队合作竞赛的重要性。
## 2. Lagent 智能体工具调用 Demo
### web demo 运行
 ![](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E6%99%BA%E8%83%BD%E4%BD%93%E5%B7%A5%E5%85%B7%E8%B0%83%E7%94%A8_Demo_2.png)
- 已知2*x+3=10，求x —> 直接给出了计算的python程序以及计算结果和过程
## 3. 浦语·灵笔图文理解创作 Demo
### - 1.创造图文并茂文章
![洛阳美景](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E5%9B%BE%E6%96%87%E7%90%86%E8%A7%A3%E5%88%9B%E4%BD%9C_Demo_3.png)
- 输入“洛阳美景” —> 先介绍了洛阳，但是给出洛阳地理位置图有问题（地理位置显示是：遵义，查了一下雒城是四川现在的广汉市，但是显示位置也不对，问题出在哪里不知道），后边的几个图片是洛阳的美景图，显示正确。
### - 2.多模态对话
![排球运动](https://github.com/sokolo05/Scholar_PuYu/blob/main/01.%E8%AF%BE%E7%A8%8B%E4%BD%9C%E4%B8%9A/%E5%9B%BE%E7%89%87/%E5%9B%BE%E6%96%87%E7%90%86%E8%A7%A3%E5%88%9B%E4%BD%9C_Demo_4.png)
- 输入图像：排球扣球运动
- —> 1.什么运动（排球）✔
- 2.图中借个人（3个人，背景区域的观众不计入人数）✔
- 3. 图中属于排球哪个技术（扣球，其实还有拦网，没识别，我琢磨着是因为只看正脸，回头找个拦网的视频试一下）✔
# 课程收获
1. 重新温习了一下pip、conda 换源的操作设置
2. 学会了三个Demo的运行、配置和web交互设置
3. 掌握了如何配置本地端口
4. 借助镜像下载Hugging Face以及其他几个模型
# 其它知识
## ssh命令
### 1. 指令：
   ```
   ssh -CNg -L 6006:127.0.0.1:6006 root@ssh.intern-ai.org.cn -p 33383
   ```
### 2. 参数介绍：
   ```
   ssh：SSH 客户端命令。
   -C：启用压缩功能，减少传输数据量
   -N：不执行远程命令，仅用于端口转发
   -g：允许远程主机连接到本地转发的端口
   -L：指定本地端口转发规则
   ```
### 3. 连接信息介绍：
   ```
   6006:127.0.0.1:6006：本地端口 6006 映射到远程服务器的 127.0.0.1 的端口 6006
   root@ssh.intern-ai.org.cn：登录远程服务器的用户名为 root，服务器地址为 ssh.intern-ai.org.cn
   -p 33383：指定 SSH 连接的端口号为 33383
   ```
## Hugging Face下载
### 1. 指令：
    export HF_ENDPOINT=https://hf-mirror.com
