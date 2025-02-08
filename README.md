# DNA to Protein Translation Tool

The **DNA to Protein Translation Tool** is a simple web-based application that translates a given DNA sequence into its corresponding protein sequences across all six reading frames (three forward frames and three reverse frames). This tool is implemented in HTML, CSS, and JavaScript and can be run directly in any modern web browser.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Customization](#customization)
- [License](#license)

---

## Overview

This application allows users to input a DNA sequence, which is then cleaned (i.e., non-ATCG characters are removed) and converted into protein sequences based on the standard genetic code. It calculates the reverse complement of the input DNA sequence and performs translation in all three reading frames for both the forward and reverse strands.

---

## Features

- **DNA Sequence Input**: Users can enter or paste a DNA sequence.
- **Data Sanitization**: Filters out any characters that are not valid nucleotides (A, T, C, G).
- **Six-Frame Translation**: Translates the DNA sequence into protein sequences in three forward reading frames and three reverse reading frames.
- **Reverse Complement Calculation**: Computes the reverse complement of the provided DNA sequence.
- **User-Friendly Interface**: A simple and clean design for easy input and output display.
- **Responsive Layout**: Works well on both desktop and mobile browsers.

---

## How It Works

1. **Input Handling**:  
   - The user inputs a DNA sequence into a textarea.
   - When the "Translate" button is clicked, the input is processed:
     - Converted to uppercase.
     - Non-ATCG characters are removed.

2. **Translation**:  
   - Uses a JavaScript object representing the standard genetic code to map DNA codons (triplets) to amino acids.
   - For each reading frame (starting positions 0, 1, and 2), the sequence is read in triplets, and the corresponding amino acids are concatenated to form the protein sequence.
   - If a codon is not found in the genetic code, a question mark (`?`) is used as a placeholder.

3. **Reverse Complement**:  
   - Computes the reverse complement of the DNA sequence by:
     - Replacing each nucleotide with its complement (A ↔ T, C ↔ G).
     - Reversing the resulting string.
   - The reverse sequence is then translated in all three reading frames.

4. **Output**:  
   - The resulting protein sequences for all six reading frames are displayed on the page, grouped under headings indicating the frame number and direction (Forward/Reverse).

---

## Usage

1. **Open the Tool**:  
   Open the HTML file in any modern web browser.

2. **Input DNA Sequence**:  
   Enter or paste your DNA sequence into the provided textarea.

3. **Translate**:  
   Click the "Translate" button to generate protein sequences.

4. **View Results**:  
   The protein sequences corresponding to the three forward reading frames and the three reverse reading frames will be displayed below the button.

---

## Code Structure

- **HTML**:  
  Provides the structure of the web page including:
  - A textarea for input.
  - A button to trigger translation.
  - A div for displaying the output.

- **CSS**:  
  Styles the application with:
  - A clean and modern look.
  - Responsive design elements (container, typography, etc.).

- **JavaScript**:  
  Contains the logic for:
  - Cleaning and processing the input DNA sequence.
  - Translating the sequence into protein sequences using the genetic code.
  - Calculating the reverse complement of the DNA sequence.
  - Dynamically updating the page with the results for all six reading frames.

---

## License

This project is open-source and available for use and modification. You can modify and distribute this tool under the terms of the [MIT License](https://opensource.org/licenses/MIT).

---
