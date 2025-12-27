# Turtle Task
### Упражнение №3. Квадрат

```python
import turtle

t = turtle.Turtle()

t.shape('turtle')
t.forward(100)
t.left(90)
t.forward(100)
t.left(90)
t.forward(100)
t.left(90)
t.forward(100)
t.left(90)

turtle.done()
```
##
### Упражнение №4. Окружность

```python
import turtle

t = turtle.Turtle()

t.shape('turtle')

for i in range(120):
    t.forward(3)
    t.left(3)

turtle.done()
```
##
### Упражнение №5. Больше квадратов

```python
import turtle

t = turtle.Turtle()

t.shape('turtle')

for i in range(10):
    t.pendown()
    size = 100 + i * 30

    for _ in range(4):
        t.forward(size)
        t.left(90)

    t.penup()
    t.left(180)
    t.forward(15)
    t.left(90)
    t.forward(15)
    t.left(90)

turtle.done()
```
##
### Упражнение №6. Паук

```python
import turtle

t = turtle.Turtle()
t.shape('turtle')

n = 8
angle = 360/n

for i in range(n):
    t.left(angle)
    t.forward(100)
    t.stamp()
    t.left(180)
    t.forward(100)
    t.left(180)

turtle.done()
```
##
### Упражнение №7. Спираль

```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)

t.penup()
t.goto(0, 0)
t.pendown()

distance = 0.5
angle = 15
increment = 0.5

for i in range(87):
    t.forward(distance)
    t.left(angle)
    distance += increment

turtle.done()
```
##
### Упражнение №8. Квадратная «спираль»

```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)

t.penup()
t.goto(0, 0)
t.pendown()

for i in range(50):
    t.forward(10+i*10)
    t.left(90)

turtle.done()
```

##
### Упражнение №9. Правильные многоугольники

```python
import turtle
import math

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)


def draw_polygon(n, radius):
    angle = 360 / n

    t.penup()
    t.goto(0, -radius)
    t.setheading(angle / 2)
    t.pendown()

    for _ in range(n):
        t.forward(2 * radius * math.sin(math.pi / n))
        t.left(angle)


for sides in range(3, 13):
    draw_polygon(sides, sides * 10 - 15)


turtle.done()
```
##
### Упражнение №10. Цветок
```python
import turtle

t = turtle.Turtle()
t.speed(0)

t.shape('turtle')


def draw_circle():
    for i in range(120):
        t.forward(3)
        t.left(3)


n = 6
angle = 360 / n

for _ in range(n):
    draw_circle()
    t.left(angle)

turtle.done()
```
##
### Упражнение №11. Бабочка
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)


def draw_circle(radius):
    for _ in range(120):
        t.forward(radius)
        t.left(3)


radius = 3
n = 6

for i in range(n):
    t.right(90)
    draw_circle(radius+i)
    t.left(180)
    draw_circle(radius+i)
    t.right(90)

turtle.done()
```
##
### Упражнение №12. Пружинка
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)


def draw_big_arc():
    for _ in range(50):
        t.forward(3)
        t.right(3.6)


def draw_small_arc():
    for _ in range(10):
        t.forward(3)
        t.right(18)


t.setheading(90)

for _ in range(4):
    draw_big_arc()
    draw_small_arc()

turtle.done()
```
##
### Упражнение №13. Смайлик
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)


def draw_circle(x, y, radius, color):
    t.penup()
    t.goto(x, y)
    t.pendown()
    t.fillcolor(color)
    t.begin_fill()
    t.circle(radius)
    t.end_fill()


def draw_arc():
    for _ in range(50):
        t.forward(3)
        t.right(3.6)


draw_circle(0, 0, 100, 'yellow')

draw_circle(-40, 130, 15, 'blue')
draw_circle(40, 130, 15, 'blue')

t.penup()
t.goto(0, 110)
t.pensize(10)
t.pencolor('black')
t.pendown()
t.right(90)
t.forward(30)

t.penup()
t.goto(50, 80)
t.pencolor('red')
t.pendown()
draw_arc()

turtle.done()
```
#
## Упражнение №14. Звёзды
```python
import turtle

t = turtle.Turtle()
t.shape('turtle')
t.speed(0)


def draw_star(n, size):
    angle = 180 - 180 / n

    for _ in range(n):
        t.forward(size)
        t.right(angle)


t.penup()
t.goto(-200, 0)
t.pendown()
t.setheading(270)

draw_star(5, 100)

t.penup()
t.goto(100, 0)
t.pendown()
t.setheading(270)

draw_star(11, 100)

turtle.done()
```