# CSSAnimations
CSS Animations

An animation lets an element gradually change from one style to another.

You can change as many CSS properties you want, as many times you want.

To use CSS animation, you must first specify some keyframes for the animation.

Keyframes hold what styles the element will have at certain times.

![alt text](https://media.giphy.com/media/S4yxvBouu2ili/giphy.gif)
![alt text](https://media.giphy.com/media/e53WDNesxxVn2/giphy.gif)

*The @keyframes Rule*

When you specify CSS styles inside the `@keyframes` rule, the animation will gradually change from the current style to the new style at certain times.

```
/* The animation code */
@keyframes example {
    from {background-color: red;}
    to {background-color: yellow;}
}
```

*Delay an Animation & Duration of an Animation*

The `animation-delay` property specifies a delay for the start of an animation.

The `animation-duration` property defines how long time an animation should take to complete. If the animation-duration property is not specified, no animation will occur, because the default value is 0s (0 seconds).

```
/* The animation code */
@keyframes example {
    0%   {background-color:red; left:0px; top:0px;}
    25%  {background-color:yellow; left:200px; top:0px;}
    50%  {background-color:blue; left:200px; top:200px;}
    75%  {background-color:green; left:0px; top:200px;}
    100% {background-color:red; left:0px; top:0px;}
}
/* The element to apply the animation to */
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
    animation-delay: 2s;
}
```
*Set How Many Times an Animation Should Run*

The `animation-iteration-count` property specifies the number of times an animation should run.

*Run Animation in Reverse Direction or Alternate Cycles*

The `animation-direction` property specifies whether an animation should be played forwards, backwards or in alternate cycles.

The animation-direction property can have the following values:

`normal` - The animation is played as normal (forwards). This is default
`reverse` - The animation is played in reverse direction (backwards)
`alternate` - The animation is played forwards first, then backwards
`alternate-reverse` - The animation is played backwards first, then forwards

*Specify the Speed Curve of the Animation*

The `animation-timing-function` property specifies the speed curve of the animation.

The `animation-timing-function` property can have the following values:

`ease` - Specifies an animation with a slow start, then fast, then end slowly (this is default)
`linear` - Specifies an animation with the same speed from start to end
`ease-in` - Specifies an animation with a slow start
`ease-out` - Specifies an animation with a slow end
`ease-in-out` - Specifies an animation with a slow start and end
cubic-bezier(n,n,n,n) - Lets you define your own values in a cubic-bezier function
