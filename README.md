# vBsaltCrack
**vBulletin Salt Cracker Script**

An interactive Bash helper that automates pre‑processing and two‑stage cracking of vBulletin < 3.8.5 MD5-based passwords (unsalted and salted forms) using hashgen and hashcat, then writes the final recovered credentials to a user‑specified file.

Important legal note: this script is for lawful use only — run it only against systems, hashes, or datasets you own or for which you have explicit authorization. Unauthorized password cracking is illegal and unethical.

*Prerequisites*

- bash environment

- hashcat installed and available on PATH

- a local ./hashgen executable (from the linked project) in the current directory

- input files: a hash list and a wordlist (both supplied interactively)

- permission to run GPU/CPU cracking on the target data

*Interactive inputs*

When you run the script it prompts for:

- Path to the hash list (file containing vBulletin hashes to process)

- Path to the wordlist (plaintext wordlist used for attacks)

- Mask for salt cracking (optional; default ?a?a?a)

- Final output path for the cracked hashes (default 2611_cracked.txt) — the script will create the parent directory if needed
