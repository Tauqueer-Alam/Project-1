# Project-1

from tkinter import *

def click(event):
  global scvalue
  text = event.widget.cget("text")
  if text == "=":
    if scvalue.get().isdigit():
      value = int(scvalue.get())
    else:
      value = eval(screen.get())
    scvalue. set(value)
    screen.update()
  elif text == "C":
    scvalue.set("")
    screen.update()
    
  else:
    scvalue.set(scvalue.get() + text)
  screen.update()

root = Tk()

root.title("Calculator By Tauqueer")

scvalue = StringVar()
scvalue.set("")
screen = Entry(root, textvar=scvalue, font=("lucida", 20, "bold"))
screen.pack(side=TOP)

f1=Frame(root, bg="grey",)
f1.pack()

b1 = Button(f1, text="1", font=("arial", 20, "bold"), fg="red", bg="yellow")
b1.pack(side=LEFT, padx=3, pady=3)
b1.bind('<Button-1>', click)

b2 = Button(f1, text="2", font=("Arrial", 20, "bold"), fg="red", bg="yellow")
b2.pack(side=LEFT, padx=3, pady=3)
b2.bind('<Button-1>', click)

b3 = Button(f1,text="3", font=("Arrial", 20, "bold"), fg="red", bg="yellow")
b3.pack(side=LEFT, padx=3, pady=3)
b3.bind('<Button-1>', click)

b14 = Button(f1, text="*", font=("Arrial", 20, "bold"), fg="white", bg="blue")
b14.pack(side=LEFT, padx=3, pady=3)
b14.bind('<Button-1>', click)
f2=Frame(root, bg="grey")
f2.pack()
b5 = Button(f2,text="4", font=("Arrial", 20, "bold"), fg="red", bg="yellow")
b5.pack(side=LEFT, padx=3, pady=3)
b5.bind('<Button-1>', click)

b6 = Button(f2,text="5", font=("Arrial", 20, "bold"), fg="red", bg="yellow")
b6.pack(side=LEFT, padx=3, pady=3)
b6.bind('<Button-1>', click)

b7 = Button(f2,text="6", font=("Arrial", 20, "bold"), fg="red", bg="yellow")
b7.pack(side=LEFT, padx=3, pady=3)
b7.bind('<Button-1>', click)

b15=Button(f2,text="-", font=("Arrial", 20,"bold"), fg="white", bg="blue")
b15.pack(side=LEFT, padx=3,pady=3)
b15.bind('<Button-1>', click)

f3=Frame(root, bg="grey")
f3.pack()
b8=Button(f3,text="7", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b8.pack(side=LEFT, padx=3,pady=3)
b8.bind('<Button-1>', click)

b9=Button(f3,text="8", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b9.pack(side=LEFT, padx=3,pady=3)
b9.bind('<Button-1>', click)

b10=Button(f3,text="9", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b10.pack(side=LEFT, padx=3,pady=3)
b10.bind('<Button-1>', click)

b16=Button(f3,text="+", font=("Arrial", 20,"bold"), fg="white", bg="blue")
b16.pack(side=LEFT, padx=3,pady=3)
b16.bind('<Button-1>', click)

f4=Frame(root,bg="grey")
f4.pack()
b11=Button(f4,text="00", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b11.pack(side=LEFT, padx=3,pady=3)
b11.bind('<Button-1>', click)

b12=Button(f4,text="0", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b12.pack(side=LEFT, padx=3,pady=3)
b12.bind('<Button-1>', click)

b13=Button(f4,text=".", font=("Arrial", 20,"bold"), fg="red", bg="yellow")
b13.pack(side=LEFT, padx=3,pady=3)
b13.bind('<Button-1>', click)

b17=Button(f4,text="=", font=("Arrial", 20,"bold"), fg="white", bg="orange")
b17.pack(side=LEFT, padx=3,pady=3)
b17.bind('<Button-1>', click)

b18=Button(f4,text="C", font=("Arrial", 20,"bold"), fg="white", bg="green")
b18.pack(side=LEFT, padx=3,pady=3)
b18.bind('<Button-1>', click)

root.mainloop()
