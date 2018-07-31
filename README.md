# SDD-Major-Project
Cricket Tkinter

from tkinter import *
green = "#327516"
white = "white"
red = "#ba1a1a"
font1 = "Helvetica 16 bold"
w, h, x, y = 300, 400, 200, 200
relief = GROOVE

def window():
    global window
    window = Tk()
    window.geometry("%dx%d+%d+%d" %(w, h, x, y))
    window.title("CRICKET SCORER")
    window.configure(background = green)
    
    mainpage()

def mainpage():
    global window
    window.destroy()
    window = Tk()

    titlept1 = Label(window, text = "CRICKET SCORER", fg = white, bg = green, font = font1).place(relx = 0.35, rely = 0.1, anchor = CENTER)
    startgame = Button(window, text = "Start Game", fg = white, activeforegroun = white, bg = green, activebackground = red, font = font1, width = 20, relief = relief, command = matchinfo).place(relx = 0.5, rely = 0.3, anchor = CENTER)
    tutorial = Button(window, text = "Help", fg = white, activeforeground = white, bg = green, activebackground = red, font = font1, width = 20, relief = relief, command = tutorial_).place(relx = 0.5, rely = 0.45, anchor = CENTER)
    quitbtn = Button(window, text = "Exit", fg = white, activeforeground = white, bg = green, activebackground = red, font = font1, width = 20, relief = relief, command = exit).place(relx = 0.5, rely = 0.6, anchor = CENTER)
    photo = PhotoImage(file="Cricket.png").subsample(10)
    draft = Label(image = photo, bg = green)
    draft.image = photo
    draft.place(relx = 0.85, rely = 0.1, anchor = CENTER)
    
    window.geometry("%dx%d+%d+%d" %(w, h, x, y))
    window.title("CRICKET SCORER")
    window.configure(background = green)

def matchinfo():
   global window
   print("MATCH INFO WORKING")

def tutorial_():
   global window
   print("TUTORIAL WORKING")

window()
