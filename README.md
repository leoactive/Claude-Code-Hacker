# Claude-Code-Hacker
Claude Code 实用技巧

## 如何拯救你的上下文？

不断要求Claude启动Sub Agent来完成任务，如果任务比较特殊，你可以要求Master Agent行动前，给你审阅它发送给Sub Agent的提示词内容。

## 如何管理压缩？答案就是不压缩。

在Claude配置文件中设置【关闭压缩】然后随便用，打完20万上下文。（什么？关闭压缩？这种邪事你也敢干？）

上下文用完后，使用/export命令导出Claude Code TUI渲染出的整个Session的文本——放心没有20万上下文那么多，因为其中的文件写入、工具调用吞吐，都不在TUI上显示。

重点来了：/clear 清空上下文，将导出的文件名发给新Session的Claude，然后对它说：这是我们上一个Session的对话内容，请你发起Sub Agent，以能够让你在这个全新的Session中继续无缝工作为目标，构建交接文档，并且请你读取交接文档。

如果你忘记了/export，可以使用/resume命令，回到上次的Session，然后执行/export/。
