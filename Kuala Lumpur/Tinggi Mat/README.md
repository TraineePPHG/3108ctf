# Tinggi Mat 🕵🏻‍♀️

## 🧾 Challenge Description
> **Points:** 100   
>  
> Kalau kat KL je mesti ingat KLCC. Alang-alang kita cerita pasal bangunan tinggi ni. Kenal tak Warisan Merdeka Tower?
>
> **Challenge Material:** WMT.rar
> 
> **Category:** Forensic 🕵🏻‍♀️  

## 🔍 Analysis
- **Initial Thoughts:**  
So, the first thing came into my mind is to unrar the file. Two files were obtained, flag2.rar and WarisanMerdekaTower.png.  

![image](https://github.com/user-attachments/assets/09f8c32d-f15f-44c1-82be-f753a384f27d)


## 🛠️ Solution
- Running the command *zsteg -a WarisanMerdekaTower.png* reveals the first part of the flag and provides the password for flag2.rar, which is MERDEKA118.

![image](https://github.com/user-attachments/assets/1cc82023-59c0-4b60-ba47-710890429a2e)

- Running the command *cat flag2.txt* gives nothing much but using the command *hexdump -C flag2.txt* gives us more information about the files. The command shows the file's contents in hexadecimal format, which can be useful for seeing hidden data or non-printable characters. I copied the command output and researched it using ChatGPT. It appears to be related to **Unicode zero-width spaces**.
  
![image](https://github.com/user-attachments/assets/4f00134e-4811-4067-a646-abb75a60e433)

- Open the flag2.txt, Ctrl+A and copy the whole content of the file. Using [Unicode Steganography with Zero-Width Characters Decoder](https://330k.github.io/misc_tools/unicode_steganography.html), the final part of the flag is revealed!

![image](https://github.com/user-attachments/assets/88ae79b1-89ab-46d5-abe6-016b7308097c)
3108{th3_t4ll3st_0n3_1n_M4l4ys14!}

## 🧰 Tools Used
- Linux CLI
- ChatGPT
- Unicode Steganography with Zero-Width Characters Decoder
