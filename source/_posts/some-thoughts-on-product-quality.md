---
title: 对产品质量的一点思考
date: 2019-07-01 06:44:41
categories: [经验总结]
tags: [经验总结]
---

不管是做产品还是做项目，也不管是采用瀑布模型还是敏捷开发，我们都有一个终极目标，就是能按时交付质量可靠的功能，其中质量尤为重要。

本文是我对产品质量的一点思考，如果您所在的团队代码质量很高，很少出BUG，那么可以私信我，我们可以交流下关于代码质量的一些问题。

<!--more-->

## 小公司面临的问题

大公司里每个人指责分明，团队的人员配置也比较齐全，有完整的开发流程，流程也会不断的迭代优化，每个环节只要按照流程严格去执行，基本不会出什么大的问题。但不是每个人都能够进入到大公司，或者说会一直待在大公司，如果您是在中小公司，可能会有下面一些情况：

* 没有专职的需求分析人员，没有专职的测试人员，很多时候是一岗多职
* 没有不急的项目，客户永远说的都是越快越好
* 虽然说唯一不变的就是变化，我们需要拥抱变化，但常常会即便拥有一双长臂，也无力拥抱
* 需求来了，直接写代码，后期补文档
* 代码中基本不写单元测试
* 没有自主研发的需求管理平台

为什么会有上面的问题，我觉得很重要的一个原因是成本问题，专职需求分析需要人力成本，写单元测试、文档等需要时间成本，等等。短期看来是节省了成本，但从长远来看，会导致质量下降，最终会得不偿失，如果您是做项目，打一枪换个地方，我不做评价，如果是在不断地迭代成品，那么就要停下来好好思考下了。

## 我们的现状

10人左右的团队，需要做的事情如下：

* 需求分析
* Vue前端开发
* dotNetCore后端开发
* H5、小程序、iOS、安卓
* 测试
* 运维

上面说到，在小公司会是一岗多职，我们也不例外，大概任务分配如下：

* 全员做需求分析，即便是新手，也要求做简单需求的分析
* 后端工程师除了iOS和安卓不做，其他的都做
* iOS和安卓工程师除了后端不做，其他都做
* 只有一两个只做纯前端的工程师

目前来看，整个团队是偏全栈的，全栈的团队理论上效率会很高，的确，效率从来都不是我担心的问题，但质量问题却一直都没能很好的解决：

* 开发人员还是更喜欢写代码，文档能力偏弱，虽然目前强制规定每个所做的需求在语雀上要写对应的需求文档，但很多时候写不到点子上，关联影响点也没有分析，给测试提供不了很好的支撑
* 文档写不好，加上开发者的思维，很多低级问题在自测阶段不能被发现
* 经常改了A模块的一个问题，引发其他模块的几个问题
* 同样的问题会反反复复出现

## 怎样解决质量问题

### 取舍和平衡

我认为软件开发其实是在时间、范围、稳定性和代码质量上做博弈：

* 时间：交付一个功能的期限，比如老板说3个月要上线某功能
* 范围：需要实现功能的边界
* 稳定性：随着版本的不断更新，用户使用产品的一个最直观的感受
* 代码质量：代码是否是可复用，易于维护的，用户不能直观感受，但也同样重要

领导总是会说，这个时间节点非常重要，或者重要客户，不能延后，等等，总之时间节点后延的可能性不大。

稳定性也不能出问题，轻则客户满意度降低，重则会造成事故，给客户带来严重损失，客户可能因此就丢了。

所以只能在范围和代码质量上做取舍：

* 本来应该三个月做的任务，非要压缩到一个月，那只能去和领导沟通，将一些不重要，或者不紧急的任务放到下一阶段完成
* 如果范围也不能压缩，那就只能舍弃代码质量了，怎么快怎么来，但也因此欠下了一个技术债，债是需要偿还的，也是有利息的，还的越迟，利息越多。

### 自动化测试

自动化测试分为两个部分，构建之前的单元测试和构建之后的端到端测试

* 单元测试又分为前端Vue的单元测试和dotNetCore的单元测试，在一个已成型的产品中去加单元测试是很困难的，所以只能先找一些关键点，经常出问题的点去尝试
* 端到端的测试我们采用TestCafe，反复出问题的地方，就提炼出来一种业务场景，有针对性地去写测试代码

配合Jenkins，做到测试的自动化，那是不是有了自动化测试就能高枕无忧了呢？并不是，我觉得更重要的是，每个人员对产品要有深入的理解，对所做的需求要能完全掌握，对关联影响点的分析要没有任务遗漏。

测试只是手段而不是目的，我们的目的是写出好的代码，交付出无缺陷的功能。

## 总结

没有任何的方法论是可以生搬硬套的，只有不断的去学习、吸收、结合现有资源进行实践、不断的重复这个过程，直到找到一种适合自己团队的落地方案。

改善质量的道路任重而道远，不断地去尝试，去实践总会有些效果的。

您所在的团队又是怎么样来保证质量的呢？欢迎讨论。
