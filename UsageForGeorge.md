# Usage for George 😄 📝

> This doc written for remembering often used command line 


### Step by Step to Run pict program

#### 1. move root directory to /pict

![cd to pict](https://user-images.githubusercontent.com/78633515/155453262-1416f253-b280-4087-a535-17eb2c3e1a8a.png)

#### 2. Create model file(e.g. env.txt) to generate test cases. and save it in pict directory.

```shell
# This is a comment and will be ignored by pict

Browser: Chrome, Firefox, Safari, Edge
OS: Window 7, Window 10, Window 11, MacOS BigSur, MacOS Monterey, Linux
Local: US, UK, KR, DE, CN
IF[OS] in {"MacOS BigSur", "MacOS Monterey"}
Then [Browser] = "Safari";
IF[Browser] = "Edge"
Then [OS] in{"Window 7", "Window 10"};
```

![Screen Shot 2022-02-24 at 12 37 40 PM](https://user-images.githubusercontent.com/78633515/155453443-8a0d0868-f25a-4743-898c-d85d6a39703e.png)
> env.txt file should located in pict directory.

#### 3. Run command in terminal

```shell
./pict env.txt
```
![Screen Shot 2022-02-24 at 12 40 07 PM](https://user-images.githubusercontent.com/78633515/155453639-eccf567c-f6e0-433b-8e9a-53257c163d33.png)
>You will get testcases like images
<br>

### Conditional command

1. Single - IF ... THEN 

```shell
# Program return only Edge - Window OS paired Test cases, not other OS like MacOS, Linux etc.
IF[Browser] = "Edge"
Then[OS] = "Window"; # Semicolon is required at the end of the conditional command line. 
```

2. Multiple - IF ...THEN
```shell
# If the OS type is MacOS BigSur or MacOS Monterery, Browser type is will be Safari.
# You can filtering multiple condition by using 'in .. {} curlybrace command  
IF[OS] in {"MacOS BigSur", "MacOS Monterey"}
Then [Browser] = "Safari";
```


