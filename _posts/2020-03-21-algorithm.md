---
layout: post
title: "OS learning"
date: 2020-03-21 01:13:14
image: '/assets/img/'
description: 'Algorithm learning note'
tags:
- algorithm
categories:
- Backend
twitter_text: 'Do you know these?'

---

## Everyday sentence

11-29: I don't like rasins. They used to be fat and jucy, and now they are twisted. They had their lives stolen. They taste sweet, but really they are humiliated grapes.

12-1: We all fear death and question our place in the universe. The artist's job is not to succumb to despair, but to find an antidote for the emptiness of existence.

12-2: You know the only thing that has made the whole thing worthwhile...has been those... few times that I've been able to really, truly connect with another human being.

12-3: We are made of dreams, and dreams are made of us.

12-5: Funny, how just when you think life can't possibly get any worse it suddenly does.

12-6: 美丽的梭罗河/ 我为你歌唱 / 你的光荣历史 / 我永远记在心上 / 旱季来临 / 你轻轻流淌 / 雨季时波涛滚滚 / 你流向远方

## 快速排序和快速选择排序

都是基于分治的思想

快排一般是选左边的数low作为基准数，然后从表的最右边放一个哨兵开始向左搜索，找到第一个小于基准数的记录，并将其与low进行交换，并low++。然后从表的最左侧开始向右搜索，找到第一个大于基准数的记录，并将其与high交换，并high--。重复直至low和high相等。此时的位置即为基准数的最终位置。

还有一种方法是左右同时开始快排，从右往左找一个小于基准的数，再从左往右找一个大于基准的数，交换他们。然后重复这个过程，一直是右边先动，直到两个指针相遇。最后把相遇的位置和pivot元素交换。

快速选择是为了找到第K大的数的一种更高效的算法，它可以不用保证主元左右两边有序，一次主元划分结束后比较k和主元的位置，有选择地对左边或者右边递归。一般分为select函数，和一个内部的partition函数。partition是一个用于找主元位置的函数，select用二分的思想并进行剪枝，只需要一半的计算量，另外在主元的选择上多了一步随机选择

## BFPRT算法

这是更高级的算法，通过n/mod 5，向下取整分组，每组中五个元素，每个组的中位数可以用插入排序得到。通常被分为partition函数，pivot_median函数，bfprt函数。思想是用组中中位数的中位数作为pivot来划分。经过数学证明在top k问题上有线性的复杂度。




