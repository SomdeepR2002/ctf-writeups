# 🧩 Challenge: Deleted File

**Platform:** RootMe  
**Category:** Forensics  
**Difficulty:** Very Easy  

---

## 🧠 Challenge Summary
Clue:  
> Your cousin found a USB drive in the library this morning. He’s not very good with computers, so he’s hoping you can find the owner of this stick!

The flag is the owner’s identity in the form `firstname_lastname`.

---

## 🔍 Analysis

Downloaded file: `ch39.gz`  
Extracted file: `usb.image`

---

### 🔸 Step 1: Identify File Type

```bash 
file usb.image          
```
![file command output](img1.png)

### 🔸 Step 2: Read File Contents

```bash
cat usb.image
```
![cat command output](img2.png)]

### 🔸 Step 3: Identify Flag

```bash
<rdf:li>Javier Turcot</rdf:li>
```

## ✅ Flag

`javier_turcot`


### 💡 Comments

- Raw tools like `cat` can reveal string hints even without parsing.

##  🛠️ Tools Used

- Linux `file` command
- Linux `cat` command
