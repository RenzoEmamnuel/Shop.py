from tkinter import *

window = Tk()
window.title("Renzo's Shop")
window.geometry("620x450")
window.config(background="#d1d1e9")

lbl_title = Label(
    window,
    text="School Supplies",
    font=("Courier", 15, "bold", "italic"),
    fg="#2b2c34",
    relief=SUNKEN,
    bd=5,
    padx=10,
    pady=5,
)
lbl_title.pack()

frame_supplies = Frame(window, width=510, height=350)
frame_supplies.pack()
lbl_product = Label(
    frame_supplies,
    text="Product",
    font=("Times", 14),
    padx=10,
    relief=SUNKEN,
    bd=3,
)
lbl_product.place(x=20, y=30)

lbl_pencil = Label(
    frame_supplies,
    text="Pencil",
    font=("Arial", 10),
)

lbl_pencil.place(x=40, y=70)
lbl_product = Label(
    frame_supplies,
    text="  Price   ",
    font=("Times", 14),
    padx=10,
    relief=SUNKEN,
    bd=3,
)
lbl_product.place(x=20, y=30)
lbl_price = Label(
    frame_supplies,
    text="Price",
    font=("Times", 14),
    padx=10,
    relief=SUNKEN,
    bd=3,
)
lbl_product.place(x=140, y=30)
lbl_price_pencil = Label(
    frame_supplies,
    text="P 15.00",
    font=("Ariel", 10)
)
lbl_price_pencil.place(x=155, y=70)

lbl_pen = Label(
    frame_supplies,
    text="Pen",
    font=("Arial", 10),
)
lbl_pen.place(x=43, y=100)
lbl_price_pen = Label(
    frame_supplies,
    text="P 25.00",
    font=("Arial", 10),
)
lbl_price_pen.place(x=155, y=100)

lbl_yellow_pad = Label(
    frame_supplies,
    text="Yellow Pad",
    font=("Arial", 10),
)
lbl_yellow_pad.place(x=30, y=130)
lbl_price_yellow_pad = Label(
    frame_supplies,
    text="P 2.00",
    font=("Arial", 10),
)
lbl_price_yellow_pad.place(x=155, y=130)

lbl_bondpaper = Label(
    frame_supplies,
    text="Bondpaper",
    font=("Arial", 10),
)
lbl_bondpaper.place(x=30, y=160)
lbl_price_bondpaper = Label(
    frame_supplies,
    text="P 1.00",
    font=("Arial", 10),
)
lbl_price_bondpaper.place(x=155, y=160)

lbl_color = Label(
    frame_supplies,
    text="Color",
    font=("Arial", 10),
)
lbl_color.place(x=43, y=190)
lbl_price_color = Label(
    frame_supplies,
    text="P 45.50",
    font=("Arial", 10),
)
lbl_price_color.place(x=155, y=190)

lbl_quantity = Label(
    frame_supplies,
    text="Quantity",
    font=("Times", 14),
    padx=10,
    relief=SUNKEN,
    bd=3,
)
lbl_quantity.place(x=260, y=30)

ent_pencil = Entry(frame_supplies,width=5)
ent_pencil.place(x=280,y=70)

ent_pen = Entry(frame_supplies,width=5)
ent_pen.place(x=280,y=100)

ent_yellowpad = Entry(frame_supplies,width=5)
ent_yellowpad.place(x=280,y=130)

ent_bondpaper = Entry(frame_supplies,width=5)
ent_bondpaper.place(x=280,y=160)

ent_color = Entry(frame_supplies,width=5)
ent_color.place(x=280,y=190)
lbl_amount = Label(
    frame_supplies,
    text="Amount",
    font=("Times", 14),
    padx=10,
    relief=SUNKEN,
    bd=3,
)
lbl_amount.place(x=390, y=30)

items = {
    "Pencil":15.00,
    "Pen":25.00,
    "Yellow Pad":2.00,
    "Bond Paper":1.00,
    "Color":45.50,
}
def checkout():
    a = int(ent_pencil.get()) * items.get("Pencil")
    b = int(ent_pen.get()) * items.get("Pen")
    c = int(ent_yellowpad.get()) * items.get("Yellow Pad")
    d = int(ent_bondpaper.get()) * items.get("Bond Paper")
    e = int(ent_color.get()) * items.get("Color")

    total_amount = a + b + c + d + e
    amounts = [
        f"P {a:.2f}",
        f"P {b:.2f}",
        f"P {c:.2f}",
        f"P {d:.2f}",
        f"P {e:.2f}",
        f"Sub-Total: P {total_amount:.2f} "
    ]
    Tax = total_amount*0.10 +total_amount
    Total = f"Total: P {Tax} with 10% VAT"
    Cash = "Cash:"
    Change = "Change:"
    lbl_checkout_amount.config(text="\n".join(amounts))
    lbl_total.config(text=Total)
    lbl_cash.config(text=Cash)
    ent_cash = Entry(frame_supplies,width=5)
    ent_cash.place(x=180,y=285)
    btn_text_cash = "OK"
    btn_cash.config(text=btn_text_cash)
    btn_cash.place(x=220,y=280)
    lbl_change.config(text=Change)
    def ok():
        btn_ok_command = int(ent_cash.get())-Tax
        Money_change.config(text=f"P {btn_ok_command:.2f}")
    btn_cash.config(command=ok)
btn_checkout = Button(frame_supplies,text="Check Out",command=checkout)
btn_checkout.place(x=400,y=210)

lbl_checkout_amount = Label(frame_supplies, text="", font=("times", 13))
lbl_checkout_amount.place(x=360, y=70)
lbl_total = Label(frame_supplies, text="", font=("Courier", 13,))
lbl_total.place(x=120, y=250)
lbl_cash = Label(frame_supplies,text="",font=("Courier", 13,))
lbl_cash.place(x=120,y=280)
lbl_change = Label(frame_supplies,text="",font=("Courier", 13,))
lbl_change.place(x=250,y=280)
btn_cash = Button(frame_supplies,text="",)
Money_change = Label(frame_supplies,font=("Courier", 13,"underline","bold"),text="")
Money_change.place(x = 320,y =280)
window.mainloop()


