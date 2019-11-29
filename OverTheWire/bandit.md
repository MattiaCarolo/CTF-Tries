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

For now things are simple. Just launch an ssh in your preferred terminal at the desired port which in this case is 2220

``` bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

After that you will be asked for the password (if I remember correctly it's the same as the username).
Now you should be logged. Running a simple ``` ls ``` command will reveal a file called ```readme``` and if it it's opened ( I used ```cat <filename>``` ) it shows the searched password

``` txt
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

### level2

Now you can access __bandit1__ :tada: 

So as before the start is simple. access with the new account __bandit1__ doing
``` bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
and then just ls for the dahed file ( the ```-``` one) and just ``` cat - ``` .

It doesn't work? well if you look at the helpful materials [here](https://overthewire.org/wargames/bandit/bandit2.html) they hint that that particular filename can create some problems. 
So what do we do here?

The command ```cat``` normally sees the string ```-``` as a synonym for ```stdin``` (standard input) so if you try

``` bash
cat -
```

it will print out every line you type.

So we need to find a way to tell cat that our filename ```-``` refers to a file and not to ```stdin```. How do we do it? We need to alter the string so when cat start it reads a string that still refers to our file but won't be a synonym of ```stdin```. A way to do it is to change the argument from ``` -``` to ```./-``` in this way we give a path to the file we desire getting around the _"synonym problem"_

<!-- markdownlint-enable MD033 -->