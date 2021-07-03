---
layout: post
img: /img/blog/animator-vs-tweening-unity.jpg
title: "Should you use Unity's Animator to animate your UI in 2021?"
category: Game Development
tags: unity animator vs tween, is animator better unity, is tweening better unity 
---

It's a headache for unity developers, mostly those who have little to no experience in animating UI. The debate is still on, whether you should use the built-in animatior to animate your UI or use a tweening library.

## Why the debate

Animating a UI game object makes the whole canvas dirty, even when it is not animating. thus it affects the performance. That's the main reason for avoiding built-in animation to animate UI. 
 
## What you should do

However, this behavior has been improved in recent versions of unity. The whole canvas doesn't get rerendered when animating a single UI object. So you can animate your UI without any problem. 

I tested in a low end mobile device, the build had reasonable amount of UI elements. I got 55-60fps while animating and 57-61 while tweening. 

If your primary target is PC and high-end devices, go for animating UI without any second thought. It'll save you a lot of time in development.
If your primary target is mobile devices, you can still animate, as it doesn't visibly affect any performance. You can only tell the difference in the profiler. In the build you will get the same result with both animating and tweening.

But does that mean tweening is over? No. Tweening is flexible, programmer-friendly and reusable. In fact I used tweening for [my game][game-link], because it's reusable.
You can still use a tweening library if you want reusability and if you are comfortable with code. 



[game-link]: https://strangegamestemp.itch.io/a-balls-cursed-day