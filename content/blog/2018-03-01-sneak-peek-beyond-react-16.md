---
title: "Sneak Peek: Beyond React 16"
author: [sophiebits]
---

我们团队成员 [Dan Abramov](https://twitter.com/dan_abramov) 刚刚在 [JSConf Iceland 2018](https://2018.jsconf.is/)，就我们正在着手做的一些 React 新的功能特性发表了演讲。这次演讲以一个问题开场："在计算能力和网速存在巨大差异的背景下，我们怎样才能给每个人带来最好的用户体验？"

这是 JSConf Iceland 提供的[视频](https://www.youtube.com/watch?v=v6iR3Zk4oDY)。

<br>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/nLF0n9SACd4?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

若果你现在停下本文的阅读去看视频，我觉得你一定会更加喜欢这个演讲视频。但是如果你没有时间观看，下面是对这次演讲的一个（非常）简要的总结。

## 关于两个演示 {#about-the-two-demos}

第一个演示中，Dan 说道： "我们已经构建了一种通用的方法来确保高优先级的更新不会被低优先级更新所阻塞，这种技术叫时间分片。如果我的设备足够快，感觉就像是同步的；如果我的设备很慢，我们仍然能感觉到应用在积极响应我们的操作。这多亏了 [requestIdleCallback API](https://developers.google.com/web/updates/2015/08/using-requestidlecallback) 使得应用可以适应不同配置的设备。需要注意的是只有最终状态被渲染出来了，屏幕的渲染始终保持一致，并没有让我们感觉到渲染速度很慢，从而导致用户体验不佳。"

在第二个演示中，Dan解释说："我们已经构建了一种通用的方法，让组件在加载异步数据时暂停渲染，这就是我们所说的 **suspense**。你可以暂停任何状态更新，直到数据准备就绪，并且可以将异步加载添加到组件树中的任何组件，而无需通过应用管理所有属性和状态，避免增加逻辑复杂度。在网速很快的情况下，更新显示非常流畅且瞬时，不会让我们看着一堆恼人的加载图标转来转去最后消失。当网速慢的时候，你可以专门设计一下用户应该看到哪些加载状态，以及它们应该呈现的粒度，而不是根据你写的代码的来决定显示什么 spinner。让程序始终保持响应。"

"重要的是，这仍然是你了解的那个 React。这仍然是那个声明式的组件化的你喜欢的 React。"

我们已经迫不及待地想在在今年晚些时候发布这些新的异步渲染功能。请在 Twitter 上关注 [@reactjs](https://twitter.com/reactjs) 以获取更新。
