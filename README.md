# NETWORKWALKS-WK3-PASSWORD-CRACKING
# Week 3 Project: Password Cracking with John the Ripper and Networkwalks Tools

This lab covers recovering the passwords of protected PDF files. I used two tools: the Networkwalks Hash Calculator and Password Cracker in the browser, and John the Ripper with its Johnny GUI on Windows.

## Status

| Part | Status | Evidence |
|---|---|---|
| PDF1 password recovered with the Networkwalks Password Cracker (`password1`) | Done | `screenshots/03-networkwalks-password1-found.png` |
| PDF1 flag captured | Done | `screenshots/04-pdf1-flag.jpg` |
| Johnny installed and John the Ripper executable set | Done | `screenshots/01-johnny-no-executable.png`, `screenshots/02-johnny-executable-detected.png` |
| PDF2 flag captured | Done | `screenshots/05-pdf2-flag.jpg` |
| PDF3 flag captured | Done | `screenshots/06-pdf3-flag.jpg` |



## Method 1: Networkwalks Hash Calculator and Password Cracker

1. Uploaded the locked PDF to the Hash Calculator. The tool generated a `$pdf$` hash in the browser.
2. Pasted the hash into the Password Cracker and started the attack against the built-in list of 100 passwords.
3. The tool found a match: `password1`.
4. Entered `password1` to open the PDF.

## Method 2: John the Ripper and Johnny (Windows)

1. Installed Johnny and opened its Settings. The John the Ripper executable field starts empty.
2. Pointed the field to `john.exe` in the John the Ripper `run` folder. Johnny detected John the Ripper 1.9.0-jumbo-1.
3. Extracted PDF hashes with the PDF hash extractor and saved them as text files beginning with `$pdf$`. The hash files are not included in this repo.

## Flags

- PDF1: `nw{cybersecurity_flag_captured_2608}`
- PDF2: `nw{networkwalks_persistence_jtr_270521}`
- PDF3: `nw{networkwalks_flag_260821_1}`

## What I learned

- A PDF stores a hash of its password, not the password itself. Cracking tools test candidate passwords against that hash.
- A dictionary attack finds weak passwords quickly. `password1` is on most lists of common passwords.
- Tools can produce different hash strings for the same file, so the hash has to be copied in full and checked against the tool that will crack it.

## Tools

- Networkwalks Hash Calculator and Password Cracker
- John the Ripper 1.9.0 Jumbo
- Johnny 2.2

## Demo video

[https://drive.google.com/file/d/1pXnD5dEgymGbyHZ0etcIdwkoOFZTyzyP/view?usp=sharing]



Completed as part of a cybersecurity course lab, on files provided for that exercise. The techniques are for learning and for testing files you own or have permission to test.
