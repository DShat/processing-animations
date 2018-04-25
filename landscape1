PVector[] clouds;
PImage original;
float y;
float cloudX;
int white;
int green;
int blue;
color from = color(blue);
color to= color(white);
void setup(){
size (500,375);
white = color(#FFFFFF);
blue = color(#216CFC);
green = color(#4BCE00);
y=0;
original = loadImage("bliss.jpg");
clouds = new PVector[10];
  for (int i = 0; i < clouds.length; i++) {
    float x = random(0, width);
    float y = random(0, height/3);
    clouds[i] = new PVector(x, y);
  }
}
void draw(){
  background(original);
  background(lerpColor(blue,white,.5));
  
  noStroke();
  fill(green);
  beginShape();
    vertex(0,375);
    vertex(0,157);
    vertex(35,151);
    vertex(99,150);
    vertex(158,155);
    vertex(235,158);
    vertex(330,170);
    vertex(431,184);
    vertex(500,194);
    vertex(500,375);
   endShape(CLOSE);
  
 
   for (int i = 0; i < clouds.length; i++) {
    clouds[i].add(1, 0);
   
    if (clouds[i].x - 75 > width) {
      clouds[i].x = -75;
      clouds[i].y = (int) random(50, height/4);
    }
    
  noStroke();
    fill(255);
    ellipse(clouds[i].x, clouds[i].y, 70, 50);
    ellipse(clouds[i].x+20, clouds[i].y+15, 70, 50);
    ellipse(clouds[i].x-20, clouds[i].y+15, 70, 50);
   }
}
void mousePressed(){
  println(mouseX + "," + mouseY);
}
