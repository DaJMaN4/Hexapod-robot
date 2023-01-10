import math
import turtle

coxa = 74
femur = 100
tibia = 162

x = -30
y = 2
z = 130
b = 0
a = 0
vite = 0
gamma = 0


def calculate():
    xc = x - coxa
    if xc < 0:
        gamma = math.atan((xc / -1) / y) * 57.296

        L1 = xc / -1
        L = math.sqrt(z ** 2 + L1 ** 2)

        a1 = math.asin(z / L) * 57.296
        a2 = math.acos((L ** 2 + femur ** 2 - tibia ** 2) / (2 * femur * L)) * 57.296
        a = a1 + a2 - 90
    else:
        gamma = math.atan(xc / y) * 57.296

        L1 = xc
        L = math.sqrt(z ** 2 + L1 ** 2)

        a1 = math.acos(z / L) * 57.296
        a2 = math.acos((L ** 2 + femur ** 2 - tibia ** 2) / (2 * femur * L)) * 57.296
        a = a1 + a2
    b = math.acos((tibia ** 2 + femur ** 2 - L ** 2) / (2 * tibia * femur)) * 57.296
    if gamma < 0:  # map() function
        gamma = (gamma - (-90)) * 90 / -90 + 90
        gamma = ((gamma - 90) / -1) + 90
    return a, b, gamma


while True:

    a, b, gamma = calculate()
    print("b = ", b, "  a = ", a, "     gamma = ", gamma, "  x =", x, "  y = ", y)

    t = turtle.Turtle()
    t2 = turtle.Turtle()
    t.speed(10000)
    t2.speed(1000)

    t.forward(coxa)
    if vite == 1:
        a_draw = (a - 90) / -1 + 90
    else:
        a_draw = (a - 90) / -1
    t.right(a_draw)
    t.forward(femur)
    b_draw = (b - 180) / -1
    t.right(b_draw)
    t.forward(tibia)
    t.penup()
    t.goto(0, 0)
    t.pendown()
    t.left(b - a)

    x = x + 1



