# Animate with CSS3 Transitions

In this presentation, I will go some CSS3 properties for transition animations and demonstrate how to use them.

## Getting Started

At its most basic form, CSS3 transitions work by having an initial state, final state, and a duration for the animation. Commonly this is achieved by having an event to change the state of an element. 

For example, button element with a hover state that changes its background colour.

- Initial state: button is dark grey
- Final state: button is light grey
- Duration: 0.3s 

For the example above, hovering over the button element will cause it to animate from a dark grey background colour to a light grey background colour. The transition animation will progress over a period of 0.3s, anything longer than 0.3s is usually perceived as being too slow, but this depends on the context.

Demo: http://codepen.io/phuongy/pen/mJOPdK?editors=110

## Using CSS3 transform

Transition animations can also work with the CSS3 `transform` property to manipulate elements. These transform properties render in the browser using hardware acceleration, so usually they will appear to be smoother.

In the next example, I will demonstrate some transform properties on the button element from the previous example.

Demo: http://codepen.io/phuongy/pen/zGoqww?editors=110

## Tweaking your animations

Timing functions allow us to refine how the animation progresses over time. By default, the timing function used in our animations is `linear`, meaning the animation progression over time is constant.

This website by Lea Verou, http://cubic-bezier.com/, gives us an elegant way to visualise the animation progression over time.

To achieve a better result, use `cubic-bezier` timing function to refine your animation and produce some more interesting effects.

Demo: http://codepen.io/phuongy/pen/zGozKa?editors=110

## How about 3D Transforms?

Three dimensional effects can easily be achieved using methods similar to those from the previous examples. The main difference now is that you need to setup a `perspective`, which will be explained in the next demo.

Demo: http://codepen.io/phuongy/pen/RPoxxg?editors=110


