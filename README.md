# Js_escrevenome
let cor;
let circuloX;
let circuloY;

function setup() {
createCanvas(400, 400);
  background("white");
  cor = color(random(0,250),random(0, 250), random(0, 250));
  
  circuloX = [0,0,0];
  circuloY = [random(height),random(height),random(height)];
}
function draw() {
  fill(cor);
  stroke("green");
  circle(circuloX[0], circuloY[0], 60, 60);
  circle(circuloX[1], circuloY[1], 60, 60);
  circle(circuloX[2], circuloY[2], 60, 60);
  circuloX[0] += random(0, 3);
  circuloY[0] += random(-3, 3);
  
  circuloX[1] += random(0, 3);
  circuloY[1] += random(-3, 3);
  
  circuloX[2] += random(0, 3);
  circuloY[2] += random(-3, 3);
  
  if(circuloX[0] >= width) {
circuloX[0] = 0;
circuloY[0] = random(height);
}
  
  if(circuloX[1] >= width) {
circuloX[1] = 0;
circuloY[1] = random(height);
}
  if(circuloX[2] >= width) {
circuloX[2] = 0;
circuloY[2] = random(height);
}
  
  if(mouseIsPressed) {
cor = color(random(0, 255), random(0, 255), random(0, 255), random(0, 100));
}
  
  
  }  
