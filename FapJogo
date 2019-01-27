from visual import *
from visual.controls import *
 
COMP_VELOCITY = 10
V_CONST = 0.005
  
humano = box(pos = (-22, -2, 0), size = (0.2, 4, 7), color = color.blue)
computador = box(pos = (8, -1, 0), size = (0.2, 34, 7), color = color.black)
wallT = box(pos = (-7, 16, 0), size = (30, 0.2, 7), color = color.blue)
wallB = box(pos = (-7, -18, 0), size = (30, 0.2, 7), color = color.blue)

bloco1 = box(pos=(-7,12,0), size = (2,2,2), color=color.green)
bloco2 = box(pos=(0,12,0), size = (2,2,2), color=color.green)
bloco3 = box(pos=(-9,10,0), size = (2,2,2), color=color.green)
bloco4 = box(pos=(2,10,0), size = (2,2,2), color=color.green)
bloco5 = box(pos=(-9,8,0), size = (2,2,2), color=color.green)
bloco6 = box(pos=(2,8,0), size = (2,2,2), color=color.green)
bloco7 = box(pos=(-11,6,0), size=(2,2,2), color=color.green)
bloco8 = box(pos=(-9,6,0), size=(2,2,2), color=color.green)
bloco9 = box(pos=(-7,6,0), size=(2,2,2), color=color.green)
bloco10 = box(pos=(-5,6,0), size=(2,2,2), color=color.green)
bloco11 = box(pos=(-3,6,0), size=(2,2,2), color=color.green)
bloco12 = box(pos=(-1,6,0), size=(2,2,2), color=color.green)
bloco13 = box(pos=(1,6,0), size=(2,2,2), color=color.green)
bloco14 = box(pos=(3,6,0), size=(2,2,2), color=color.green)
bloco15 = box(pos=(-13,4,0), size=(2,2,2), color=color.green)
bloco16 = box(pos=(5,4,0), size=(2,2,2), color=color.green)
bloco17 = box(pos=(-5,2,0), size=(2,2,2), color=color.red)
bloco18 = box(pos=(-3,2,0), size=(2,2,2), color=color.red)
bloco19 = box(pos=(-7,0,0), size=(2,2,2), color=color.red)
bloco20 = box(pos=(-5,0,0), size=(2,2,2), color=color.red)
bloco21 = box(pos=(-3,0,0), size=(2,2,2), color=color.red)
bloco22 = box(pos=(-1,0,0), size=(2,2,2), color=color.red)
bloco23 = box(pos=(-13,-2,0), size=(2,2,2), color=color.green)
bloco24 = box(pos=(-5,-2,0), size=(2,2,2), color=color.red)
bloco25 = box(pos=(-3,-2,0), size=(2,2,2), color=color.red)
bloco26 = box(pos=(5,-2,0), size=(2,2,2), color=color.green)
bloco27 = box(pos=(-11,-4,0), size=(2,2,2), color=color.green)
bloco28 = box(pos=(3,-4,0), size=(2,2,2), color=color.green)
bloco29 = box(pos=(-9,-6,0), size=(2,2,2), color=color.green)
bloco30 = box(pos=(-7,-6,0), size=(2,2,2), color=color.green)
bloco31 = box(pos=(-5,-6,0), size=(2,2,2), color=color.green)
bloco32 = box(pos=(-3,-6,0), size=(2,2,2), color=color.green)
bloco33 = box(pos=(-1,-6,0), size=(2,2,2), color=color.green)
bloco34 = box(pos=(1,-6,0), size=(2,2,2), color=color.green)
bloco35 = box(pos=(-7,-8,0), size=(2,2,2), color=color.green)
bloco36 = box(pos=(-5,-8,0), size=(2,2,2), color=color.green)
bloco37 = box(pos=(-3,-8,0), size=(2,2,2), color=color.green)
bloco38 = box(pos=(-1,-8,0), size=(2,2,2), color=color.green)
bloco39 = box(pos=(-5,-10,0), size=(3,2,2), color=color.green)
bloco40 = box(pos=(-3,-10,0), size=(3,2,2), color=color.green)
bloco41 = box(pos=(-5,-12,0), size=(2,2,2), color=color.green)
bloco42 = box(pos=(-3,-12,0), size=(2,2,2), color=color.green)
bloco43 = box(pos=(-4,-14,0), size=(3,2,2), color=color.green)
bloco44 = box(pos=(-4,-16,0), size=(2,2,2), color=color.green)

blocos = [bloco1, bloco2, bloco3,bloco4,bloco5,bloco6,bloco7,bloco8,bloco9,bloco10,
          bloco11,bloco12,bloco13,bloco14,bloco15,bloco16,bloco17,bloco18,bloco19,bloco20,
          bloco21,bloco22,bloco23,bloco24,bloco25,bloco26,bloco27,bloco28,bloco29,bloco30,
          bloco31,bloco32,bloco33,bloco34,bloco35,bloco36,bloco37,bloco38,bloco39,bloco40,
          bloco41,bloco42,bloco43,bloco44]
 
bola = sphere (pos = (-22,0,0), radius = 0.6, color = color.yellow)

 
 
 
dt = 0
inc = 1
vscale = 0.005
scoreJogador = 0
scoreComputador = 0
targetScore = 21
 
inicioJogo = False
fimJogo = False

 
def hitPaddle(direction):
     if direction > 0 and \
     bola.pos.x + bola.radius >= computador.pos.x - computador.size.x and \
     bola.pos.y <= computador.pos.y + (computador.size.y / 2) and \
     bola.pos.y >= computador.pos.y - (computador.size.y / 2):
         return true
     if direction < 0 and \
     bola.pos.x - bola.radius < humano.pos.x + humano.size.x and \
     bola.pos.y <= humano.pos.y + (humano.size.y / 2) and \
     bola.pos.y >= humano.pos.y - (humano.size.y / 2):
         return true
     return false
 
def passedPaddle(direction):
     if direction >= 0 and \
     bola.pos.x + bola.radius >= computador.pos.x - computador.size.x and \
     (bola.pos.y >= computador.pos.y + (computador.size.y / 2) or \
     bola.pos.y <= computador.pos.y - (computador.size.y / 2)):
         return 1
     if direction < 0 and \
     bola.pos.x - bola.radius < humano.pos.x + humano.size.x and \
     (bola.pos.y >= humano.pos.y + (humano.size.y / 2) or \
     bola.pos.y <= humano.pos.y - (humano.size.y / 2)):
         return -1
     return 0
 
def collide(wall,bola):
     if \
     abs (wall.pos.x - bola.pos.x) <= wall.length/2 and \
      ((wall.pos.y + wall.height/2 + bola.radius > bola.pos.y) and\
      (wall.pos.y - wall.height/2 - bola.radius < bola.pos.y)):
          return True
     else:
          return False
 
while inicioJogo == False:
     rate(100)
     if scene.mouse.pos.y - (humano.size.y / 2) > wallB.pos.y + wallB.size.y and \
     scene.mouse.pos.y + (humano.size.y / 2) < wallT.pos.y - wallT.size.y:
         humano.pos.y = scene.mouse.pos.y
         bola.pos.y = scene.mouse.pos.y
     if scene.mouse.clicked:
         bola.velocity = vector(10, 5, 0)
         inicioJogo = True
 
while fimJogo == False:
     rate(100)
     if scene.mouse.pos.y - (humano.size.y / 2) > wallB.pos.y + wallB.size.y and \
     scene.mouse.pos.y + (humano.size.y / 2) < wallT.pos.y - wallT.size.y:
         humano.pos.y = scene.mouse.pos.y
     if bola.pos.y > computador.pos.y and bola.velocity.x > 0:
         computador.pos.y = computador.pos.y + COMP_VELOCITY * V_CONST
     elif bola.pos.y < computador.pos.y and bola.velocity.x > 0:
         computador.pos.y = computador.pos.y - COMP_VELOCITY * V_CONST
     if hitPaddle(bola.velocity.x):
         bola.velocity.x = -bola.velocity.x
         bola.velocity += (bola.velocity*0.01)
     if bola.pos.y + bola.radius > wallT.pos.y - wallT.size.y or \
     bola.pos.y - bola.radius < wallB.pos.y + wallB.size.y:
         bola.velocity.y = -bola.velocity.y
     if passedPaddle(bola.velocity.x) == 1 and bola.velocity.x > 0:
         scoreJogador += 1
         if blocos<= 0:
             fimJogo = True
             print "Ganhaste!"
     elif passedPaddle(bola.velocity.x) == -1 and bola.velocity.x < 0:
         scoreComputador += 1
         if scoreComputador >= targetScore:
             fimJogo = True
             print """Perdeste!"""
     bola.pos = bola.pos + bola.velocity * vscale
 
     bola.pos = bola.pos + bola.velocity * vscale
     for bloco in blocos:
 
          if collide(bloco, bola) and bloco.visible:
              bloco.visible = 0
              bola.velocity.y = -1 * bola.velocity.y
 
 
     if bola.x > computador.x:
          bola.velocity.x = -bola.velocity.x
