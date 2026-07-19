# 🎨 ANSI Escape Codes: Colorful Texts in Your Terminal

**Hacking the Terminal: How to Print **Colorful** Text in Your Terminal**

Have you ever looked at a boring, black-and-white terminal and wondered, *"How do hacker movies show those neon green messages?"*

The secret lies in something built right into your computer: **ANSI Escape Codes**.

---

## 🧠 The Core Concept: What is an **ANSI Code**?

Think of your terminal as a "Dumb Typewriter". Whatever text you send to it, it just prints it on the screen. But what if you want to tell the terminal to change the ink color?

You need a way to whisper a "**secret command**" to the terminal. We do this using an **Escape Character** ( **\033[** ).

In Python, the escape character is written as `\033[`. 
When the terminal sees `\033[`, it immediately stops printing the next text and says: *"Oh wait, the programmer is giving me a secret instruction!"*

---

## 📐 **The Formula-**
```text
\033[ + Code Number + m
```

\033[ = **Start** the secret command.

**Code Number** = The actual color or style (e.g., **31 for Red**).

m = **Modify!** This tells the terminal that the command is over, now apply it.

**👉 So, the code for red text is simply: \033[31m**



**🚦The 2026 **CodeNumbers** Cheat Sheet-**

1.**Text Colors**-

🔴 Red: 31



🟢 Green: 32



🟡 Yellow: 33



🔵 Blue: 34



🟣 Magenta: 35


🌐 Cyan: 36

---

2.**Text Styles**-

Bold: 1

Underline: 4

---

3.The Most Important Code: **RESET**

🔄 **Reset: 0** ( **\033[0m** )


⚠️ The Golden Rule of Terminal Colors:

If you tell the trminal to turn Red, it will stay Red **FOREVER**, even after your program finishes running! You must ALWAYS add the **RESET code ( \033[0m )** **at the end** of your colored text to turn the colors OFF.

---
# **Boilerplate Code in **Python** Using Classes**-
```python

class Color:
    RED = '\033[31m'
    GREEN = '\033[32m'
    YELLOW = '\033[33m'
    CYAN = '\033[36m'
    
    BOLD = '\033[1m'
    RESET = '\033[0m'

# Use Python f-strings to inject the colors
print(f"{Color.GREEN}System booted successfully!{Color.RESET}")   # Turn ON Green ink , Type the word "Hello" , Turn OFF the ink (Reset to default).

print(f"{Color.RED}ERROR: File not found.{Color.RESET}")

# You can even mix them! (Bold + Cyan)
print(f"{Color.BOLD}{Color.CYAN}Welcome to the Matrix.{Color.RESET}")
```
## 💻**Boilerplate Code in C++ Using Strings-**

```cpp
#include <iostream>
#include <string>
using namespace std;

// Define colors in simple string variables
string RED = "\033[31m";
string GREEN = "\033[32m";
string CYAN = "\033[36m";
string BOLD = "\033[1m";
string RESET = "\033[0m";

int main() {

    cout << GREEN << "System booted successfully!" << RESET << "\n";
    
    cout << RED << "ERROR: File not found." << RESET << "\n";
    
    cout << BOLD << CYAN << "Welcome to the Matrix." << RESET << "\n";
    
    return 0;
}
```

---
# How to get ANY Custom Color (True RGB) ??
- Standard colors are great, but what if you want a very specific color, like Codeforces Orange or Spotify Green?
- he formula changes slightly to include the RGB numbers (from 0 to 255):
```text
\033[38;2; + R;G;B + m
```
**Example - ORANGE = '\033[38;2;255;165;0m'**

---
## 🚀 Conclusion

That’s it! You now know how to build beautiful, colorful **Command Line Interfaces (CLIs)**. 

By keeping your color codes organized inside a `Class` and using modern `f-strings`, your code naturally remains:
* ✨ **Clean**
* 👔 **Professional** 
* 📖 **Easy to read**

**Happy Coding! 💻**

