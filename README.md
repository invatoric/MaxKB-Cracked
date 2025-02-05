# MaxKB Cracked Edition
去除了所有数量限制的MaxKB社区版\
（由于本人技术原因，没有去除限制代码，而是改成了一个极大值（反正是你一辈子都用不完的））

---
[English](README_EN.md) | [中文](README.md)

<p align="center"><img src= "https://github.com/1Panel-dev/maxkb/assets/52996290/c0694996-0eed-40d8-b369-322bf2a380bf" alt="MaxKB" width="300" /></p>
<h3 align="center">基于大语言模型和 RAG 的知识库问答系统</h3>
<p align="center"><a href="https://trendshift.io/repositories/9113" target="_blank"><img src="https://trendshift.io/api/badge/repositories/9113" alt="1Panel-dev%2FMaxKB | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a></p>
<p align="center">
  <a href="https://www.gnu.org/licenses/gpl-3.0.html#license-text"><img src="https://img.shields.io/github/license/1Panel-dev/maxkb?color=%231890FF" alt="License: GPL v3"></a>
  <a href="https://app.codacy.com/gh/1Panel-dev/maxkb?utm_source=github.com&utm_medium=referral&utm_content=1Panel-dev/maxkb&utm_campaign=Badge_Grade_Dashboard"><img src="https://app.codacy.com/project/badge/Grade/da67574fd82b473992781d1386b937ef" alt="Codacy"></a>
  <a href="https://github.com/1Panel-dev/maxkb/releases/latest"><img src="https://img.shields.io/github/v/release/1Panel-dev/maxkb" alt="Latest release"></a>
  <a href="https://github.com/1Panel-dev/maxkb"><img src="https://img.shields.io/github/stars/1Panel-dev/maxkb?color=%231890FF&style=flat-square" alt="Stars"></a>    
  <a href="https://hub.docker.com/r/1panel/maxkb"><img src="https://img.shields.io/docker/pulls/1panel/maxkb?label=downloads" alt="Download"></a>  
</p>
<hr/>

MaxKB = Max Knowledge Base，是一款基于大语言模型和 RAG 的开源知识库问答系统，广泛应用于企业内部知识库、客户服务、学术研究与教育等场景。

- **开箱即用**：支持直接上传文档 / 自动爬取在线文档，支持文本自动拆分、向量化和 RAG（检索增强生成），有效减少大模型幻觉，智能问答交互体验好；
- **模型中立**：支持对接各种大模型，包括本地私有大模型（Llama 3 / Qwen 2 等）、国内公共大模型（通义千问 / 腾讯混元 / 字节豆包 / 百度千帆 / 智谱 AI / Kimi 等）和国外公共大模型（OpenAI / Claude / Gemini 等）；
- **灵活编排**：内置强大的工作流引擎和函数库，支持编排 AI 工作过程，满足复杂业务场景下的需求；
- **无缝嵌入**：支持零编码快速嵌入到第三方业务系统，让已有系统快速拥有智能问答能力，提高用户满意度。

## 快速开始

```
docker run -d --name=maxkb --restart=always -p 8080:8080 -v ~/.maxkb:/var/lib/postgresql/data -v ~/.python-packages:/opt/maxkb/app/sandbox/python-packages cr2.fit2cloud.com/1panel/maxkb

# 用户名: admin
# 密码: MaxKB@123..
```

- 你也可以通过 [1Panel 应用商店](https://apps.fit2cloud.com/1panel) 快速部署 MaxKB + Ollama + Llama 3 / Qwen 2，快速上线基于本地大模型的 AI 知识库问答系统；
- 如果是内网环境，推荐使用 [离线安装包](https://community.fit2cloud.com/#/products/maxkb/downloads) 进行安装部署；
- 你也可以在线体验：[DataEase 小助手](https://dataease.io/docs/v2/)，它是基于 MaxKB 搭建的智能 AI 问答系统，已经嵌入到 DataEase 产品及在线文档中；
- MaxKB 产品版本分为社区版和专业版，详情请参见：[MaxKB 产品版本对比](https://maxkb.cn/pricing.html)。

如你有更多问题，可以查看使用手册，或者通过论坛与我们交流。

- [使用手册](https://maxkb.cn/docs/)
- [演示视频](https://www.bilibili.com/video/BV1BE421M7YM/)
- [论坛求助](https://bbs.fit2cloud.com/c/mk/11)
- 技术交流群

<image height="150px" width="150px" src="https://github.com/1Panel-dev/MaxKB/assets/52996290/a083d214-02be-4178-a1db-4f428124153a"/>

## UI 展示

<table style="border-collapse: collapse; border: 1px solid black;">
  <tr>
    <td style="padding: 5px;background-color:#fff;"><img src= "https://github.com/1Panel-dev/MaxKB/assets/52996290/d87395fa-a8d7-401c-82bf-c6e475d10ae9" alt="MaxKB Demo1"   /></td>
    <td style="padding: 5px;background-color:#fff;"><img src= "https://github.com/1Panel-dev/MaxKB/assets/52996290/47c35ee4-3a3b-4bd4-9f4f-ee20788b2b9a" alt="MaxKB Demo2"   /></td>
  </tr>
  <tr>
    <td style="padding: 5px;background-color:#fff;"><img src= "https://github.com/user-attachments/assets/9a1043cb-fa62-4f71-b9a3-0b46fa59a70e" alt="MaxKB Demo3"   /></td>
    <td style="padding: 5px;background-color:#fff;"><img src= "https://github.com/user-attachments/assets/3407ce9a-779c-4eb4-858e-9441a2ddc664" alt="MaxKB Demo4"   /></td>
  </tr>
</table>

## 技术栈

- 前端：[Vue.js](https://cn.vuejs.org/)
- 后端：[Python / Django](https://www.djangoproject.com/)
- LangChain：[LangChain](https://www.langchain.com/)
- 向量数据库：[PostgreSQL / pgvector](https://www.postgresql.org/)
- 大模型：各种本地私有或者公共大模型

## 飞致云的其他明星项目

- [1Panel](https://github.com/1panel-dev/1panel/) - 现代化、开源的 Linux 服务器运维管理面板
- [JumpServer](https://github.com/jumpserver/jumpserver/) - 广受欢迎的开源堡垒机
- [DataEase](https://github.com/dataease/dataease/) - 人人可用的开源数据可视化分析工具
- [MeterSphere](https://github.com/metersphere/metersphere/) - 新一代的开源持续测试工具
- [Halo](https://github.com/halo-dev/halo/) - 强大易用的开源建站工具

## License

Copyright (c) 2014-2024 飞致云 FIT2CLOUD, All rights reserved.

Licensed under The GNU General Public License version 3 (GPLv3)  (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

<https://www.gnu.org/licenses/gpl-3.0.html>

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
