# Python-File-Handeling-Practice

#### __1. Write a Python program to read an entire text file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.read()
print(text)
file.close()
```


#### __2. Write a Python program to read first n lines of a file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.readlines()
print(text[0:2])
file.close()
```


#### __3. Write a Python program to append text to a file and display the text__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","a")
file.write("\nPython is very reliable")
file.close()
```


#### __4. Write a Python program to read last n lines of a file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.readlines()
print(len(text))
print(text[4:2:-1])
file.close()
```


#### __5. Write a Python program to read a file line by line and store it into a list.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.read()
list=text.split("\n")
print(list)
file.close()
```


#### __6. Write a Python program to read a file line by line store it into a variable.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.readlines()
print(text[0::])
file.close()
```


#### __7. Write a Python program to read a file line by line store it into a list.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
text=file.read()
list=text.split("\n")
print(list)
file.close()
```


#### __8. Write a python program to find the longest words of a file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\input.txt","r")
text=file.read()
list=text.split(" ")
print(list)
largest_word=""
largest_length=0
for word in list:
    if len(largest_word)<len(word):
        largest_word=len(word)
        largest_word=word        
print("the longest word:",word)
file.close()
```


#### __9. Write a Python program to count the number of lines in a text file__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\line.txt","r")
text=file.read()
list=text.split("\n")
print(list)
print(len(list))
file.close()
```


#### __10. Write a Python program to count the frequency of words in a file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\freq.txt","r")
text=file.read()
words=text.split(" ")
for w in words:
    print (w,"'s freuency:",text.count(w))
file.close()
```


#### __11. Write a Python program to get the file size of a plain file.__

**Solution**
```python
import os

info= os.stat("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\empty.txt")
print("the size of file:", info.st_size,"bytes")
```


#### __12. Write a Python program to write a list to a file.__

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\write.txt","w")
t=file.write("2021")
t.split("")
#list=[]
#list.append(t)
print("list created")
file.close()
```


#### __13. Write a Python program to copy the contents of a file to another  file .__ 

**Solution**
```python
fst_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\freq.txt","r")
text=fst_file.read()
scnd_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\empty.txt","a")
t=text.split("\n")
for line in t: 
     scnd_file.write(line)
```


####  __14.program to combine each line from first file with the corresponding line in second file.__

**Solution**
```python
fst_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\1st.txt","r")
text1=fst_file.read()
scnd_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\2nd.txt","r")
text2=scnd_file.read()
t1=text1.split("\n")
#print(t1)
t2=text2.split("\n")
#print(t2)
print (t1[0]+" " + t2[0])
print (t1[1]+" "+t2[1])
```


#### __15. Write a Python program to read a random line from a file.__

**Solution**
```python
import random
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
lines=file.readlines()
print(random.choice(lines))
```


#### __16. Write a Python program to assess if a file is closed or not.__ 

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\prac.txt","r")
#file.close()
if file.closed:
    print ("file is closed")
else:
    print("file is open")
```
        
#### __17. Write a Python program to remove newline characters from a file.__

**Solution**
```python
list=open("python.txt").readlines()
for l in list:
    l.rstrip('\n')
print(list)
```


#### __18. Write a Python program that takes a text file as input and returns the number of words of a given text file.__  

**Solution**
```python
file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\freq.txt","r")
text=file.read()
s=text.replace(",", " ")
print(s)
words=s.split(" ")
print(words)
print("no.of words:",len(words))
```


#### __19. Write a Python program to extract characters from various text files and puts them into a list.__   

**Solution**
```python
fst_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\char1.txt","r")
text1=fst_file.read()
scnd_file=open("C:\\Users\\Ansh\\Desktop\\Ansh\\basic python\\char2.txt","r")
text2=scnd_file.read()
l=list()
s="!@#$%^&*()_"
for i in s:
    if i in text1:
        l.append(i)
for j in s:
    if j in text2:
        l.append(j)
print(l)
```


#### __20. Write a Python program to generate 26 text files named A.txt, B.txt, and so on up to Z.txt.__

**Solution**
```python
alpha="ABCDEFGHIJKLMNOPQRSTUVWXYZ"
for i in alpha:
    file=open("C:/Users/Ansh/Desktop/A-Z/"+i+".txt","w")
```


#### __21. Write a Python program to create a file where all letters of English alphabet are listed by specified number of letters on each line.__  

**Solution**
```python
msg="Python"
l=list(msg)
s="\n".join(l)
file=open("msg.txt","w")
file.write(s)
file.close()
```

##

### Contributing 💡

If you want to contribute to this project and make it better with new Question and their Solutions, your pull request is most welcomed. If you find any issue just put it in the repository issue section.
<br>
<br>
or
<br>
<h5> If you have any suggetions or advice please feel free to connect me:--

<a href="mailto:anshvnm@gmail.com" target="_blank"><img src="https://img.icons8.com/bubbles/50/000000/gmail.png" alt="Gmail"/></a>
<a href="https://github.com/anshdmishra" target="_blank"><img src="https://img.icons8.com/bubbles/50/000000/github.png" alt="GitHub"/></a>
</h5>

#

Show some ❤️ by starring ⭐️ some repositories !!

#


