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
|       1200: 12          |        1204: 24          |
|       1201: 34          |        1205: 68          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |

#### Manual Calculations

<img width="400" height="400" alt="Screenshot 2025-09-03 000224" src="https://github.com/user-attachments/assets/cf32383d-eed2-415c-bd88-4ee5508ad14d" />

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 18 31 50_5d02642d](https://github.com/user-attachments/assets/bb52413a-2f4d-4ac0-bb60-24cc33180c75)
![WhatsApp Image 2025-09-09 at 19 42 17_8c1fbeeb](https://github.com/user-attachments/assets/05f3ba52-c7dc-4842-99a8-e389180cf398)



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
|       1200: 12          |        1204: 00          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: C4          |
#### Manual Calculations

<img width="400" height="400" alt="Screenshot 2025-09-03 000254" src="https://github.com/user-attachments/assets/eeadcb68-b587-4d0d-88ab-196374dbcef7" />

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-09 at 18 51 53_91225ed0](https://github.com/user-attachments/assets/1410a3dc-991a-4050-8428-e5fa8809e88a)
![WhatsApp Image 2025-09-09 at 18 55 49_bb8cd4ae](https://github.com/user-attachments/assets/7e22533f-3e09-41d0-b6f9-26d60dd2d8d1)

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
|       1200: 12          |        1204: 44          |
|       1201: 34          |        1205: 51          |
|       1202: 12          |        1206: 97          |
|       1203: 34          |        1207: 0A          |
#### Manual Calculations
<img width="400" height="400" alt="Screenshot 2025-09-03 000327" src="https://github.com/user-attachments/assets/163f968d-1f20-45ad-9ad5-520b197a7454" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="631" height="389" alt="image" src="https://github.com/user-attachments/assets/25226987-5f0a-42b8-bd5e-423bdf5417d5" />

<img width="630" height="395" alt="image" src="https://github.com/user-attachments/assets/ceea432f-6769-4cf6-a7c4-0d10429ffc46" />



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
|       1200: 12          |        1204: 01          |
|       1201: 34          |        1205: 00          |
|       1202: 12          |        1206: 00          |
|       1203: 34          |        1207: 00          |

#### Manual Calculations

<img width="400" height="400" alt="Screenshot 2025-09-03 000353" src="https://github.com/user-attachments/assets/ce61a799-d563-4b4b-b163-785ca06a4bc3" />

## OUTPUT FROM MASM SOFTWARE
<img width="627" height="386" alt="image" src="https://github.com/user-attachments/assets/311f7225-a9d2-4282-b96a-354916e9ce70" />

![WhatsApp Image 2025-09-09 at 19 29 47_f6800382](https://github.com/user-attachments/assets/01dd98fb-6c4d-4c48-9f46-adfac5d4de5d)





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
