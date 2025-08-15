# Project 1 README

**Student:** Saisidharth Mannava (920691968)

---

## Project Status
The project currently has working implementations for all three problems. Each circuit was built and tested in **Logisim Evolution** using various combinations of inputs to ensure correctness.

---

## Problem 1: Comparator Circuits

I created two separate circuits:
1. **X = Y Circuit** – Output `N` is true when `X` equals `Y`.
2. **X < Y Circuit** – Output `E` is true when `X` is less than `Y`.

### X = Y Circuit
- **Inputs:** `X2`, `X1`, `X0`, `Y2`, `Y1`, `Y0`  
- **Output:** `N` (true if equal)  
- **Implementation:**
  - Used three **XNOR** gates to compare each bit of `X` and `Y`.
  - Fed the XNOR outputs into a **three-input AND** gate so all bits must match.

### X < Y Circuit
- **Inputs:** same as above  
- **Output:** `E` (true if less than)  
- **Implementation:**
  - Used **NOT**, **XNOR**, and **AND** gates.
  - Cross-checked in discussion with the professor.
  - Verified with multiple input combinations.

---

## Problem 2: 4-bit Binary to Gray Code Converter

- My SID’s last digit is **8**, so I used the corresponding Gray code values in column 8.
- **Steps:**
  1. Created a **truth table** with 4 binary input bits.
  2. Retrieved the Gray codes for SID ending in 8.
  3. Built **4-variable K-maps** for each Gray code output (`G0`, `G1`, `G2`, `G3`).
  4. Derived **simplified boolean equations** from each K-map.
  5. Implemented the circuits in Logisim using **AND**, **NAND**, and **OR** gates.
  6. Tested all table inputs to verify outputs.

---

## Problem 3: 7-Segment Display Decoder

This problem was the most challenging. After attending office hours, I treated the **vertical bar** input as a **don’t care**.

- **Inputs:**
  - 3 variables for vertical bars
  - 1 variable for horizontal bar
- **Outputs:** `A`, `B`, `C`, `D`, `E`, `F`, `G` (segment enables)
- **Process:**
  1. Populated a truth table for the required 7-segment patterns.
  2. Defined two input sets in Logisim (vertical vs. horizontal).
  3. Built the decoder from the truth table.
  4. Tested all combinations to confirm correct segment activation.

---

## Known Issues
- In early iterations, the **X < Y** circuit had logic conflicts due to misused NOT gates. Fixed after debugging with the professor.
- The **7-segment decoder** was initially incorrect because the vertical bar wasn’t treated as a don’t care value.

---

## References
- Course Textbook
- K-Maps - (https://www.youtube.com/watch?v=H4FkpBAK2Wk)
- 5-segment and 7-segment display tutorial - (https://www.youtube.com/watch?v=H4FkpBAK2Wk&t=36s)
- Logisim tutorial - (https://www.youtube.com/watch?v=Dp32ur04XcQ&list=PLFnx8Vsp0KYkhig6WCHnU-kt-1bugtl7e)

---
