# Sketching ball movements over time.

A math and physics problem, where the student must draw the path of the ball by graphing the **x** and **y** positions over time. [Live Demo](https://realnumbers.app/ball-movements-x-y-canvas/).

![enter image description here](http://petesmaluck.com/project.png)

## Initial Sketch of the idea
![enter image description here](http://petesmaluck.com/IMG_4195.jpg)
## Projection of a point from graph to image.
```
const graphWidth = 324;
const graphHeight = 320;

const imageWidth = 907;
const imageHeight = 513.3;

// Functions to pass a point from the graph, and map it on the image

function getX(x) {
  return x * (imageWidth/graphWidth);
}

function getY(y) {
  return y * (imageHeight/graphHeight);
}

```
## Height Graph.
```
  // Setting the height graph's x and y scale
  
  const TIME_RANGE = [0, 5] // Unit is seconds
  const IMAGE_Y_RANGE = [0.2, 18] // Unit is feet
  const x = d3.scaleLinear().domain(TIME_RANGE).range([0, graphWidth]);
  const y = d3.scaleLinear().domain(IMAGE_Y_RANGE).range([graphHeight, 0]);
  
  const intialBballValue = [{x: 0, y: 13.5}];
```
## X-Position Graph.
```
  // Setting the x-position graph's x and y scale
  
  const TIME_RANGE = [0, 5] // Unit is seconds
  const IMAGE_X_RANGE = [-4.5, 28] // Unit is feet
  const x = d3.scaleLinear().domain(TIME_RANGE).range([0, graphWidth]);
  const y = d3.scaleLinear().domain(IMAGE_X_RANGE).range([graphHeight, 0]);
  
  const intialBballValue = [{x: 0, y: 19.3}];
```

### References 

The main inspiritation.  [Crossing Turtles](https://teacher.desmos.com/activitybuilder/custom/5ddbf9ae009cd90bcdeaadd7#preview/8809fa03-a71e-45d9-b2cd-bef8ee337602) by [Desmos](https://www.desmos.com/).

The video of [Kawhi Leonard's shot](https://www.youtube.com/watch?v=K42-D8QPnok).

[Image Reference](https://a.espncdn.com/photo/2019/0513/r542285_2_1296x729_16-9.jpg).

[Story Reference](https://www.espn.com/nba/story/_/id/26735155/kawhi-ousts-sixers-unprecedented-shot), which contains the photo.

