---
title: Globe
description: Generating random concentric ellipses
author: Daniela Heinz
image: daniela-globe.png
layout: post
reset: true
---

<script>
function setup() {
    let canvas = createCanvas(600, 600);

    canvas.parent("post");

    background(0);
    colorMode(HSL);
}

function draw() {
    noFill();


if (mouseIsPressed) {
    var breite = random(20, 600);
    var hoehe = random(20, 600);
    var deckkraft = random(10, 100);

    stroke(deckkraft);
  
    stroke(190, 100, 50, 0.4)
  ellipse(width / 2, height / 2, breite, hoehe);

  //line(width / 2, height /2, mouseX, mouseY);
  }

  if (keyCode == 65 && keyIsPressed) {
      speichern();
  }
}

function keyPressed() {
    if (key == 's') {
        speichern();
    }

    if (key == 'n') {
        setup();
    }
}

function speichern() {
    saveCanvas('globe', 'png')
}
</script>