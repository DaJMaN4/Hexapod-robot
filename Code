from adafruit_blinka.board.pyboard import X3
from board import I2C
from evdev import InputDevice, categorize, ecodes
from adafruit_servokit import ServoKit
kit = ServoKit(channels=16,i2c=None, address=0x40)
kit2 = ServoKit(channels=16,i2c=None, address=0x41)
import time
import math
import os
import sys
number = 0
for _ in range(6): 
    kit.servo[number].set_pulse_width_range(500, 2500)
    number = number + 1
number = 4
for _ in range(12): 
    kit2.servo[number].set_pulse_width_range(500, 2500)
    number = number + 1
gamepad = InputDevice('/dev/input/event0')
print(gamepad)
lewygas = 310
prawygas = 311
nadlewygas = 308
nadprawygas = 309

#up = 307
down = 305
left = 304
right = 306

start = 313
select = 312

start_red = 316

clicjoysticklewy = 314
clicjoystickprawy = 315

coxa = 74
femur = 100
tibia = 162
gamma = 90

x = 160
y = 0.1
z = 210

xx = x 
yy = y 
yyy = y
xxx = x 
xx2 = x 
yy2 = y 
yyy2 = y
xxx2 = x 

n = 1
x_max = 215
up = 2

o = 0
h = 1
gammalist1 = []
alist1 = []
blist1 = []

gammalist2 = []
alist2 = []
blist2 = []

outalist = []
outblist = []
outgammalist = []

xh = 0
yh = 0

def zz():
    return z
def move(): 
    z = 210
    def calculate(): 
        if x < 0:
            gamma = math.atan((x/-1) / y) * 57.296

            L1 = x - coxa / -1 
            L = math.sqrt(z**2 + L1**2)

            a1 = math.asin(z/L) * 57.296
            a2 = math.acos((L**2 + femur**2 - tibia**2)/(2*femur*L)) * 57.296
            a = a1 + a2 - 90 
        else: 
            gamma = math.atan(x / y) * 57.296

            L1 = x - coxa 
            L = math.sqrt(z**2 + L1**2)

            a1 = math.acos(z/L) * 57.296
            a2 = math.acos((L**2 + femur**2 - tibia**2)/(2*femur*L)) * 57.296
            a = a1 + a2
        b = math.acos((tibia**2 + femur**2 - L**2)/(2*tibia*femur)) * 57.296 - 90
        if (gamma < 0): #map() fuknsjon
            gamma = (gamma - (-90)) * 90 / -90 + 90
            gamma = ((gamma - 90) / -1 )+ 90
        return gamma,a,b
    if up == 1 or up == 3:
        x = xx
        y = 0.1
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else: 
        x = xx
        y = 0.1
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    if up == 2 or up == 3: 
        x = xx
        y = 0.1
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else: 
        x = xx
        y = 0.1
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    if up == 2 or up == 3:
        x = xxx
        y = yy
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else:
        x = xxx
        y = yy
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    if up == 1 or up == 3:
        x = xxx
        y = yyy
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else: 
        x = xxx
        y = yyy
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    if up == 2 or up == 3:
        x = xxx
        y = yyy
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else: 
        x = xxx
        y = yyy
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    if up == 1 or up == 3:
        x = xxx
        y = yy
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
    else:
        x = xxx
        y = yy
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist1.append(gamma)
        alist1.append(a)
        blist1.append(b)
        z = z1 
    return alist1, blist1, gammalist1
def move2():
    z = 210
    def calculate(): 
        if x < 0:
            gamma = math.atan((x/-1) / y) * 57.296

            L1 = x - coxa / -1 
            L = math.sqrt(z**2 + L1**2)

            a1 = math.asin(z/L) * 57.296
            a2 = math.acos((L**2 + femur**2 - tibia**2)/(2*femur*L)) * 57.296
            a = a1 + a2 - 90
        else: 
            gamma = math.atan(x / y) * 57.296

            L1 = x - coxa
            L = math.sqrt(z**2 + L1**2)

            a1 = math.acos(z/L) * 57.296
            a2 = math.acos((L**2 + femur**2 - tibia**2)/(2*femur*L)) * 57.296
            a = a1 + a2
        b = math.acos((tibia**2 + femur**2 - L**2)/(2*tibia*femur)) * 57.296 - 90
        if (gamma < 0): #map() fuknsjon
            gamma = (gamma - (-90)) * 90 / -90 + 90
            gamma = ((gamma - 90) / -1 )+ 90
        return gamma,a,b
    if up == 1 or up == 3:
        y = yy2
        x = math.sqrt(math.pow(y,2) + 25600)
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else: 
        y = yy2
        x = math.sqrt(math.pow(y,2) + 25600)
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    if up == 2 or up == 3: 
        y = yyy2
        x = math.sqrt(math.pow(y,2) + 25600)
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else: 
        y = yyy2
        x = math.sqrt(math.pow(y,2) + 25600)
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    if up == 2 or up == 3:
        x = xxx2
        y = yyy2
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else:
        x = xxx2
        y = yyy2
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    if up == 1 or up == 3:
        x = xxx2
        y = yy2
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else: 
        x = xxx2
        y = yy2
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    if up == 2 or up == 3:
        x = xx2
        y = yyy2
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else: 
        x = xx2
        y = yyy2
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    if up == 1 or up == 3:
        x = xx2
        y = yy2
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
    else:
        x = xx2
        y = yy2
        z1 = zz()
        z = 191
        gamma, a, b = calculate()
        gammalist2.append(gamma)
        alist2.append(a)
        blist2.append(b)
        z = z1 
    return alist2, blist2, gammalist2
while True:
    event = gamepad.read_one()
    if event != None and event.type == ecodes.EV_ABS: 
        if event.code == 0: 
            xh = (event.value / 255 - 0.5) * 2
            if xh > 0 and xh < 0.1:
                xh = 0
            elif xh < 0 and xh > -0.1: 
                xh = 0
        elif event.code == 1: 
            yh = (event.value / 255 - 0.5) * 2
            if yh > 0 and yh < 0.1:
                yh = 0
            elif yh < 0 and yh > -0.1: 
                yh = 0
        #print("x = ",xh,"y = ",yh,"xx = ",xx,"xxx = ",xxx,"xx2 = ",xx,"xxx2 = ",xxx2)
        #print("xx = ",xx,"xxx = ",xxx,"xx2 = ",xx,"xxx2 = ",xxx2)
    if xx == 160 and xxx == 160 and xx2 == 160 and xxx2 == 160:
        yyh = yh
        xxh = xh
    if event != None and event.type == ecodes.EV_KEY and event.value == 1:
        if event.code == lewygas:
            print("left_down")
            n = n - 1
            if n < 0:
                n = 1
            print(n)
        elif event.code == prawygas:
            print("right_down")
            n = n + 1
            print(n)
        elif event.code == start_red:
            print("restart")
            os.execv(sys.executable, ['python'] + sys.argv)
        elif event.code == start: 
            kit2.servo[4].angle = 90
            kit2.servo[5].angle = 0
            kit2.servo[6].angle = 0
            kit2.servo[7].angle = 90
            kit2.servo[8].angle = 0
            kit2.servo[9].angle = 0
            kit2.servo[10].angle = 90
            kit2.servo[11].angle = 0
            kit2.servo[12].angle = 0
            kit.servo[3].angle = 90
            kit.servo[4].angle = 0
            kit.servo[5].angle = 0
            kit.servo[0].angle = 90
            kit.servo[1].angle = 0
            kit.servo[2].angle = 0
            kit2.servo[13].angle = 90
            kit2.servo[14].angle = 0
            kit2.servo[15].angle = 0
    if 0 > yyh:
        if up == 1: #rett
            xx = xx - n
            yy = yy - n
            yyy = yyy + n   
            xxx = xxx + n
        elif up == 2: 
            xx = xx + n
            yy = yy + n
            yyy = yyy - n
            xxx = xxx - n
        alist1, blist1, gammalist1 = move()
    elif 0 < yyh:
        if up == 1: #bakk
            xx = xx + n
            yy = yy + n
            yyy = yyy - n
            xxx = xxx - n
        elif up == 2: 
            xx = xx - n
            yy = yy - n
            yyy = yyy + n
            xxx = xxx + n
        alist1, blist1, gammalist1 = move()
    if 0 > xxh:
        if up == 1: #venstre
            xx2 = xx2 - n
            yy2 = yy2 - n
            yyy2 = yyy2 + n   
            xxx2 = xxx2 + n
        elif up == 2: 
            xx2 = xx2 + n
            yy2 = yy2 + n
            yyy2 = yyy2 - n
            xxx2 = xxx2 - n
        alist2, blist2, gammalist2 = move2()
    elif 0 < xxh:
        if up == 1: #høyre
            xx2 = xx2 + n
            yy2 = yy2 + n
            yyy2 = yyy2 - n
            xxx2 = xxx2 - n
        elif up == 2: 
            xx2 = xx2 - n
            yy2 = yy2 - n
            yyy2 = yyy2 + n
            xxx2 = xxx2 + n
        alist2, blist2, gammalist2 = move2()
    if gammalist1 != []:
        print("gamma1 = ",gammalist1[1])
    if gammalist2 != []:
        print("gamma2 = ",gammalist2[1])
    if gammalist1 != [] or gammalist2 != []:
        #print("j")
        number = 0
        yyyh = yh 
        xxxh = xh
        if xxxh < 0:
            xxxh = xxxh/-1
        if yyyh < 0:
            yyyh = yyyh/-1
        if xxxh < yyyh:
            h = (yyyh*math.sqrt(2))/(math.sqrt((yyyh*xxxh+(yyyh*yyyh)/2+(xxxh*xxxh)/2)*2)*math.sqrt(2))
        elif xxxh > yyyh:
            h = (xxxh*math.sqrt(2))/(math.sqrt((yyyh*xxxh+(yyyh*yyyh)/2+(xxxh*xxxh)/2)*2)*math.sqrt(2))/-1 + 1
        elif xxxh == yyyh:
            h = 0.5
        if yyyh == 0:
            h = xxxh
        elif xxxh == 0:
            h = yyyh
        #if h > 1:
        #print("error   xh",xh,"yh",yh,"h", h)
        #print(gammalist1)
        #if gammalist1 != [] and gammalist2 != []:
        if gammalist1 != [] and gammalist2 != []:
            while number != 6:
                outalist.append((alist1[number]-alist2[number])*h+alist2[number])
                outblist.append((blist1[number]-blist2[number])*h+blist2[number])
                outgammalist.append((gammalist1[number]-gammalist2[number])*h+gammalist2[number])
                number = number + 1
            kit2.servo[4].angle = outgammalist[0]
            kit2.servo[5].angle = outalist[0]
            kit2.servo[6].angle = outblist[0]
            kit2.servo[7].angle = outgammalist[1]
            kit2.servo[8].angle = outalist[1]
            kit2.servo[9].angle = outblist[1]
            kit2.servo[10].angle = outgammalist[2]
            kit2.servo[11].angle = outalist[2]
            kit2.servo[12].angle = outblist[2]
            kit.servo[3].angle = outgammalist[3]
            kit.servo[4].angle = outalist[3]
            kit.servo[5].angle = outblist[3]
            kit.servo[0].angle = outgammalist[4]
            kit.servo[1].angle = outalist[4]
            kit.servo[2].angle = outblist[4]
            kit2.servo[13].angle = outgammalist[5]
            kit2.servo[14].angle = outalist[5]
            kit2.servo[15].angle = outblist[5]
        #print(h)
        #print(outgammalist)
        #print("a = ",outalist)
        #print("b = ",outblist)
            print("gamma1 = ",gammalist1[1],"gamma2 = ",gammalist2[1],"gammaout = ",outgammalist[1],"h = ",h)
            alist1.clear()
            blist1.clear()
            gammalist1.clear()
            alist2.clear()
            blist2.clear()
            gammalist2.clear()
        elif gammalist1 != []:
            kit2.servo[4].angle = gammalist1[0]
            kit2.servo[5].angle = alist1[0]
            kit2.servo[6].angle = blist1[0]
            kit2.servo[7].angle = gammalist1[1]
            kit2.servo[8].angle = alist1[1]
            kit2.servo[9].angle = blist1[1]
            kit2.servo[10].angle = gammalist1[2]
            kit2.servo[11].angle = alist1[2]
            kit2.servo[12].angle = blist1[2]
            kit.servo[3].angle = gammalist1[3]
            kit.servo[4].angle = alist1[3]
            kit.servo[5].angle = blist1[3]
            kit.servo[0].angle = gammalist1[4]
            kit.servo[1].angle = alist1[4]
            kit.servo[2].angle = blist1[4]
            kit2.servo[13].angle = gammalist1[5]
            kit2.servo[14].angle = alist1[5]
            kit2.servo[15].angle = blist1[5]
            alist1.clear()
            blist1.clear()
            gammalist1.clear()
        elif gammalist2 != []:
            kit2.servo[4].angle = gammalist2[0]
            kit2.servo[5].angle = alist2[0]
            kit2.servo[6].angle = blist2[0]
            kit2.servo[7].angle = gammalist2[1]
            kit2.servo[8].angle = alist2[1]
            kit2.servo[9].angle = blist2[1]
            kit2.servo[10].angle = gammalist2[2]
            kit2.servo[11].angle = alist2[2]
            kit2.servo[12].angle = blist2[2]
            kit.servo[3].angle = gammalist2[3]
            kit.servo[4].angle = alist2[3]
            kit.servo[5].angle = blist2[3]
            kit.servo[0].angle = gammalist2[4]
            kit.servo[1].angle = alist2[4]
            kit.servo[2].angle = blist2[4]
            kit2.servo[13].angle = gammalist2[5]
            kit2.servo[14].angle = alist2[5]
            kit2.servo[15].angle = blist2[5]
            alist2.clear()
            blist2.clear()
            gammalist2.clear()
        outalist.clear()
        outblist.clear()
        outgammalist.clear()
        #if xh != 0 and yh != 0:
            #print("x = ",xh,"y = ",yh,"xx = ",xx,"xxx = ",xxx,"xx2 = ",xx2,"xxx2 = ",xxx2)
    if xx >= x_max or xxx >= x_max or xx2 >= x_max or xxx2 >= x_max:
        if up == 1:
            up = 2 
        elif up == 2:
            up = 1
            
