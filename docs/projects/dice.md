# Dice

## Introduction @unplugged

![A microbit dice](/static/mb/projects/dice.png)

Let's turn the @boardname@ into a dice! To do so, we need 3 pieces of code: detect a throw (shake),
pick a random number, show the number.

## Step 1 @fullscreen

Place the ``||input:on shake||`` block. It runs code when you shake the @boardname@.

```blocks
input.onGesture(Gesture.Shake, () => {

})
```

## Step 2 @fullscreen

Place the ``||basic:show number||`` block in the ``||input:on shake||`` block to display a number.

```blocks
input.onGesture(Gesture.Shake, () => {
    basic.showNumber(0)
})
```

## Step 3 @fullscreen

Place the ``||Math:pick random||`` block in an ``||input:on shake||`` block to pick a random number.

```blocks
input.onGesture(Gesture.Shake, () => {
    basic.showNumber(Math.randomRange(0, 10))
})
```

## Step 4 @fullscreen

A typical dice shows values from `1` to `6`. So, in ``||Math:pick random||``, don't forget to choose the right minimum and maximum values!

```blocks
input.onGesture(Gesture.Shake, () => {
    basic.showNumber(Math.randomRange(1, 6))
})
```

## Step 5

Use the simulator to try out your code. Does it show the number you expected?

## Step 6

If you have a @boardname@ connected, click ``|Download|`` and transfer your code to the @boardname@!