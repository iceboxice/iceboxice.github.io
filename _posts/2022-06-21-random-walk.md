June 21, 2022  

Welcome to the wonderful world of widgets.  
==========================================

Today's widget is a random walk.

![random walk](https://raw.githubusercontent.com/iceboxice/iceboxice.github.io/main/_posts/img/random_walk.gif)  

```python
# https://www.youtube.com/watch?v=BfS2H1y6tzQ

import random

def random_walk(n):
    x,y=0,0
    for i in range(n):
                                #N,S,W,E
        (dx,dy) = random.choice([(0,1),(0,-1),(1,0),(-1,0)])
        x += dx
        y += dy
    return (x,y)

#for i in range(25):
#    walk = random_walk_2(10)
#    print(walk, "Distance from home = ", abs(walk[0]) + abs(walk[1]))

number_of_walks = 20000

for walk_length in range(1,31):
    no_transport = 0 # counter that end <=4 blocks from home
    for i in range(number_of_walks):
        (x,y) = random_walk(walk_length)
        distance = abs(x) + abs(y) #calc dist from home
        if distance <= 4:
            no_transport += 1
    no_transport_percentage = float(no_transport) / number_of_walks
    print("Walk size = ", walk_length, "/% of no transport = ", 100*no_transport_percentage)
```
<ins>Reference</ins>  
[random walk gif](https://mathematica.stackexchange.com/questions/156626/generate-random-walk-on-a-graph)
