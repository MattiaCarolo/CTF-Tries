<!-- markdownlint-disable MD033 -->
# Over the wire - Bandit

## All challenges

[Level 1](#level1)

[Level 2](#level2)

[Level 3](#level3)

[Level 4](#level4)

[Level 5](#level5)

[Level 6](#level6)

[Level 7](#level7)

[Level 8](#level8)

[Level 9](#level9)

[Level 10](#level10)

[Level 11](#level11)

[Level 12](#level12)

[Level 13](#level13)

[Level 14](#level14)

[Level 15](#level15)

[Level 16](#level16)

[Level 17](#level17)

[Level 18](#level18)

[Level 19](#level19)

[Level 20](#level20)

<br>

<br>

<br>

## Let's start the challenge

### level1

For now things are simple. Just launch an ssh at the desired port which in this case is 2220

``` bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

After that you will be asked for the password (id I remember correctly it's the same as the username).
Now you should be logged. Running a simple ``` ls ``` command will reveal a file called ```readme``` and if it it's opened ( I used ```cat <filename>``` ) will reveal  the searched password

``` txt
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

### level2

Now you can access __bandit1__ :tada:

<!-- markdownlint-enable MD033 -->