var g = 0.4; // Gravidade
var fy = 0; // Força resultante em Y
var px = 50; // Posição do player no eixo X
var py = -100; // Posição do player no eixo Y
var cy = 320; // posição do obstaculo no eixo Y
var cx = 650; // posição do obstaculo no eixo x
var speed = 3; // Velocidade de deslocamento do Player no eixo Y
var x2 = 400;
let bg;
var vel=1;//Velocidade do inimigo

function setup() {
  bg = loadImage('assets/moonwalk.jpg')
  createCanvas(600, 400);
 
}

function draw() {
  background(bg);
  rectMode(CENTER);

  if(keyIsDown(LEFT_ARROW)){
    px = px - speed;
  }
  if(keyIsDown(RIGHT_ARROW)){
    px = px + speed;
  }
 
  fy = fy + g;
  if(py > 335){ // if(posição_y_do_player > determinada_posição)
    fy = 0; // Anula a força atuando sobre o player (Funciona como a força Normal)
    py = 335;
    puloDuplo = false// Corrige a posição do Player
  }
 
  if(keyIsDown(UP_ARROW) && py >= 335){
    fy = fy - 10;
  }
 
  //Declaração das informações
  py = py + fy
  ellipse(px,py,30,30);
  rect(cx, cy, 20, 60);
 
  text('Pontuação: 0', 500, 20);
  textSize(15);
  fill(0);
 
  text('Nivel: 0', 435, 20);
  textSize(15);
  fill(0);
 
  text('Vidas: $$$', 350, 20);
  textSize(15);
  fill(0);
 
  //Colisão
  if(keyIsDown(RIGHT_ARROW) && dist(px, py, cx, cy)<25){
  px = cx - 25
  fill(0)
}
 
if(keyIsDown(LEFT_ARROW) && dist(px, py, cx, cy)<25){
  px = cx + 25
  fill(0)
}
 
if(keyIsDown(UP_ARROW) && dist(px, py, cx, cy)<45){
  py = cy - 45
  fill(0)
}
 
  if(dist(px, py, cx, cy)<25)
  {
    px = cx - 25
    cx=650
    vel+=0,2
  }
 
if(dist(px, py, cx, cy)>25){
  fill(255)
}
 
//Movimentação do objeto
cx = cx-vel

//Repetição do objeto
if(cx<0)
  {
    cx=650
    vel+=0,2
  }
 
}
