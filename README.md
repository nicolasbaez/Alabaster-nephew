# Alabaster-nephew
Ask me

![buh](https://github.com/nicolasbaez/Alabaster-nephew/blob/main/xp020.gif)
```javascript
h = 255;
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  background(0);
  stroke(0, h, h, 16);
  directionalLight(h, 0, h, 1, 1, 0);
  for (i = 25; i <= 200; i += 25) {
    k = map(i + w, 50, h, PI, 2 * PI);
    rotateX(k);
    rotateY(k / 2);
    torus(i);
  }
  w -= 0.5;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp020.gif", 700, { delay: 0, units: "frames" });
  }
};
