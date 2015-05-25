# Animations with CSS3 transitions

At its most basic form, CSS3 transitions work by having an initial state, final state, and a duration for the animation.

## Simple transitions

Commonly this is achieved by having an event to change the state of an element. For example, button element with a hover state, that changes its background colour.

- Initial state = button is black
- Final state = button is red
- Duration = 0.3s // anything slower than this is usually too slow

We can use the :hover state in css to change this button state.

```
// simple transition

.button {
	background: black;
	border: none;
	border-radius: 4px;
	color: #fff;
	padding: 5px 10px;
	//transition-duration: 0.3s;		// add transition-duration for the browser to animate the state change effect
}

.button:hover {
	background: red;
}
```

## Using CSS3 transform

We can use `transform` to manipulate the element.

- `scale(x,y)`
- `rotate()`
- `translate()`

```
// simple transforms

.button {
	background: black;
	border: none;
	border-radius: 4px;
	color: #fff;
	padding: 5px 10px;
	transition-duration: 0.3s;	
}

.button:hover {
	transform: scale(1.1,1.1);
	transform: rotate(90deg);
	transform: translate(10px,0);
	transform: scale(1.1,1.1) rotate(90deg) translate(10px,0);
}
```

## Mixing things up

We can achieve interesting effects if we add transition changes to pseudo elements.

```
// delete button
// - using delay
// - opacity
// - multiple transforms
// - timing function

.button {
	background: black;
	border: none;
	border-radius: 4px;
	color: #fff;
	padding: 5px 10px;
	transition-duration: 0.3s;	
}

.button:hover {

}

.button:after {
	background: rgba(255,255,255,0);
	content: ‘X’;
	transform: translate(0,0);
	transition-duration: 0.3s;
}

.button:after:hover {
	background: rgba(255,255,255,0.2);
	transform: translate(100%,0);
}	
```

## Achieving more realistic animations with timing functions

Don’t use `linear`, `ease-in`, `ease-out`, or `ease-in-out`.

To achieve a better result, use `cubic-bezier`.

Tweak the curve and experiment with the effects.
- bounce effect
- tweaking the speed

## How about some 3D transitions?

Provide context for notifications or errors.

```
.container {
	perspective: 1000;
}

.form {

}

.form.error {
	
}

.button {

}

.button:hover, .button:active {

}

.dropdown {
	transform: rotateX(-0.25turn);
}

.dropdown.active {
	transform: rotateX(0);
}
```




