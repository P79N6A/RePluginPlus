# RePluginPlus
RePlugin扩展，方便使用



安卓开发领域，有关插件化的讨论一直热度不减。目前市面上的插件化方案虽然很多，但多数只能实现某些功能的插件化，距离开发者的预期尚有相当差距。对此，在近期GMTC全球移动技术大会上，360手机卫士主程序架构负责人张炅轩宣布，360的插件化框架RePlugin已经可以实现“全面插件化”，同时具有出色的稳定性和灵活性，可适用于各种类型的应用上。

“RePlugin预计7月份开源，这将是我们献给安卓世界最好的礼物。”此言一出，引发全场沸腾。

三大因素制约  使用插件化的开发者不足5%

安卓应用插件化的优势众所周知，然而张炅轩在GMTC上的调查结果却让人大跌眼镜。在参会200多位安卓开发者中，仅有不足5%的比例，使用了插件化方案。超过九成的开发者，目前上没有将插件化应用在软件开发之中。

360手机卫士通过各渠道的调查发现，有三大挑战制约了插件化在安卓开发界的普及。

首先是不够稳定。目前有很多比较灵活的插件化框架，虽然支持特性众多，但因Hook点较多，所以不是非常稳定。因此很多大型项目不是很愿意用它们来开发插件，担心出现应用崩溃、插件无法正常使用等问题。

其次是不够灵活，有一些相对稳定的插件化框架，又存在“不够灵活、自由”的问题，一旦插件有特别大的改动，如新增一个Activity、Service、进程等，就需要主程序发版，更不用说能做到“一年前的主程序，无需升级，可以用新插件和组件”的目标了。

最后就是插件化框架仅在功能丰富的大型项目中，才被考虑使用，且多用于边缘功能。目前几乎所有App在使用插件化框架时，都是将自己的一些“比较边缘的”模块作为插件，比如“红包”、“天气”、“摇一摇”等，他们认为只有“非核心”模块，才会考虑做成插件。这也使得插件化的应用范围非常狭窄。

总而言之，现在很多市面上插件化方案，没有很好解决稳定、灵活和自由等方面的问题，因此始终没有被广泛使用。

将Hook点降低为1   让“核心功能皆为插件”

“只有让核心功能实现全面插件化，才能真正让插件化方案走向普及”，张炅轩在GMTC表示，“要实现这个目标，必须先实现优异的稳定性，继而确保出色的灵活性。”

据介绍，360手机卫士团队早在2013年，就推出了卫士插件化框架，在2014年又发布了卫士完整占坑方案，2016年实现了“核心功能皆为插件”的目标，并将其命名为RePlugin。在整个过程中，卫士团队很好解决了“稳定”和“灵活”的平衡难题，破解了“只有功能丰富的项目才用”的“魔咒”，目前已经有数亿台设备使用了卫士的插件化方案。

在稳定性方面，RePlugin的Hook点只有一处：ClassLoader，这使得框架崩溃率仅为万分之一。而在灵活性方面，由于RePlugin采用了全新、独创的“分层坑位方案”，加上一些其它独创新特性，如多进程坑位、Task-Affinity坑位等，从而真正实现了插件组件任意增改、新插件直接用、无须主程序发版、自有设置进程等特性，而独创的“动态编译方案”，能极大的提高插件开发者的研发效率，真正做到“只需几行代码，就能‘秒变’插件”的神奇效果。

![RePlugin对比](/img/img_1.png)

图1：卫士RePlugin各项指标全面领先行业

值得一提的是，手机卫士团队将业界公认非常复杂的桌面应用，变成了插件，在卫士插件化框架中完美的运行，且能做到非常出色的稳定和灵活。这让在场嘉宾倍感惊叹，充分体现了RePlugin插件化方案的领先优势。

多个亿级APP已采用 RePlugin预计七月开源

截止目前，RePlugin的插件数已达102个，核心基础插件57个，而插件占应用比更是达到了惊人的83%，而且年发版次数高达596次，平均每个工作日发版2-3次。目前360公司几乎所有的亿级用户量的APP，以及多款主流第三方APP，都采用了卫士RePlugin插件化方案。为了让更多第三方应用享受到插件化方案带来的便利，张炅轩在GMTC2017上正式宣布，将对RePlugin实现全面开源，并将此称为“献给安卓世界的最好礼物”。

![RePlugin插件](/img/img_1.png)

图2: RePlugin插件占应用比达到83%

作为国内市场占有率最大、累计拥有10亿用户的手机端安全防护软件，360手机卫士近年来不断在提升用户体验方面发力，在夯实清理加速、骚扰拦截、软件管理、手机杀毒这些核心功能之外，在插件化开源等领域一直在深入探索，最终推出了兼顾稳定和灵活、更加成熟可靠的RePlugin方案。本次宣布代码开源，对安卓开发无疑具有非常深远的意义，对于广大APP 开发者无疑是一个福音。分析人士认为，这将在安卓界掀起一场“全面插件化”的趋势，让众多应用从RePlugin的开源中受益。

GMTC全球移动技术大会是由InfoQ主办的全球顶级技术盛会。大会关注移动、前端、跨平台、AI应用等多个技术领域，旨在促进全球技术交流，推动国内技术升级，目前正成为面向移动开发、前端、AI技术人员，聚焦前沿技术及实践经验，打造技术人员的学习和交流平台。360手机卫士团队此次的分享引来与会者一致赞誉。