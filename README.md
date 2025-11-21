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
|     2000-06             |      2004-1C             |
|     2001-13             |      2005-28             |
|     2002-16             |                          |
|     2003-15             |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-11 at 21 06 19_4d12b867](https://github.com/user-attachments/assets/65993ba6-f3d6-419d-94ac-0571f437acda)

(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="628" height="415" alt="experiment 1 indadd" src="https://github.com/user-attachments/assets/135be13c-92ec-4966-a6fc-cc7cf2de7c43" />


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
|     2000-55             |      2004-33             |
|     2001-55             |      2005-33             |
|     2002-22             |                          |
|     2003-22             |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-11 at 21 23 43_3c1e6fbb](https://github.com/user-attachments/assets/36acd870-52db-470a-8dac-a4ffcebd3307)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="647" height="430" alt="experiment 1 indsub" src="https://github.com/user-attachments/assets/e645df58-017f-42bb-95b4-0b2f1284a3d7" />


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
|     2000-22             |      2004-42             |
|     2001-00             |      2005-02             |
|     2002-11             |                          |
|     2003-00             |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-11 at 21 36 51_0809cce4](https://github.com/user-attachments/assets/cf492f32-f1cd-491b-b1e5-c56aa505f694)

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="646" height="430" alt="experiment 1 indmul" src="https://github.com/user-attachments/assets/c71c3f3b-f979-4c6c-a7cd-d987c04b5c5a" />


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
|     2000-44             |      2004-02             |
|     2001-44             |      2005-00             |
|     2002-22             |                          |
|     2003-22             |                          |

#### Manual Calculations

![WhatsApp Image 2025-11-11 at 21 38 56_cf3c0962](https://github.com/user-attachments/assets/c882eee8-a3c3-498c-b43c-0414fb216c11)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
<img width="637" height="426" alt="experiment 1 inddiv" src="https://github.com/user-attachments/assets/a96db3cf-876d-435e-b413-d44d254c0d06" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

