# Simple-Calculator
#import tkinter to the root 
#input the values, sign, lable, button
#use get() set() to retrive the values and sign
#main code of calculator



import tkinter as tk
from tkinter import *

root =tk. Tk()
root.geometry("600x350")
root.title("Simple Calculator")

def calculator():
    v1=var_val1.get()
    v2=var_val2.get()
    s=var_sign.get()
    
    result=0

    if s=='+':
        result= (float(v1) + float(v2))
    elif s=='-':
        result= (float(v1) - float(v2))
    elif s=='*':
        result= (float(v1) * float(v2))
    elif s=='/':
        result= (float(v1) / float(v2))
    elif s=='%':
        result= (float(v1) % float(v2))

    text="Your result is: "+str(result)
    var_lbl.set(text)

var_val1= StringVar()
var_val1.set("first_val")
var_sign= StringVar()
var_sign.set("sign")
var_val2= StringVar()
var_val2.set("second_val")

var_lbl = StringVar()
var_lbl.set("Result shown here")
    
first_val= Entry(root, textvariable= var_val1, width=20).place(x=100, y=100)
sign= Entry(root, textvariable= var_sign, width=10).place(x=280, y=100)
second_val= Entry(root, textvariable= var_val2, width=20).place(x=400,y=100)

btn= Button(root, command= calculator, text="Calculate").place(x=265, y=140)
lbl= Label(root, textvariable= var_lbl).place(x=265, y=200)

root.mainloop()
