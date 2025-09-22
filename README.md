# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         2000               |     64                   |
|2001 |65|
|2002|72|
|2003|83|

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 10 01 59_016f7e33](https://github.com/user-attachments/assets/cfd975c8-15c6-4f21-baf7-0bedde99bf43)


## OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 10 02 25_d2f68fcd](https://github.com/user-attachments/assets/5034b345-633a-4ef8-b676-49e1adca1ce9)

----
## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   20001                      |     45                     |
|2002  | 63 |
|2003 | 76 |
|2004 | 98 |
#### Manual Calculations

(Add your calculation here) 

![WhatsApp Image 2025-09-22 at 10 24 58_e9ef81c2](https://github.com/user-attachments/assets/41a2c0d6-2b5d-4c77-a93a-81196c96ebcf)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 10 02 25_db071694](https://github.com/user-attachments/assets/a2477d19-aec1-4686-b231-133940873d93)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   2000                      |     04                     |
|2001 |  06 |
|2002 | 02 |
|2004 | 98 |
#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-09-22 at 10 01 59_5ac3bc36](https://github.com/user-attachments/assets/3e1ee313-5c41-4bd9-a51a-16d9e568839f)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 10 02 26_251e710f](https://github.com/user-attachments/assets/48409139-04f6-4121-bcd4-b615b514b4a0)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  2000                       |   69|
|2001|24|
| 2002| 34|
|2003|12 |

#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-09-22 at 10 02 00_b65429b2](https://github.com/user-attachments/assets/c8730c16-b513-4bbc-a691-9f2fdc832fe0)

---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 10 02 27_512ebd47](https://github.com/user-attachments/assets/3337171b-232d-4308-b717-5a7c003f61f7)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

