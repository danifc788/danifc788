import tkinter as tk
from tkinter import messagebox

def verificar():
    if entrada1.get()>='18':
        messagebox.showinfo("AVISO","Usted es mayor de edad")
    else:
        messagebox.showwarning("AVISO","Usted es menor de edad")

def cv():
    ventana.destroy()

def callback(event):
    verificar()

ventana=tk.Tk()
ventana.title("VERIFICAR")
ventana.geometry('300x300')
ventana.configure(background='blue')
ventana.bind('<Return>', callback)
e1=tk.Label(ventana,text="EDAD:",bg="yellow",fg="green")
e1.pack(padx=5,pady=5,ipadx=5,ipady=5)
entrada1=tk.Entry(ventana)
entrada1.pack(padx=5,pady=5,ipadx=5,ipady=5)
boton=tk.Button(ventana,text="VERIFICAR",fg='red',command=verificar)
boton.pack(side=tk.TOP)
ventana.mainloop()
