# billing-system

from tkinter import *
import random
from tkinter import IntVar

class Bill_App:
    def __init__(self,root):
        self.root = root
        self.root.geometry("1300x700+0+0")
        self.root.maxsize(width = 1280,height = 700)
        self.root.minsize(width = 1280,height = 700)
        self.root.title("Billing Software")
        
        #====================Variables========================#
        self.cus_name = StringVar()
        self.c_phone = StringVar()
        #For Generating Random Bill Numbers
        x = random.randint(1000,9999)
        self.c_bill_no = StringVar()
        #Seting Value to variable
        self.c_bill_no.set(str(x))

        self.burger = IntVar()
        self.noodles = IntVar()
        self.soup = IntVar()
        self.sandwich = IntVar()
        self.butterchicken = IntVar()
        self.palakpaneer = IntVar()
        self.daal = IntVar()    
        self.ButterNaan = IntVar()
        self.maza = IntVar()
        self.coke = IntVar()
        self.frooti = IntVar()
        self.nimko = IntVar()
        self.biscuits = IntVar()
        self.total_fastfood = StringVar()
        self.total_maincourse = StringVar()
        self.total_other = StringVar()
        self.tax_fast = StringVar()
        self.tax_main = StringVar()
        self.tax_other = StringVar()
        self.total_fastfood_price = IntVar()
        self.total_maincourse_price = IntVar()
        self.total_other_prices = IntVar()
        


        #===================================
        bg_color = "#074463"
        fg_color = "white"
        lbl_color = 'white'
        #Title of App
        title = Label(self.root,text = "Billing Software",bd = 12,relief = GROOVE,fg = fg_color,bg = bg_color,font=("times new roman",30,"bold"),pady = 3).pack(fill = X)

        #==========Customers Frame==========#
        F1 = LabelFrame(text = "Customer Details",font = ("time new roman",12,"bold"),fg = "gold",bg = bg_color,relief = GROOVE,bd = 10)
        F1.place(x = 0,y = 80,relwidth = 1)

        #===============Customer Name===========#
        cname_lbl = Label(F1,text="Customer Name",bg = bg_color,fg = fg_color,font=("times new roman",15,"bold")).grid(row = 0,column = 0,padx = 10,pady = 5)
        cname_en = Entry(F1,bd = 8,relief = GROOVE,textvariable = self.cus_name)
        cname_en.grid(row = 0,column = 1,ipady = 4,ipadx = 30,pady = 5)

        #=================Customer Phone==============#
        cphon_lbl = Label(F1,text = "Phone No",bg = bg_color,fg = fg_color,font = ("times new roman",15,"bold")).grid(row = 0,column = 2,padx = 20)
        cphon_en = Entry(F1,bd = 8,relief = GROOVE,textvariable = self.c_phone)
        cphon_en.grid(row = 0,column = 3,ipady = 4,ipadx = 30,pady = 5)

        #====================Customer Bill No==================#
        cbill_lbl = Label(F1,text = "Bill No.",bg = bg_color,fg = fg_color,font = ("times new roman",15,"bold"))
        cbill_lbl.grid(row = 0,column = 4,padx = 20)
        cbill_en = Entry(F1,bd = 8,relief = GROOVE,textvariable = self.c_bill_no)
        cbill_en.grid(row = 0,column = 5,ipadx = 30,ipady = 4,pady = 5)
        
        #====================Bill Search Button===============#
        bill_btn = Button(F1,text = "Enter",bd = 7,relief = GROOVE,font = ("times new roman",12,"bold"),bg = bg_color,fg = fg_color)
        bill_btn.grid(row = 0,column = 6,ipady = 5,padx = 60,ipadx = 19,pady = 5)

        #==================fast food Frame=====================#
        F2 = LabelFrame(self.root,text = 'Fast food',bd = 10,relief = GROOVE,bg = bg_color,fg = "gold",font = ("times new roman",13,"bold"))
        F2.place(x = 5,y = 180,width = 325,height = 380)

        #===========Frame Content
        burger_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Burger")
        burger_lbl.grid(row = 0,column = 0,padx = 10,pady = 20)
        burger_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.burger)
        burger_en.grid(row = 0,column = 1,ipady = 5,ipadx = 5)

        #=======noodles
        noodles_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Noodles")
        noodles_lbl.grid(row = 1,column = 0,padx = 10,pady = 20)
        noodles_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.noodles)
        noodles_en.grid(row = 1,column = 1,ipady = 5,ipadx = 5)

  

        #========soup
        soup_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Soup")
        soup_lbl.grid(row = 3,column = 0,padx = 10,pady = 20)
        soup_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.soup)
        soup_en.grid(row = 3,column = 1,ipady = 5,ipadx = 5)

        #============Sandwich
        sandwich_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Sandwich")
        sandwich_lbl.grid(row = 4,column = 0,padx = 10,pady = 20)
        sandwich_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.sandwich)
        sandwich_en.grid(row = 4,column = 1,ipady = 5,ipadx = 5)

        #==================main course=====================#
        F2 = LabelFrame(self.root,text = 'main course',bd = 10,relief = GROOVE,bg = bg_color,fg = "gold",font = ("times new roman",13,"bold"))
        F2.place(x = 330,y = 180,width = 325,height = 380)

        #===========Frame Content
        butterchicken_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Butter Chicken")
        butterchicken_lbl.grid(row = 0,column = 0,padx = 10,pady = 20)
        butterchicken_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.butterchicken)
        butterchicken_en.grid(row = 0,column = 1,ipady = 5,ipadx = 5)

        #=======
        palakpaneer_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Palak Paneer")
        palakpaneer_lbl.grid(row = 1,column = 0,padx = 10,pady = 20)
        palakpaneer_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.palakpaneer)
        palakpaneer_en.grid(row = 1,column = 1,ipady = 5,ipadx = 5)

        #=======
        daal_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Daal")
        daal_lbl.grid(row = 2,column = 0,padx = 10,pady = 20)
        daal_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.daal)
        daal_en.grid(row = 2,column = 1,ipady = 5,ipadx = 5)

        #========
        ButterNaan_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Butter Naan")
        ButterNaan_lbl.grid(row = 3,column = 0,padx = 10,pady = 20)
        ButterNaan_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.ButterNaan)
        ButterNaan_en.grid(row = 3,column = 1,ipady = 5,ipadx = 5)

        #============
       

        #==================Other Stuff=====================#

        F2 = LabelFrame(self.root,text = 'Others',bd = 10,relief = GROOVE,bg = bg_color,fg = "gold",font = ("times new roman",13,"bold"))
        F2.place(x = 655,y = 180,width = 325,height = 380)

        #===========Frame Content
        maza_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Maza")
        maza_lbl.grid(row = 0,column = 0,padx = 10,pady = 20)
        maza_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.maza)
        maza_en.grid(row = 0,column = 1,ipady = 5,ipadx = 5)

        #=======
        cock_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Coke")
        cock_lbl.grid(row = 1,column = 0,padx = 10,pady = 20)
        cock_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.coke)
        cock_en.grid(row = 1,column = 1,ipady = 5,ipadx = 5)

        #=======
        frooti_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Frooti")
        frooti_lbl.grid(row = 2,column = 0,padx = 10,pady = 20)
        frooti_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.frooti)
        frooti_en.grid(row = 2,column = 1,ipady = 5,ipadx = 5)

        #========
        cold_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Nimkos")
        cold_lbl.grid(row = 3,column = 0,padx = 10,pady = 20)
        cold_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.nimko)
        cold_en.grid(row = 3,column = 1,ipady = 5,ipadx = 5)

        #============
        bis_lbl = Label(F2,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Biscuits")
        bis_lbl.grid(row = 4,column = 0,padx = 10,pady = 20)
        bis_en = Entry(F2,bd = 8,relief = GROOVE,textvariable = self.biscuits)
        bis_en.grid(row = 4,column = 1,ipady = 5,ipadx = 5)

        #===================Bill Aera================#
        F3 = Label(self.root,bd = 10,relief = GROOVE)
        F3.place(x = 960,y = 180,width = 325,height = 380)
        #===========
        bill_title = Label(F3,text = "Bill Area",font = ("Lucida",13,"bold"),bd= 7,relief = GROOVE)
        bill_title.pack(fill = X)

        #============
        scroll_y = Scrollbar(F3,orient = VERTICAL)
        self.txt = Text(F3,yscrollcommand = scroll_y.set)
        scroll_y.pack(side = RIGHT,fill = Y)
        scroll_y.config(command = self.txt.yview)
        self.txt.pack(fill = BOTH,expand = 1)

        #===========Buttons Frame=============#
        F4 = LabelFrame(self.root,text = 'Bill Menu',bd = 10,relief = GROOVE,bg = bg_color,fg = "gold",font = ("times new roman",13,"bold"))
        F4.place(x = 0,y = 560,relwidth = 1,height = 145)

        #===================
        fastfood_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "fast food")
        fastfood_lbl.grid(row = 0,column = 0,padx = 10,pady = 0)
        fastfood_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.total_fastfood)
        fastfood_en.grid(row = 0,column = 1,ipady = 2,ipadx = 5)

        #===================
        maincourse_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Main course")
        maincourse_lbl.grid(row = 1,column = 0,padx = 10,pady = 5)
        maincourse_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.total_maincourse)
        maincourse_en.grid(row = 1,column = 1,ipady = 2,ipadx = 5)

        #================
        oth_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Others Total")
        oth_lbl.grid(row = 2,column = 0,padx = 10,pady = 5)
        oth_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.total_other)
        oth_en.grid(row = 2,column = 1,ipady = 2,ipadx = 5)

        #================
        fastfood_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "fast food Tax")
        fastfood_lbl.grid(row = 0,column = 2,padx = 30,pady = 0)
        fastfood_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.tax_fast)
        fastfood_en.grid(row = 0,column = 3,ipady = 2,ipadx = 5)

        #=================
        maincourse_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Main course Tax")
        maincourse_lbl.grid(row = 1,column = 2,padx = 30,pady = 5)
        maincourse_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.tax_main)
        maincourse_en.grid(row = 1,column = 3,ipady = 2,ipadx = 5)

        #==================
        otht_lbl = Label(F4,font = ("times new roman",15,"bold"),fg = lbl_color,bg = bg_color,text = "Others Tax")
        otht_lbl.grid(row = 2,column = 2,padx = 10,pady = 5)
        otht_en = Entry(F4,bd = 8,relief = GROOVE,textvariable = self.tax_other)
        otht_en.grid(row = 2,column = 3,ipady = 2,ipadx = 5)

        #====================
        total_btn = Button(F4,text = "Total",bg = bg_color,fg = fg_color,font=("lucida",12,"bold"),bd = 7,relief = GROOVE,command = self.total)
        total_btn.grid(row = 1,column = 4,ipadx = 20,padx = 30)

        #========================
        genbill_btn = Button(F4,text = "Generate Bill",bg = bg_color,fg = fg_color,font=("lucida",12,"bold"),bd = 7,relief = GROOVE,command = self.bill_area)
        genbill_btn.grid(row = 1,column = 5,ipadx = 20)

        #====================
        clear_btn = Button(F4,text = "Clear",bg = bg_color,fg = fg_color,font=("lucida",12,"bold"),bd = 7,relief = GROOVE,command = self.clear)
        clear_btn.grid(row = 1,column = 6,ipadx = 20,padx = 30)

        #======================
        exit_btn = Button(F4,text = "Exit",bg = bg_color,fg = fg_color,font=("lucida",12,"bold"),bd = 7,relief = GROOVE,command = self.exit)
        exit_btn.grid(row = 1,column = 7,ipadx = 20)

#Function to get total prices
    def total(self):
        #=================Total Fast food
        self.total_fastfood_price = (
            (self.burger.get() *         40)+
            (self.noodles.get() *        40)+
            (self.soup.get() *          100)+
            (self.sandwich.get() *       80)
           
        )
        self.total_fastfood.set("Rs. "+str(self.total_fastfood_price))
        self.tax_fast.set("Rs. "+str(round(self.total_fastfood_price*0.05)))
        #====================Total main couse
        self.total_maincourse_price = (
            (self.butterchicken.get()*  180)+
            (self.palakpaneer.get() *   180)+
            (self.daal.get() *          100)+
            (self.ButterNaan.get() *     32)
            

        )
        self.total_maincourse.set("Rs. "+str(self.total_maincourse_price))
        self.tax_main.set("Rs. "+str(round(self.total_maincourse_price*0.05)))
        #======================Total Other Prices
        self.total_other_prices = (
            (self.maza.get() *          20)+
            (self.frooti.get() *        50)+
            (self.coke.get() *          60)+
            (self.nimko.get() *         20)+
            (self.biscuits.get() *      20)
        )
        self.total_other.set("Rs. "+str(self.total_other_prices))
        self.tax_other.set("Rs. "+str(round(self.total_other_prices*0.05)))


#Function For Text Area
    def welcome_soft(self):
        self.txt.delete('1.0',END)
        self.txt.insert(END,"       Welcome To farzi Dhaba\n")
        self.txt.insert(END,f"\nBill No. : {str(self.c_bill_no.get())}")
        self.txt.insert(END,f"\nCustomer Name : {str(self.cus_name.get())}")
        self.txt.insert(END,f"\nPhone No. : {str(self.c_phone.get())}")
        self.txt.insert(END,"\n===================================")
        self.txt.insert(END,"\nProduct          Qty         Price")
        self.txt.insert(END,"\n===================================")

#Function to clear the bill area
    def clear(self):
        self.txt.delete('1.0',END)

#Add Product name , qty and price to bill area
    def bill_area(self):
        self.welcome_soft()
        if self.burger.get() != 0:
            self.txt.insert(END,f"\nburger            {self.burger.get()}           {self.burger.get() *       40}")
        if self.noodles.get() != 0:
            self.txt.insert(END,f"\nnoodles           {self.noodles.get()}           {self.noodles.get() *      40}")
        if self.soup.get() != 0:
            self.txt.insert(END,f"\nsoup              {self.soup.get()}           {self.soup.get() *        100}")
        if self.sandwich.get() != 0:
            self.txt.insert(END,f"\nsandwich          {self.sandwich.get()}           {self.sandwich.get() *     80}")
       
        if self.butterchicken.get() != 0:
            self.txt.insert(END,f"\nbutterchicken     {self.butterchicken.get()}           {self.butterchicken.get() *180}")
        if self.palakpaneer.get() != 0:
            self.txt.insert(END,f"\npalakpaneer       {self.palakpaneer.get()}           {self.palakpaneer.get() *  180}")
        if self.daal.get() != 0:
            self.txt.insert(END,f"\nDaal              {self.daal.get()}           {self.daal.get() *         100}")
        if self.ButterNaan.get() != 0:
            self.txt.insert(END,f"\nButterNaan        {self.ButterNaan.get()}           {self.ButterNaan.get() *    32}")
        
        if self.maza.get() != 0:
            self.txt.insert(END,f"\nMaza              {self.maza.get()}           {self.maza.get() *          20}")
        if self.frooti.get() != 0:
            self.txt.insert(END,f"\nFrooti            {self.frooti.get()}           {self.frooti.get() *        50}")
        if self.coke.get() != 0:
            self.txt.insert(END,f"\nCoke              {self.coke.get()}           {self.coke.get() *          60}")
        if self.nimko.get() != 0:
            self.txt.insert(END,f"\nNimko             {self.nimko.get()}           {self.nimko.get() *         20}")
        if self.biscuits.get() != 0:
            self.txt.insert(END,f"\nBiscuits          {self.biscuits.get()}           {self.biscuits.get() *      20}")
        self.txt.insert(END,"\n===================================")
        self.txt.insert(END,f"\n                   Total : {self.total_fastfood_price+self.total_maincourse_price+self.total_other_prices+self.total_fastfood_price * 0.05+self.total_maincourse_price * 0.05+self.total_other_prices * 0.05}")


    #Function to exit
    def exit(self):
        self.root.destroy()

    #Function To Clear All Fields


        


root = Tk()
object = Bill_App(root)
root.mainloop()

