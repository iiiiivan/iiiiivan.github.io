Platform Game
=============
![level1 screen shoot](https://user-images.githubusercontent.com/91009153/229108398-2034dbec-3bcd-4a49-87b9-a157f5bc3c49.JPG)

  * Find the door to teleport and go to checkpoint.
  * Lots of enemies want to stop you avoid touching them.



https://user-images.githubusercontent.com/91009153/232002500-c50607bb-2904-4285-b931-54b4248c960f.mp4


Resources used
--------------

  * [python](https://www.python.org/)
  * [ldtk](https://ldtk.io/)
  * [vs code](https://code.visualstudio.com)

Code 

  
Enemy's code for moving back and forward.
  
~~~python
class Enemy(Sprite):
    def on_create(self):
        self.image="enemy.png"
        self.going_right=True
        self.add_tag('enemy')
        self.scale=2
        

    def on_update(self, dt):
        if self.going_right:
            self.x+=2.5
        else:
            self.x-=2.5
        if self.going_right and self.x>self.right_target.x:
            self.going_right=False
        if self.going_right==False and self.x<self.left_target.x:
            self.going_right=True


for enemy in w.get_sprites_with_tag('ldtk_Enemy'):
    enemy=w.create_sprite(Enemy, position=enemy.position)
    enemy.right_target=Point(enemy.x+9+18*8, 0)
    enemy.left_target=enemy.position
~~~  
  
Lunar Lander
=============    
 * Try to touch the star and get some fuel
 * Don't touch any rocks and land on the platform

*[click](https://iiiiivan.github.io/lunar_lander_webgl_01/index.html)

Resources used
---
 * [Unity](https://unity.com/cn)
 * [C#](https://visualstudio.microsoft.com/zh-hant/downloads/)

Move Game
==========

[click](https://iiiiivan.github.io/move Webgl/index.html)

Tower
==========

(https://iiiiivan.github.io/Tower_webgl1/index.html)
