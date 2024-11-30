import math
from turtle import *

# دالة رسم القلب بناءً على معادلات رياضية
def hearta(k):
    return 16 * math.sin(k)**3

def heartb(k):
    return 13 * math.cos(k) - 5 * math.cos(2*k) - 2 * math.cos(3*k) - math.cos(4*k)

# إعدادات السلحفاة
speed(0)
bgcolor("black")  # خلفية سوداء

# إعداد اللون
color("red")

# بدء الرسم
penup()
goto(0, -200)  # تغيير الموقع البداية
pendown()

# رسم القلب
for i in range(1000):
    x = hearta(i * 0.1) * 20  # تحديد موقع x
    y = heartb(i * 0.1) * 20  # تحديد موقع y
    goto(x, y)

# إنهاء الرسم
done()


