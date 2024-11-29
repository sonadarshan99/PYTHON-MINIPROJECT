# Import Module
from tkinter import *

# Create Object
root = Tk()
root.title(&quot;Address Book&quot;)

# Set geometry
root.geometry(&#39;400x500&#39;)

# Information List
datas = []

# Add Information
def add():
global datas
datas.append([Name.get(),Number.get(),address.get(1.0, &quot;end-1c&quot;)])
update_book()

# View Information
def view():
Name.set(datas[int(select.curselection()[0])][0])
Number.set(datas[int(select.curselection()[0])][1])
address.delete(1.0,&quot;end&quot;)
address.insert(1.0, datas[int(select.curselection()[0])][2])

# Delete Information

def delete():
del datas[int(select.curselection()[0])]
update_book()

def reset():
Name.set(&#39;&#39;)
Number.set(&#39;&#39;)
address.delete(1.0,&quot;end&quot;)

# Update Information
def update_book():
select.delete(0,END)
for n,p,a in datas:
select.insert(END, n)

# Add Buttons, Label, ListBox
Name = StringVar()
Number = StringVar()

frame = Frame()
frame.pack(pady=10)

frame1 = Frame()
frame1.pack()

frame2 = Frame()

frame2.pack(pady=10)

Label(frame, text = &#39;Name&#39;, font=&#39;arial 12 bold&#39;).pack(side=LEFT)
Entry(frame, textvariable = Name,width=50).pack()

Label(frame1, text = &#39;Phone No.&#39;, font=&#39;arial 12 bold&#39;).pack(side=LEFT)
Entry(frame1, textvariable = Number,width=50).pack()

Label(frame2, text = &#39;Address&#39;, font=&#39;arial 12 bold&#39;).pack(side=LEFT)
address = Text(frame2,width=37,height=10)
address.pack()

Button(root,text=&quot;Add&quot;,font=&quot;arial 12 bold&quot;,command=add).place(x= 100, y=270)
Button(root,text=&quot;View&quot;,font=&quot;arial 12 bold&quot;,command=view).place(x= 100, y=310)
Button(root,text=&quot;Delete&quot;,font=&quot;arial 12 bold&quot;,command=delete).place(x= 100, y=350)
Button(root,text=&quot;Reset&quot;,font=&quot;arial 12 bold&quot;,command=reset).place(x= 100, y=390)

scroll_bar = Scrollbar(root, orient=VERTICAL)
select = Listbox(root, yscrollcommand=scroll_bar.set, height=12)
scroll_bar.config (command=select.yview)
scroll_bar.pack(side=RIGHT, fill=Y)
select.place(x=200,y=260)

# Execute Tkinter
root.mainloop()
