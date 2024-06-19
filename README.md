import tkinter as tk
from time import strftime

# สร้างหน้าต่างหลัก
root = tk.Tk()
root.title("นาฬิกาดิจิตอล")

# ฟังก์ชันสำหรับรับเวลาปัจจุบันและแสดงบน Label
def time():
    string = strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000, time)

# สร้าง Label สำหรับแสดงเวลา
label = tk.Label(root, font=('calibri', 40, 'bold'), background='purple', foreground='white')
label.pack(anchor='center')

time()  # เรียกใช้ฟังก์ชันเพื่อเริ่มต้นการแสดงเวลา

# แสดงหน้าต่าง
root.mainloop()
