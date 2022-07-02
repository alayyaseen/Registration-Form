# Registration-Form
import tkinter as tk
from tkinter import*
from tkinter import ttk
from random import randint

rf=Tk()
rf.configure(bg='white')
rf.geometry('800x600')
rf.title('Registration Form')


#heading
a= Label(rf,text="Registration Form",font="times 25 bold",bg='white',fg='black')
a.grid(column=0, row=5)
#fullname
fn=Label(rf,text='Full Name',font='times 15',bg='white',fg='black')
fn.grid(column=0,row=7)
#Email
em=Label(rf,text='Email',font='times 15',bg='white',fg='black')
em.grid(column=0,row=8)
#gender
g=Label(rf,text='Gender',font='times 15',bg='white',fg='black')
g.grid(column=0,row=9)
#country
c=Label(rf,text='Country',font='times 15', bg='white',fg='black')
c.grid(column=0,row=10)
#programming
p=Label(rf,text='Programming',font='times 15',bg='white',fg='black')
p.grid(column=0,row=11)

n=StringVar
e=StringVar
g=StringVar
c=StringVar
p=StringVar

name=Entry(rf,textvariable=n,fg='blue',bg='yellow',width=60)
name.grid(column=2,row=7)

email=Entry(rf,textvariable=e,fg='blue',bg='yellow',width=60)
email.grid(column=2,row=8)

gender=IntVar()
tk.Radiobutton(rf,text='Male',padx=5,variable=gender,value=1,bg='white',fg='black').grid(column=1,row=9)
tk.Radiobutton(rf,text='Female',padx=5,variable=gender,value=2,bg='white',fg='black').grid(column=2,row=9)

country=StringVar()
country.set('Select your Country')
cou=OptionMenu(rf,country,'Pakistan','America','China','India','Bangladesh','Russia','Iran','Iraq','Saudi Arabia')
cou.grid(row=10,column=2)

program=IntVar()
pro=Checkbutton(rf,text='Java',variable=program)
pro.grid(column=1,row=11)


program1=IntVar()
pro1=Checkbutton(rf,text='Python',variable=program1)
pro1.grid(column=2,row=11)

def submition():
    print("Registration Successful")



sub=Button(rf,text='Submit',command=submition,fg='white',bg='red',font='times18')
sub.grid(column=0,row=13)


rf.mainloop()
