#import and initialize pygame 
import pygame
from pygame import event
pygame.init()

#set dimensions of the screen
screen= pygame.display.set_mode((600,600))
screen.fill((255,255,255))

#Colors
black = (0,0,0)
white = (255,255,255)
red = (255,0,0)
green = (0,255,0)
blue = (0,0,255)
pygame.display.update()

class Circle():
    def __init__(self,c,p,r,w):
        self.color=c
        self.pos=p
        self.radius=r
        self.width=w
        self.screen=screen
    def draw(self):
        self.draw=pygame.draw.circle(self.screen,self.color,self.pos,self.radius,self.width)
a=Circle(red,(250,250),30,4)
a.draw()
pygame.display.update()

while True:
    event=pygame.event.poll()
    if event.type == pygame.MOUSEMOTION:
        pos = pygame.mouse.get_pos()
        xC= Circle(red,pos,25,1)
        xC.draw()
        pygame.display.update()

        







        
        
