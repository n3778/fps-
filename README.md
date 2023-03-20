# fps-
小飞机fps
将下面代码复制进去，保存为plane_f.py：

导入随机

导入游戏

SCREEN_RECT=pygame。矩形（0，0，660，909）

FRAME_PER_SEC=60

CREATE_ENEMY_EVENT=pygame。用户事件

HERO_FIRE_EVENT=pygame。用户事件+1

class GameSprite （pygame.sprite.Sprite）：

def __init__（自身，image_name，速度=1，速度1=1）：

超级（）.__init__（）

self.image = pygame.image.load（image_name）

self.rect = self.image.get_rect（）

自身速度 = 速度

自我速度1 = 速度1

DEF 更新（自我）：

self.rect.y += self.speed

班级背景（游戏精灵）：

def __init__（self，is_alt=False）：

super（）.__init__（“./ditu.jpg”）

 

如果is_alt：

self.rect.y=-self.rect.height

 

DEF 更新（自我）：

super（）.update（）

 

如果 self.rect.y>=SCREEN_RECT.height：

self.rect.y=-self.rect.height

 

类敌人（游戏精灵）：

定义__init__（个体经营）：

如果 random.random（）<0.21：

super（）.__init__（“./bd2.png”）

elif random.random（）>0.81：

super（）.__init__（“./bd4.png”）

elif random.random（）>0.21 和 random.random（）<0.4 ：

super（）.__init__（“./bd5.png”）

            

还：

super（）.__init__（“./bd6.png”）

            

self.speed=random.randint（1，2）

self.rect.bottom=0

max_x=SCREEN_RECT.宽度-自我.矩形.宽度

self.rect.x=random.randint（0，max_x）

通过

DEF 更新（自我）：

super（）.update（）

如果 self.rect.y>=SCREEN_RECT.height：

自我杀戮（）

def __del__（个体经营）：

通过

职业英雄（游戏精灵）：

 

定义__init__（个体经营）：

super（）.__init__（“./ys1.png”，0）

self.rect.centerx=SCREEN_RECT.centerx

self.rect.bottom=SCREEN_RECT.bottom-50

self.bullets=pygame.sprite.Group（）

        

DEF 更新（自我）：

self.rect.x += self.speed

self.rect.y += self.speed1

如果 self.rect.x<0：

self.rect.x=0

elif self.rect.right>SCREEN_RECT.right：

self.rect.right=SCREEN_RECT.right

elif self.rect.y>800：

self.rect.y=800

elif self.rect.y<SCREEN_RECT.top：

self.rect.y=SCREEN_RECT.top

Def Fire（个体经营）：

keys_pressed=pygame.key.get_pressed（）

如果keys_pressed[皮加姆。K_SPACE]：

sound3=pygame.mixer.Sound（“./hu1.wav”）

声音3.播放（）

对于范围 （1） 中的 i：

子弹=布莱特（）

bullet.rect.bottom=self.rect.y

bullet.rect.centerx=self.rect.centerx+i*42

self.bullets.add（bullet）

类 BUllet（游戏精灵）：

定义__init__（个体经营）：

super（）.__init__（“./2.png”，-4）

DEF 更新（自我）：

super（）.update（）

如果 self.rect.bottom<0：

自我杀戮（）

def __del__（个体经营）：

通过
