import turtle
import math

turtle.title("Juego del Tic Tac Toe")
turtle.setup(1350, 690, 0, 0)
def pintarTab():
    cuadro.penup()
    cuadro.ht()
    cuadro.goto(-300, 310)
    cuadro.pendown()
    cuadro.color('#29F021')
    cuadro.forward(600)
    cuadro.penup()
    cuadro.ht()
    cuadro.goto(-300, -310)
    cuadro.pendown()
    cuadro.color('#29F021')
    cuadro.forward(600)

    cuadro.penup()
    cuadro.ht()
    cuadro.goto(-300, 100)
    cuadro.pendown()
    cuadro.color(1, 0, 0)
    cuadro.forward(600)
    cuadro.penup()
    cuadro.ht()
    cuadro.goto(-300, -100)
    cuadro.pendown()
    cuadro.color(1, 0, 0)
    cuadro.forward(600)
    cuadro.right(90)

    # PRIMERA LINEA Vertical
    # dddd#
    cuadro.penup()
    cuadro.ht
    cuadro.goto(110 + 200, 300)
    cuadro.pendown()
    cuadro.color('#29F021')
    cuadro.forward(600)
    sn.update()

    cuadro.penup()
    cuadro.ht
    cuadro.goto(-510 + 200, 300)
    cuadro.pendown()
    cuadro.color('#29F021')
    cuadro.forward(600)
    sn.update()
    # 4444#
    cuadro.penup()
    cuadro.ht
    cuadro.goto(-100 + 200, 300)
    cuadro.pendown()
    cuadro.color(0, 0, 1)
    cuadro.forward(600)
    sn.update()
    # SEGUNDA LINEA
    cuadro.penup()
    cuadro.ht
    cuadro.goto(-300 + 200, 300)
    cuadro.pendown()
    cuadro.color(0, 0, 1)
    cuadro.forward(600)

    num = 1
    cuadro.color('#E1D2F7')
    for fila1 in range(3):
        cuadro.penup()
        cuadro.goto(-220 + fila1 * 200, 280 - 100)
        cuadro.pendown()
        cuadro.write(num, font=("Arial", 30))
        num += 1
    num = 4
    cuadro.color('#E1D2F7')
    for fila2 in range(3):
        cuadro.penup()
        cuadro.goto(-220 + fila2 * 200, 280 - 300)
        cuadro.pendown()
        cuadro.write(num, font=("Arial", 30))
        num += 1
    sn.update()
    num = 7
    cuadro.color('#E1D2F7')
    for fila3 in range(3):
        cuadro.penup()
        cuadro.goto(-220 + fila3 * 200, 280 - 500)
        cuadro.pendown()
        cuadro.write(num, font=("Arial", 30))
        num += 1
    sn.update()

def pintarX(x,y):
    cuadro.color('#29F021')
    cuadro.penup()
    cuadro.goto(x,y)
    cuadro.pendown()
    cuadro.ht()
    cuadro.setheading(60)

    cuadro.forward(75)
    cuadro.backward(150)
    cuadro.forward(75)
    cuadro.left(60)

    cuadro.forward(75)
    cuadro.backward(150)
    cuadro.forward(75)
    cuadro.left(60)

    sn.update()

def pintarO(x,y):
    cuadro.color('#141eb4')
    cuadro.penup()
    cuadro.goto(x, y +75)
    cuadro.pendown()
    cuadro.ht()
    cuadro.setheading(0)

    for i in range(180):
        cuadro.forward((150*math.pi)/180)
        cuadro.right(2)
    sn.update()

def ganadorP(ficha):
    for i in range(3):
        if coordenada[i][0] == coordenada[i][1]:
            if coordenada[i][1] == coordenada[i][2]:
                if coordenada[i][0] == ficha:
                    return True
        if coordenada[0][i] == coordenada[1][i]:
            if coordenada[1][i] == coordenada[2][i]:
                if coordenada[0][i] == ficha:
                    return True


    if coordenada[0][0] == coordenada[1][1]:
        if coordenada[1][1] == coordenada[2][2]:
            if coordenada[0][0] == ficha:
                return True
    if coordenada[0][2] == coordenada[1][1]:
        if coordenada[1][1] == coordenada[2][0]:
            if coordenada[0][2] == ficha:
                return True



    return False
def empate():
    contador = 0
    for i in range(3):
        for j in range(3):
            if coordenada[i][j] == "x":
                contador+=1
    if contador>4:
        return True
    else:
        return False
def agregarO():
    for i in range(3):
        for j in range(3):
            if coordenada[i][j] == " ":
                coordenada[i][j]="o"
                if ganadorP("o"):
                    pintarO(-200+200*j,200-200*i)
                    return
                coordenada[i][j]=" "

    for i in range(3):
        for j in range(3):
            if coordenada[i][j] == "":
                coordenada[i][j] = "x"
                if ganadorP("x"):
                    coordenada[i][j]="o"
                    pintarO(-200+200*j,200-200*i)
                    return
                coordenada[i][j]=" "
    for i in range(0,3,2):
        for j in range(0,3,2):
            if coordenada[i][j]==" ":
                coordenada[i][j]="o"
                pintarO(-200+200*j,200-200*i)
                return
    for i in range(3):
        for j in range(3):
            if coordenada[i][j]==" ":
                coordenada[i][j]="o"
                pintarO(-200+200*j,200-200*i)
                return
def colocar(posicionTab):
    for i in range(9):
     sn.onkey(posicionesTab[i], str(i+1))
def  quitar():
    for i in range(9):
     sn.onkey(None,str(i+1))

def agregarX(fila,columna):
    maquina.clear()
    if coordenada[fila][columna] == "x" or coordenada[fila][columna] == "o":
       maquina.write("Ocupado",font=("Arial", 36))
       sn.update()
    else:
       pintarX(-200+200*columna,200-200*fila)

       coordenada[fila][columna] = "x"


       if ganadorP("x"):
            maquina.goto(-97,0)
            maquina.write("Ganaste :D", font=("Arial",36))

            sn.update()
            quitar()
       else:
           agregarO()
           if ganadorP("o"):
               maquina.goto(-90,0)
               maquina.write("Perdiste :C", font=("Arial",36))
               sn.update()
               quitar()
           elif empate():
               maquina.goto(-90,0)
               maquina.write("Empate :c", font=("Arial",36))
               sn.update()
               quitar()
def posicionUno():
    agregarX(0,0)
def posicionDos():
    agregarX(0,1)
def posicionTres():
    agregarX(0,2)
def posicionCuatro():
    agregarX(1,0)
def posicionCinco():
    agregarX(1,1)
def posicionSeis():
    agregarX(1,2)
def posicionSiete():
    agregarX(2,0)
def posicionOcho():
    agregarX(2,1)
def posicionNueve():
    agregarX(2,2)

posicionesTab=[posicionUno,posicionDos,posicionTres,posicionCuatro,posicionCinco,
           posicionSeis,posicionSiete,posicionOcho,posicionNueve]

cuadro = turtle.Turtle()
maquina = turtle.Turtle()

cuadro.pensize(10)
cuadro.ht()

maquina.penup()
maquina.ht()
maquina.goto(-200,0)
maquina.color("red")

sn = turtle.Screen()
sn.tracer()

pintarTab()

coordenada = []
for i in range(3):
    fila = []
    for j in range(3):
        fila.append(" ")
    coordenada.append(fila)

colocar(posicionesTab)
sn.listen()

turtle.done()
