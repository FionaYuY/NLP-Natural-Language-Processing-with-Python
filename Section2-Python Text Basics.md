# Introduction to Python Text Basics
- Open files (.txt, .pdf)
- Regular expressions

# Working with Text FIles with Python - Part One
- Basic print formatting (f-string literal)
- Files: 00-Python-Text-Basics/00-Working-with-Text-Files.ipynb
- Pass !r to get the string representation
  + ```print(f'His name is {name!r}')``` --> The result: His name is 'Fred'
- Minimum Widths, alignment, and padding 

<img width="918" alt="截圖 2024-09-22 晚上8 58 03" src="https://github.com/user-attachments/assets/3eccc4a9-f22d-417a-b051-9f66d25df287">

- Date formating

<img width="918" alt="截圖 2024-09-22 晚上9 00 07" src="https://github.com/user-attachments/assets/4b1a5c3d-fbb6-4e9f-b880-79751d5e3519">
  
  + Checkout strftime.org

# Working with Text Files with Python - Part Two
## Read files
- A magic command to write files.
  
<img width="923" alt="截圖 2024-09-22 晚上9 11 31" src="https://github.com/user-attachments/assets/c4d7161c-4dc4-4368-af3c-01955955e849">

- To checkout where your current notebook is located: ```pwd```

<img width="938" alt="截圖 2024-09-22 晚上9 16 28" src="https://github.com/user-attachments/assets/bfd89d0f-5602-48a7-b316-57d56e9e2dbc">

- If you want to open files that are located in different location, just pass in the entire file path.
- Read files
  + Notice: you can't call ```read()``` multiple times on a file.
  + Why? You have a cursor at the very beginning of a text file, and after you call ```.read()``` , that cursor goes throughout the entire text file and then returns the entire file as a string, and the cursor is sitting at the end of the file. Therefore, when you call ```read()``` again, it's going to read from the cursor all the way to the end of the file, which will return an empty string.
  + Solution: ```.seek(0)``` , you can change the cursor to index position zero (the beginning of the file).

<img width="939" alt="截圖 2024-09-22 晚上9 20 04" src="https://github.com/user-attachments/assets/4a120b7a-d85f-492d-aab2-54a6e258b073">

  + ```.read()``` is really useful for smaller files where you just wanna grab everythin and then save it as a string.
- Always close a file once you're done working with it. ```.close()```
  + Why? The reason you wanna make sure to do that is just in case you try opening that text file for another program, if you still have it open in Python, it may cause issues with your operating system. If you've ever tried to pull out a USB drive, and it said, "Hey, some files are still under use," that's the sort of thing that happens if you don't close a file. It'll basically say, "Hey Python is using this text file, I can't open it right now." So always make sure to close your files.
- ```readlines()``` : read in each line as a separte item in a list.

<img width="934" alt="截圖 2024-09-22 晚上9 31 45" src="https://github.com/user-attachments/assets/341d1252-96ba-4c4c-8aac-1f01522e22c7">

## Write files
- mode
  + 'r': reading
  + 'w': writing
  + 'x': create a new file and open it for writing
  + 'a': open for writing, appending to the end of the file if it exists.
  + 'b': binary mode
  + 't': text mode
  + '+': open a disk file for updating (reading and writing)
  + 'U': universal newline mode (deprecated)

<img width="791" alt="截圖 2024-09-22 晚上9 50 17" src="https://github.com/user-attachments/assets/589e7062-fa45-4625-bdc9-c822039f785f">


<img width="932" alt="截圖 2024-09-22 晚上9 44 05" src="https://github.com/user-attachments/assets/f5d3ec6e-23f8-4e98-923b-88683e262cfb">

## Appending files
<img width="922" alt="截圖 2024-09-22 晚上9 45 29" src="https://github.com/user-attachments/assets/2c879ce9-3ded-494f-965f-1b34e3a6a3d4">

## Aliases and context manger
- By using ```with open()``` , once this block of code is done running, it will automatically close the file.
<img width="925" alt="截圖 2024-09-22 晚上9 54 46" src="https://github.com/user-attachments/assets/75d7e2f8-ca9e-438a-87ea-46b4c6579a85">



