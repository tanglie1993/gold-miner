> * 原文地址：[What It Was Like to Write a Full Blown Flutter App](https://hackernoon.com/what-it-was-like-to-write-a-full-blown-flutter-app-330d8202825b)
> * 原文作者：[Nick Manning](https://hackernoon.com/@seenickcode?source=post_header_lockup)
> * 译文出自：[掘金翻译计划](https://github.com/xitu/gold-miner)
> * 本文永久链接：[https://github.com/xitu/gold-miner/blob/master/TODO1/what-it-was-like-to-write-a-full-blown-flutter-app.md](https://github.com/xitu/gold-miner/blob/master/TODO1/what-it-was-like-to-write-a-full-blown-flutter-app.md)
> * 译者：
> * 校对者：

# 写一个完整的 Flutter App 是什么感觉

![](https://cdn-images-1.medium.com/max/800/1*SZK7j8dPQuaecmaeJoWxwA.jpeg)

**更新**: 我将会放出一个新的 Flutter 课程，名为 Practical Flutter。它将在 18 年 七月底开始。如果你想收到通知， [点击这里](https://mailchi.mp/5a27b9f78aee/practical-flutter)。 🚀

今天早上我吃了两顿早饭，因为我需要发动所有的写博客用的脑力。从[我的上一个帖子](https://codeburst.io/why-flutter-will-take-off-in-2018-bbd75f8741b0) 以后，我有了很多想说的话，所以我们开始吧。

我非常激动，因为我可以正式继续写关于 Flutter 的文章了，因为我即将把我的第一个 Flutter app 放出到 iOS 和 Android 商店——只有一两周了！因为我在空闲时间里一直在写这个 app，所以在过去几个月我一直拒绝被打扰。

**自从 Ruby on Rails 或 Go 以来，我从没有因为一个技术而这么激动过。** 在花了好几年深入学习 iOS app 开发之后，我因为对 Android 非常不熟悉而感到不爽。而且，以前的那些跨平台开发框架都很难吸引我。

比如在两年前，前往跨平台 app 开发的聚会，我会觉得那些东西都很不正规、不稳定、开发者体验糟糕、难以使用，或者最近一两年都没法用。

我刚刚完成第一个 Flutter app，并感到我可以长期安全地向这个框架投入更多的时间。写一个 app 是对一个框架最后的检验，而 Flutter 通过了这个检验。能够熟练地开发 iOS 和 Android app 令我感到惊喜。我也很喜欢服务端的开发与扩容，而 [我的妻子 Irina](https://www.behance.net/irinamanning) 是一名用户体验设计师，所以这是一个强大的组合。

**这篇博文将会很长，因为它包括很多内容：**

1.  **我关于把 iOS app 迁移到 Flutter 的经验**
2.  **目前为止关于 Flutter 的想法**
3.  **对 Google 团队的建议**

我决定尽快写下我的想法，以便尽快继续写教程（以及更多的 app！）。

### 1. 把 iOS 应用迁移到 Flutter

自从我的上一个 [关于 Flutter 的帖子](https://codeburst.io/why-flutter-will-take-off-in-2018-bbd75f8741b0) 以来，我感觉合乎逻辑的下一步是真正深入地学习 Flutter。我非常喜欢久经考验、有端到端的实例的教程 (think Digital Ocean 或者甚至 Auth0 教程)。端到端，细致的，高质量的例子一直是新技术吸引我的方式，因为我可以看到基本能够正式上线的代码，并且确信我在使用正确的方式实现功能。我也想做同样的事，所以我决定写 Flutter 的教程。

有了这些目标之后，我决定最适合我的 app 是重写一个我已经发布到 App store 上的 iOS app。 Steady Calendar ([homepage](https://www.steadycalendar.com), [Product Hunt](https://www.producthunt.com/posts/steady-calendar)), 是一款 [我的妻子 Irina](https://www.behance.net/irinamanning) 和我设计和开发的习惯养成器。我们是在几年前生活在柏林时开发的。从那时候以来，这个产品使我们为设计、实现和发布帮助他人养成健康习惯的产品而着迷。

把这个 iOS app 迁移到 Flutter 花了我一到两个月的空闲时间。这使我可以毫无压力地写出优秀的 Flutter 教程。

很酷的是我可以把以下内容包括在我的教程中，因为我在 app 中实现了它们：
      
*   登录之前的介绍。
*   Facebook / email 注册与登录。
*   展示日历的网格 view ，用户可以在完成一个目标之后高亮某一天。
*   iOS 与 Android 用户都熟悉的跨平台表单。
*   使用 [Scoped Model](https://pub.dartlang.org/packages/scoped_model) 的 Redux 风格的状态管理。
*   具有栈、定位元素、图像和按钮的自定义 UI。
*   列表 view。
*   简单、多语言、国际化的 UI。
*   跨平台导航栏，同样是 iOS 和 Android 用户都很熟悉的。
*   具有全局样式的控件。
*   集成测试。
*   把 app 提交到 Apple 应用商店。
*   把 app 提交到 Google Play 商店。

### 2. 目前为止关于 Flutter 的想法

我已经在后端和 webapp 开发方面有了 17 年以上的经验，其中的 4 年我重度参与了 iOS 开发，并且在上一年，我需要花很多的工作时间在React Native 上 (去年也发布了一些 React 项目）。

**以下是在学习 Flutter 时出现的想法：**

1.  **开发者体验**, 开发者的团体精神和给我的支持十分惊人。从 Stack Overflow， Google Groups 到博文的所有东西质量都很高，因为人们对 Flutter 非常有热情。 Google 工程师在日常工作之外，还愿意花很多时间在 Google Groups 上回答问题，这就形成了一个了不起的社区。他们在和 各种背景的工程师合作时表现得非常礼貌、非常专业，而其他很多公司就不见得是这样。开发者社区非常热闹，成员们非常积极，并提供深思熟虑的答案。文档也非常出色  There’s also a lively community where members are super active and provide really thoughtful answers. Documentation is fantastic. The libraries are very stable and with Flutter being based on Dart, a language that’s been around for years, learning is very easy as it is more established and battle tested. All around, great developer experience.
2.  As expected, there there is less **availability of third party libraries written in Dart**. Yet these are not deal breakers, at least in my experience. **95% of the features I’ve needed to use were there and available**, just one exception was say, some third party integration with a popular analytics tool but nothing that a simple HTTP wrapper could take care of.
3.  **Material Design widgets**, something that the Flutter framework is heavily comprised of, is great for cranking out simple apps yet for professional, cross-platform apps, it will alienate iOS users. I cannot present Material Design widgets to my iOS users because it would make my app look alien to them. Flutter does indeed provide its own set of iOS widgets, but these still have a way to go in terms of comprehensiveness. Luckily, with the Steady app I wrote, most of the UI was already custom. But for things like forms, that was more of a challenge. So at the end of the day, the documentation, examples and overallFlutter SDK is heavily oriented around Material Design which is great but there needs to be more of a balance for folks like me.
4.  **Developing custom UIs in Flutter was a breeze**. I have high standards too after being spoiled by leaning CocoaTouch / iOS back in the day. After diving through lots of Flutter code and judging by the experience of writing customer UIs, the **Google team really has their act together**. Sure, there are some widgets I really think are super overkill and can make the learning curve a bit more convoluted (i.e. the Center widget), but it’s not a huge deal. After writing a real app one quickly starts to see a pattern of what the most critical widgets they’d probably be using on a regular basis (and hey, I’ll be covering that in my future tutorials).
5.  As an iOS user, taking a few months to write my original iOS app Steady Calendar, **I’ll never forget the sheer excitement of running it for the first time on a physical Android device**. I guess it’s just because I always was super turned off by other cross platform mobile frameworks. If you take months of your spare time, lots of hard work developing something and realize you can run it on two major platforms, you will get hooked. This is probably not very insightful feedback for most people but I needed to share it anyway!
6.  **Writing cross platform apps will throw more design challenges your way** but this hasn’t really anything to do with Flutter itself but more to do with getting into development for multiple platforms. When you plan out a Flutter app, make sure you have a good designer and a nice custom UI mocked up or be ready to write your Flutter app so that your code conditionally uses either Material Design or Cupertino widgets. In the former case though, this is less of a Flutter issue and more of a challenge writing cross platform apps, you need to make sure the UI is designed to be good looking for Android users and iOS users based on the conventions they are each used to.
7.  **Dart is a pure pleasure to learn and use**. I love the stability and reliability I get vs using something like TypeScript or Flow. To put this into context, I have a bit of a React background and have been learning React Native heavily for my day job (heavily) for the past few months. I’ve also worked a lot with Objective-C and then Swift for years. Dart is a breath of fresh air because **it doesn’t try to be overly complex and has a solid core library and packages**. Honestly, I think even high school freshmen can use Dart for basic programming. I just can’t believe how many I hear complaining they’d have to learn a new language, which for Dart would take between one or two hours or a day max.
8.  **Flutter rocks.** It’s not perfect by any means, but in my own opinion, the learning curve, ease of use, tools available make it by far a nicer experience than other mobile frameworks I’ve used in the past.

### What Google Should Do

1.  Google team members and friends should to **continue to provide thoughtful, friendly and responsive support** in its Google Groups. This is a big plus and is what makes the framework standout in terms of approachability and support. The team supporting and cultivating the community are **really likable guys and have a good, positive attitude and that’s huge.**
2.  Get a poll from community members to see which Widgets may simply not be useful. **For the not so useful Widgets, just remove them from documentation tutorials** or deprecate them altogether. For example, the ‘Center’ widget is nice for a Hello, World container but I never understood it. Why can’t ‘Container’, something that’s way more prevalent have a property to do the same thing? This is a super trivial example but I think that’s part of the reason why Go was so successful, because it’s core library was simple and lean (and stayed lean).
3.  **Devote more focus on iOS users.** Material Design is great to get going quickly or if you’re only building something for Android users. I’d never use Material Design in an iOS app. With that said, I’ve found Flutter to be a nicer, less complex developer experience than learning Swift and all the one million library features one has to know to write iOS apps nowdays. I think a lot of iOS users would love to learn Flutter if Flutter had just even a bit more iOS style widgets.
4.  **More tutorials** on building realistic features and screens. I’d love to see more tutorials like this one: [https://flutter.io/get-started/codelab/](https://flutter.io/get-started/codelab/) but also “end to end” ones, where an example of integration with a backend is shown.
5.  **Theming apps** should be **less focused on Material Design**. Again, I don’t want to use the ‘MaterialApp’ widget if I’m writing an iOS app. Theming seems tightly coupled to this and it should be more generic.
6.  **Less prevalence of Firebase in the documentation** or pushing it so often. I realize Firebase really useful to get going fast and it helps bolster the approachability for new developers, but a significant amount of folks out there already have a backend ready or would not ever consider using Firebase. So I think more emphasis on how to work with simple web services and JSON would help. I had to read a lot of third party tutorials on this because I felt the documentation wasn’t realistic enough. I can elaborate when I write a future blog post about this.

So far, I’m super happy with Flutter overall.

Next, I’m going to consider re-writing another iOS I have in the app store, [www.brewswap.co](http://www.brewswap.co) that’s more complex (Tinder-style photo swiping, real time chat, etc).

So far, those are the main takeaways I can think of for now. Like any framework, there are a lot of quirks and learning curve issues but really overall, **Flutter is something I feel like I can really invest in and most importantly, really enjoy using**.

Stay tuned for some initial Flutter tutorials and I hope I was able to give some insight for anyone considering making the investment in Flutter — I’d say, go for it!

For anyone with questions on insight, etc, it’s better to just [**ping me on Twitter**](https://twitter.com/seenickcode) **@seenickcode.**

**UPDATE**: [Sign up](https://mailchi.mp/5a27b9f78aee/practical-flutter) and get notified about my upcoming Flutter course, Practical Flutter. 🚀

Happy Fluttering.

> 如果发现译文存在错误或其他需要改进的地方，欢迎到 [掘金翻译计划](https://github.com/xitu/gold-miner) 对译文进行修改并 PR，也可获得相应奖励积分。文章开头的 **本文永久链接** 即为本文在 GitHub 上的 MarkDown 链接。


---

> [掘金翻译计划](https://github.com/xitu/gold-miner) 是一个翻译优质互联网技术文章的社区，文章来源为 [掘金](https://juejin.im) 上的英文分享文章。内容覆盖 [Android](https://github.com/xitu/gold-miner#android)、[iOS](https://github.com/xitu/gold-miner#ios)、[前端](https://github.com/xitu/gold-miner#前端)、[后端](https://github.com/xitu/gold-miner#后端)、[区块链](https://github.com/xitu/gold-miner#区块链)、[产品](https://github.com/xitu/gold-miner#产品)、[设计](https://github.com/xitu/gold-miner#设计)、[人工智能](https://github.com/xitu/gold-miner#人工智能)等领域，想要查看更多优质译文请持续关注 [掘金翻译计划](https://github.com/xitu/gold-miner)、[官方微博](http://weibo.com/juejinfanyi)、[知乎专栏](https://zhuanlan.zhihu.com/juejinfanyi)。
