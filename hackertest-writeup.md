# Hacker Test Walkthrough

[Hacker Test](http://www.hackertest.net/) is an online "hacker simulator" where you can "test your hacking skills." This challenge set was recommended to our Security Reading Group (SRG)/hckd group by Sergey Bratus of Dartmouth College.

What follows is a walkthrough of the challenges, including spoilers and passwords. **If your goal is to learn**, do not simply copy the answers. The real value lies in exploring, problem-solving, and learning tools and techniques.

---

## 🔒 Disclaimer: Spoilers Ahead!

This document contains *passwords in plaintext* and detailed descriptions of how to solve each level. If you want to improve your skills and thinking, use this as a last resort.

---

## 🛠️ Tools & Tips

- **Browser Developer Tools**: Use your browser’s DevTools (Cmd+U, right-click → “Inspect”) to view source and inspect elements.
- **Image Editing**: Tools like Photoshop or [GIMP](https://www.gimp.org/) can help analyze image files.
- **Command-line utilities**: Use `base64`, `wget`, `xxd`, `strings`, or a hex editor to explore files.

---

## 🔍 Level-by-Level Solutions

### Level 1
**URL**: [http://www.hackertest.net/](http://www.hackertest.net/)  
**Hint**: Check the HTML source.  
**Password**: `null`

### Level 2
**URL**: [http://www.hackertest.net/null.htm](http://www.hackertest.net/null.htm)  
**Password**: `l3l` (lowercase "L", not the digit "1")

### Level 3
**URL**: [http://www.hackertest.net/l3l.htm](http://www.hackertest.net/l3l.htm)  
**Hint**: Look at `alinkColor`.  
**Password**: `#000000`

### Level 4–5
**URL**: [http://www.hackertest.net/abrae.htm](http://www.hackertest.net/abrae.htm)  
Click through to [http://www.hackertest.net/sdrawkcab.htm](http://www.hackertest.net/sdrawkcab.htm)  
**Password**: `SAvE-as hELpS a lOt`

### Level 6
**URL**: [http://www.hackertest.net/save_as.htm](http://www.hackertest.net/save_as.htm)  
Check `passwd.js`  
**Password**: `hackertestz`

### Level 7
**URL**: [http://www.hackertest.net/included.htm](http://www.hackertest.net/included.htm)  
Check [included.gif](http://www.hackertest.net/images/included.gif)  
**Username**: `phat`  
**Password**: `jerkybar3`

### Level 8
**URL**: [http://www.hackertest.net/pwd2.php](http://www.hackertest.net/pwd2.php)  
Check [phat.gif](http://www.hackertest.net/images/phat.gif) → then [phat.psd](http://www.hackertest.net/images/phat.psd)  
**Credentials**: `zadmin / stebbins`

### Level 9
**URL**: [http://www.hackertest.net/phat.php](http://www.hackertest.net/phat.php)  
Decode base64: `Z2F6ZWJydWg=` → `gazebruh`  
**Next**: [http://www.hackertest.net/gazebruh.php](http://www.hackertest.net/gazebruh.php)

### Level 10
**Password**: Combine italicized letters → `shackithalf`

### Level 11
**URL**: [http://www.hackertest.net/rofl.php](http://www.hackertest.net/rofl.php)  
**Hint**: Source code says go to `clipart.php`

### Level 12
**URL**: [http://www.hackertest.net/clipart.php](http://www.hackertest.net/clipart.php)  
**Hint**: Look at the image → `puta.php`

### Level 13
**URL**: [http://www.hackertest.net/puta.php](http://www.hackertest.net/puta.php)  
Zoom in on "l" → `4.xml`

### Level 14
**URL**: [http://www.hackertest.net/4.xml](http://www.hackertest.net/4.xml)  
Follow the link in the XML.

### Level 15
**URL**: [http://www.hackertest.net/4xml.php](http://www.hackertest.net/4xml.php)  
GIF reveals: `totally.php`

### Level 16
**URL**: [http://www.hackertest.net/totally.php](http://www.hackertest.net/totally.php)  
Use a hex editor to read image → Find "unavailable" → [http://www.hackertest.net/unavailable/](http://www.hackertest.net/unavailable/)

### Level 17
**URL**: [http://www.hackertest.net/unavailable/](http://www.hackertest.net/unavailable/)  
Page source reveals image → Check `bg.jpg` → hex reveals: `Ducky.php`  
**Next**: [http://www.hackertest.net/unavailable/Ducky.php](http://www.hackertest.net/unavailable/Ducky.php)

### Level 18
**URL**: [http://www.hackertest.net/level18.shtml](http://www.hackertest.net/level18.shtml)  
**Password**: `password`

### Level 19
**URL**: [http://www.hackertest.net/level19.shtml](http://www.hackertest.net/level19.shtml)  
Download GIF → Extract word → Use as filename

### Level 20
**URL**: [http://www.hackertest.net/gazebruh2.htm](http://www.hackertest.net/gazebruh2.htm)  
Base64 decode multiple times:

```bash
$ echo "VldwSk5Gb3lVa2hQUjJSclRUSlJlbFJITlU5TlIwNTBWbTE0YTFJelVqSlpNakF4WWtkT2NFNVlWbUZYUmtZeVYycEtTbG95U25SUFZFNU5Xbm93T1QwOT09" | base64 -D


---

⚠️ **Disclaimer:**  These solutions are based on vulnerable lab environments designed for legal security training.
