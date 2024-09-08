import pygame 
from tkinter import*       
from tkinter import messagebox
import tkinter as tk
from PIL import Image, ImageTk
from tkinter import filedialog
from pygame import mixer
pygame.mixer.init()
list_name = []
list_pass = []
root = Tk() 
photo = PhotoImage(file = 'logo.png')
root.wm_iconphoto(False, photo)
root.title("login mmd player")
root.geometry("300x400")
root.resizable(width=False,height=False)
back_image = tk.PhotoImage(file='logo.png')
back_image_lable = tk.Label(root,image=back_image)
back_image_lable.place(x=0,y=0,relwidth=1,relheight=1) 
def close ():
       root.destroy()
def login():
        str = StringVar
        username = userEntry.get()
        passname = passEntry.get()
        if username == '1234' and passname == '1234':
                messagebox.showinfo('','your name and password is true \n wellcome to your panel')
                root.destroy()
                import test 
        for username in list_name:         
                if username == list_name and passname == list_pass :
                    messagebox.showinfo('','your name and password is true \n wellcome to your panel')
                root.destroy()
                import test                                       
        if userEntry == '' and passEntry== "":
                 messagebox.showinfo("","enter your real name and password")
def singup (): 
        def sing ():
              username2 = userEntry2.get()
              pass2 = passEntry2.get()
              list_name.append(username2)
              list_pass.append(pass2)
              messagebox.showinfo('','sing up was successful')
              root.destroy()
        def exi ():
               root.destroy()      
        str = StringVar
        messagebox.showinfo('','wellcome to sing up page lets start')
        root = Tk()
        root.title = ('sing up mmd player')
        root.geometry('300x300')
        root.resizable(width=False,height=False)
        userEntry2 = Entry(root)
        userEntry2.place(x=160,y=40)  
        userLable2 = Label(root,text='enter your user name :' , bg='lightblue')
        userLable2.place(y=40,x=10)
        passEntry2 = Entry(root)
        passEntry2.place(x=160,y=80)
        passLable = Label(root , text = 'enter your password :' , bg="lightblue")
        passLable.place(x=10, y=80)
        age_spin = tk.Spinbox(root,from_=18,to=99).place(x=160,y=120)
        ageLable = Label(root,text='enter your age :' , bg='lightblue')
        ageLable.place(x=10,y=120)
        buttonS1 = Button(root,text= 'sing up' , bg='#d1aded', command=sing)
        buttonS1.place(x=80,y=220)
        buttonS2 = Button(root,text='Exit',bg='yellow' , command=exi)
        buttonS2.place(x=210,y=220)
        root.mainloop()
def guiiiii ():
       messagebox.showinfo('', 'you can use beta app')
       root.destroy()
       import test      
userEntry = Entry(root,bg='lightyellow')
userEntry.place(x=160,y=80)  
userLable = Label(root,text='enter your user name :' , bg='lightblue')
userLable.place(y=80,x=10)
passEntry = Entry(root , bg='lightyellow' , show='*')
passEntry.place(x=160,y=160)
passwordLable = Label(root,text='enter your password : ' , bg='lightblue')
passwordLable.place(y=160,x=10)
button = Button(text ='sing up' , bg='#d1aded' , command=singup ,).place(x=80,y=220)
button2 = Button(text='log in' , bg = '#cfefb5' , command=login).place(x=210,y=220)
button3 = Button(text='gusset' , bg ='#fff000'  , command=guiiiii).place(x=145,y=220)     
root.mainloop()                    
