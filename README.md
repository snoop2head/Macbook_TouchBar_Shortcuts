# Macbook Pro Touchbar Shortcuts for Developers

## What you can do

1. **For Macbook Pros with touch bars, you can open folder with programs with one click.**

- **On touchbar, shortcut Buttons will look like following** 

![touchbar_example](./imgs/touchbar_example.png)

- **Runthrough Example: Open folder with VSCode**

![gif](./imgs/gif.gif)

2. **Right Click to open folder with certain programs: Iterm2, Typora, VSC etc...**

![img](https://k.kakaocdn.net/dn/purvw/btqCdhjUMVM/s9QOiJMSDyWVLyxcr1nCz1/img.png)



## How

1. Spotlight(CMD + Space) to find Automator.

![img](https://k.kakaocdn.net/dn/GLisZ/btqCbgsXSow/0oRZQSpeNhkhEzD31DIV30/img.png)

2. Choose Quick Action

![img](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FcX5b5R%2FbtqCbT5m6NR%2Ft0hIShG5VlKHvetDxd89Qk%2Fimg.png)

3. You'll get this screen after selecting quick action

![img](https://k.kakaocdn.net/dn/zt4wn/btqCcjJvg2W/WEuhRAkexKY8aISyRkxwJk/img.png)

4. On the left side of panel, search for "Run Shell Script"

![img](https://k.kakaocdn.net/dn/bu6Yp4/btqCckPasVP/Mg4QKiJVUpKMMEWEUPFdeK/img.png)

5. Then, on the right side of panel will look like this. Now We are ready to customize this quickaction one-by-one.

![img](https://k.kakaocdn.net/dn/bjcaIz/btqCbUwqLbz/7jNzUfLHAtg3U4LFK5Va60/img.png)

6. Workflow receives current "files or folders"

![img](https://k.kakaocdn.net/dn/dEGAo3/btqCdhYw2rM/n2Ho9IKmeQMM15NZbmHlhk/img.png)

7. Workflow receives current "files or folders" in "Finder"

![img](https://k.kakaocdn.net/dn/bHCOBi/btqCdgkZ6MN/obGi8eT41jQzlFS9DH127K/img.png)


(optional) Choose Icon which intuitively displays the action for you.

![img](https://k.kakaocdn.net/dn/cGE3ri/btqCcBC8XHu/vSM6IcYRX1Tng2UKulKo30/img.png)

8. Select shell as "/bin/bash" and write the script(AppleScript) as following:

![img](https://k.kakaocdn.net/dn/wq0bO/btqCae3tmPa/HEMkm2uRdUrroyg55N2i3k/img.png)

To Open VSCode with quickaction:

```
for f in "$@"; do
    open -a 'Visual Studio Code' "$f"
done
```

To Open iTerm with quickaction:

```
for f in "$@"; do
    open -a iTerm "$f"
done
```

To Open Typora with quickaction:

```
for f in "$@"; do
    open -a typora "$f"
done
```



9. Pass input "as arguments"

![img](https://k.kakaocdn.net/dn/uUJRT/btqCaeI92tg/oyyKmin5eNRTWQslAguc21/img.png)

10. After the process 1 ~ 9, it should look like the following:

![img](https://k.kakaocdn.net/dn/c4W8k1/btqCd1unbls/0sDn3kMbg4AykQpgjhwQN1/img.png)



11. CMD+S to save the quickaction and name the quick action.

12. Quickactions can be archived on Services folders. You can rename/delete/edit your quickactions here.

![img](https://k.kakaocdn.net/dn/NXK1J/btqB9XAN8WE/gnAINypE3kNibDUmd7t3KK/img.png)

## Version

- Mac OS Cattalina ver. 10.15.3
- Macbook Pro 16 inch model

## Reference

- [How to add a right click option in folder to open the folder with an application like VS Code](https://apple.stackexchange.com/questions/238948/osx-how-to-add-a-right-click-option-in-folder-to-open-the-folder-with-an-applic)
- [Automator Specifications](http://www.macosxautomation.com/automator/services/index.html)