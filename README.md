## คลังสินค้า

ในคลังสินค้า สินค้าจะถูกเก็บไว้ในตำแหน่งเฉพาะบนตาราง โดยแต่ละตำแหน่งสามารถมีสินค้าหลายรายการได้ แต่สินค้าทุกชิ้นควรถูกบันทึกเพียงครั้งเดียวในตำแหน่งนั้น ๆ นักศึกษามีหน้าที่สร้างโปรแกรมที่อ่านข้อมูลการจัดเก็บสินค้าและเก็บข้อมูลไว้ในพจนานุกรม (dictionary) โดยมี key เป็น tuple ที่แทนพิกัด (x, y) และ value เป็นเซ็ต (set) ของชื่อสินค้า จากนั้นสร้างพจนานุกรมใหม่เพื่อแสดงว่าแต่ละตำแหน่ง (x, y) มีจำนวนชนิดของสินค้าเท่าใด และแสดงผลลัพธ์ (output) ที่ได้

## ข้อมูลนำเข้า
บรรทัดแรกจะระบุจำนวนรอบที่ใช้ในการวนรับข้อมูล โดยในแต่ละรอบ โปรแกรมจะวนรับข้อมูล

* พิกัด x (int) เช่น 2
* พิกัด y (int) เช่น -1
* ชื่อสินค้า (str) เช่น apple
  
**Input:**
  
ผู้ใช้ input `num` = 7
```
7
1
2
banana
2
-1
apple
1
2
banana
1
2
apple
1
2
apple
5
5
coke
1
2
apple
```
## ข้อมูลส่งออก
จากข้อมูลด้านบนจะได้ dictionary เป็น 
```
{(1, 2): {'apple', 'banana'}, (2, -1): {'apple'}, (5, 5): {'coke'}}

```
จากนั้นให้ทำการนับจำนวนชนิดสินค้าเพื่อสร้างเป็น output

```
{(1, 2): 2, (2, -1): 1, (5, 5): 1}

```

## ตัวอย่าง1
**Input:**
```
10
6
7
coke
1
-10
coke
-10
1
apple
6
7
coke
1
-10
coke
6
7
coke
6
7
coke
-1
-1
cheese
1
-10
grape
-1
-1
ham
```
**Output:**
```
{(6, 7): 1, (1, -10): 2, (-10, 1): 1, (-1, -1): 2}

```
## ตัวอย่าง2
**Input:**
```
10
-1
-1
item002
-1
-1
item002
1
-1
item002
1
-1
item004
-1
1
item002
1
1
item001
-1
-1
item001
-1
-1
item002
-1
1
item002
-1
-1
item001
```
**Output:**
```
{(-1, -1): 2, (1, -1): 2, (-1, 1): 1, (1, 1): 1}

```
