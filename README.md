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
|  1200: 31               |	1204: 62               |
|  1201: 12               |	1205: 24               |
|  1202: 31	              |   1206: 00               |
|  1203: 12	              |   1207: C4               |                          |

#### Manual Calculations

(Add your calculation here)
![add manual](https://github.com/user-attachments/assets/5dd34b4f-d05b-48f3-94d3-c5a29b5949d7)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![MASM add1](https://github.com/user-attachments/assets/0201d116-5055-4422-ae41-50c4abd13dba)
![MASM add1 1](https://github.com/user-attachments/assets/084adfcc-9b56-446b-8d7a-bba7fb6caa06)

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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200: 31                |   	1204: 00            |
| 1201: 12                |   	1205: 00            |
| 1202: 31                |   	1206: 00            |
| 1203: 12                |  	   1207: C4            |
                                                

#### Manual Calculations

(Add your calculation here)
![sub manual](https://github.com/user-attachments/assets/2093e9ca-1280-4662-a158-a2f415164b21)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![MASM sub 2](https://github.com/user-attachments/assets/d8dd66be-1725-4159-8826-ac345acbb6fa)
![MASM sub 2 1](https://github.com/user-attachments/assets/12d2a0cc-08d5-404d-a027-04a199d7ef59)

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
|    1200: 31	            |            1204: 61      |
|    1201: 12	            |            1205: ED      |
|    1202: 31             |            1206: 4A      |
|    1203: 12             |            1207: 01     |    

#### Manual Calculations

(Add your calculation here)
![mul manual](https://github.com/user-attachments/assets/fb79f06a-d9e7-435d-bce8-079edfc89507)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![MASM mul 3 1](https://github.com/user-attachments/assets/4b0c3bbe-7a11-4946-8c41-67b526a9509e)
![MASM mul 3](https://github.com/user-attachments/assets/69b8bd17-3c86-4478-8364-5760685c360c)

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
|   1200: 31	            |          1204: 01        |
|   1201: 12              |          1205: 00        |
|   1202: 31              |          1206: 00        |
|   1203: 12              |          1207: 00        |                    |                          |

#### Manual Calculations

(Add your calculation here)
![div manual](https://github.com/user-attachments/assets/658bd10b-33f7-46cb-870f-35ba0978388c)

---
## OUTPUT FROM MASM SOFTWARE
![MASM div 4 1](https://github.com/user-attachments/assets/bf1aa388-0bf0-4098-a123-b93a6465d2aa)
![MASM div 4](https://github.com/user-attachments/assets/5ac4cb80-7c57-4c92-9850-8664f27f288e)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
