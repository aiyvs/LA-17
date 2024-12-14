# LA-17

class Player:
     def __init__(self, name, health, attack_power):
        self.name = name
        self.health = health
        self.attack_power = attack_power
        
     def attack(self, target):
        target.health = target.health - self.attack_power
        print(f"the player {self.name}'s name for {self.attack_power} attack power")
        print(f"the player {target.name}'s health: {target.health} points")
        
     def heal(self, amount):
        self.health = amount.health + 15
        print(f"{self.name} heals for {amount}. Current health: {self.health}")
        
        
nilou = Player("Nilou", 2000, 100)
kuki = Player("Kuki", 2500, 150)

while nilou.health > 0 and kuki.health >0:
          kuki.attack(nilou)
        
if nilou.health <=0:
     print(f"{nilou.name} win!")
        
else:
     print(f"{kuki.name} win!")
