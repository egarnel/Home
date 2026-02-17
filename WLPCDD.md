# Lab 1: Getting Your Tools Ready

**Time needed:** 10–15 minutes  
**What you'll accomplish:** Clone the student materials repo, set up Visual Studio Code (VS Code), install GitHub Copilot, create a Python workspace, and run your first script to make sure everything is working.

---

### Step 0: Clone the Student Repository

**What you're doing:** Getting all the lab materials for the entire course in one place.

Before you start Lab 1, clone the student materials repository to your computer. This repo contains all the labs, resources, and starter files you'll need for Labs 1–6.

1. Open a terminal or command prompt on your computer
2. Navigate to where you want to save your projects (e.g., Documents or Desktop):
   ```bash
   cd ~/Documents
   # or on Windows: cd C:\Users\YourUsername\Documents
   ```
3. Clone the student repo:
   ```bash
   git clone https://github.com/robb404/wlpc-vibe-coding-student.git
   cd wlpc-vibe-coding-student
   ```
   > **Don't have git installed?** Download it from [git-scm.com](https://git-scm.com)

4. You should now see folders for `labs/` with subfolders: `01-setup/`, `02-snake-vague/`, `03-snake-structured/`, `04-snake-web/`, `05-converter/`, `06-mcp/`

> **What you should see:** A `wlpc-vibe-coding-student/` folder on your computer with all lab materials inside. You now have everything you need for the entire course!

---

### Step 1: Create your workshop folder structure in VS Code

**What you're doing:** Opening the cloned student repo in VS Code.

1. Open VS Code (you can find it in your Start menu or Applications folder)
2. Click **File** → **Open Folder**
3. Navigate to the `wlpc-vibe-coding-student` folder you cloned in Step 0 and click **Select Folder** (or **Open** on Mac)
4. VS Code will open the student materials folder. You should see a file explorer on the left with `labs/` and other files.

> **What you should see:** The VS Code Explorer on the left showing the `wlpc-vibe-coding-student` folder structure with `labs/` and lab subfolders (01-setup, 02-snake-vague, 03-snake-structured, 04-snake-web, 05-converter, 06-mcp).

Your folder structure should look like this:
```
wlpc-vibe-coding-student/
├── labs/
│   ├── 01-setup/
│   ├── 02-snake-vague/
│   ├── 03-snake-structured/
│   ├── 04-snake-web/
│   ├── 05-converter/
│   └── 06-mcp/
└── ...other files...
```

You're ready to start Lab 1 work. As you complete each lab, you'll create new folders inside each lab directory for your work files.

---

### Step 2: Install GitHub Copilot

**What you're doing:** Adding an AI coding assistant to VS Code that will help you write code faster.

1. Look at the **left sidebar** in VS Code and click the **square blocks icon** (this is the Extensions view)
2. In the search box at the top, type **"GitHub Copilot"**
3. Click the **Install** button next to "GitHub Copilot"
4. When prompted, click **Sign In** and follow the instructions to log in with your GitHub account
   > **Don't have a GitHub account yet?** Visit [github.com/signup](https://github.com/signup) to create one

> **What you should see:** After installing, you might see a checkmark or "Installed" label. You may also see a Copilot icon in the bottom-right corner of VS Code.

---

### Step 3: Open the terminal inside VS Code

**What you're doing:** Opening a command-line window where you'll type commands to check Python.

1. At the top of VS Code, click **View**, then **Terminal** (or press **Ctrl+`** on Windows/Linux, **Cmd+`** on Mac)
2. A panel will open at the bottom of the screen—this is your **terminal** (it looks like a command-line window)
3. Check the path shown in the terminal. It should end with `wlpc-vibe-coding-student` or your student repo folder name

> **What you should see:** A blinking cursor in the terminal at the bottom of your VS Code window.

---

### Step 4: Use Copilot to check and install Python

**What you're doing:** Using GitHub Copilot to validate Python is installed and working (or help you install it if needed). This is your first real taste of AI-assisted development!

> **What are Copilot suggestions?** After you type a comment, Copilot will show you gray suggested text next to your cursor. If nothing appears, wait 2-3 seconds or press **Ctrl+I** (Windows) / **Cmd+I** (Mac) to trigger it manually.

1. Create a new file in the `labs/01-setup` folder called `check_python.py`
2. Type a comment asking Copilot for help:
   ```python
   # Check if Python is installed and working
   ```
3. Press **Enter** twice and **wait**. Copilot will generate a complete program based on that comment.
4. Accept the suggestion (press **Tab** or click the checkmark)
5. Save the file (Ctrl+S or Cmd+S)
6. In the terminal, run:
   ```
   cd labs/01-setup
   python check_python.py
   ```
7. You should see your Python version printed.

> **What you should see:** Output showing your Python version (like `Python 3.10.5 ...`).

⚠️ **If you get "python not found":** This means Python was installed but wasn't added to your PATH (the list of folders your computer searches for commands). This is a common first-timer friction point—and it's intentional! It teaches you how to debug OS-level issues. **Fix:**
   1. Reinstall Python from [python.org](https://www.python.org/downloads/)
   2. **During installation, check the box "Add Python to PATH"** (it's easy to miss!)
   3. After install completes, close and reopen VS Code
   4. In VS Code terminal, type `python check_python.py` again
   5. If still "not found", try the full path: `C:\Users\%USERNAME%\AppData\Local\Programs\Python\Python312\python.exe check_python.py` (replace `%USERNAME%` with your Windows login name)

**Why this matters:** Learning to manage PATH variables is a real-world skill. Tools don't magically appear on your PATH—you have to configure them. After you solve it once, you'll understand why the pre-class email emphasized this step!

**Note:** This is exactly what you'll be doing in Labs 2-5: describing what you want, letting Copilot suggest code, and running it to verify it works!

---

### Step 5: Tell VS Code which Python to use

**What you're doing:** Making sure VS Code knows where to find Python on your computer.

1. Press **Ctrl+Shift+P** (Windows/Linux) or **Cmd+Shift+P** (Mac) to open the **Command Palette** (a search box at the top of the screen)
2. Type **"Python: Select Interpreter"** and click it when it appears
3. A list of Python installations will appear. Pick the one that shows the highest version number (like `Python 3.11.x`)

> **What you should see:** The bottom-right corner of VS Code should now show something like `Python 3.x.x`.

---

### Step 6: Let Copilot write from a one-line prompt

**What you're doing:** Describing what you want in a single sentence. This shows what Copilot can create with minimal guidance—and introduces the concept of vague vs. structured prompts.

> **Important:** Don't worry about understanding the code Copilot writes—just let it generate it for you. Focus on the pattern: how clear is your one-line prompt?

1. Create a new file in the `labs/01-setup` folder called `demo.py`
2. Write a single one-sentence prompt, just like Lab 2:
   ```python
   # Write me a simple hello world program
   ```
3. Press **Enter** twice and **wait**. Copilot will generate a complete program based on just that one sentence.
4. When you see the suggestion, accept it (press **Tab** or click the checkmark)
5. Save the file (Ctrl+S or Cmd+S)
6. In the terminal, run it:
   ```
   cd labs/01-setup
   python demo.py
   ```
7. It should run successfully and print output.

> **What you should see:** Copilot took a vague one-liner and produced working code. Simple prompts work when requirements are straightforward. What happens with more complex requests? That's something to think about as you tackle bigger challenges.

> **If Copilot doesn't suggest anything:** Press **Ctrl+I** (Windows/Linux) or **Cmd+I** (Mac) to trigger Copilot manually.

---

## Success! 🎉

If your `demo.py` ran successfully, **you are all set!** You now have:
- ✅ A working Python environment
- ✅ GitHub Copilot installed and generating code
- ✅ A lab folder where you'll do your work
- ✅ Experience using a one-line prompt (just like Lab 2)

---

## Troubleshooting

**Problem: "Python not found" error**
- **Root cause:** Python installed but not added to PATH during setup.
- **Fix (2-minute solution):** Reinstall Python from [python.org](https://www.python.org/downloads/) and **carefully check "Add Python to PATH"** during the install wizard. Then close and reopen VS Code.
- **Workaround (if you can't reinstall):** Use the full path: `C:\Users\%USERNAME%\AppData\Local\Programs\Python\Python312\python.exe check_python.py` (replace `%USERNAME%` with your login name)
- **Pro tip:** After fixing this, you'll understand why the pre-class email made such a big deal about PATH configuration!

**Problem: VS Code is using the wrong Python version**
- **Fix:** Repeat Step 5 (Select Interpreter) and make sure you pick the latest Python 3.x version.

**Problem: Copilot isn't responding**
- **Fix:** Click your profile icon in the bottom-left corner of VS Code and make sure you're signed in. Also check that the Copilot extension shows "Enabled" in the Extensions view.

**Problem: Terminal path doesn't end with the workshop folder**
- **Fix:** Use the `cd` command to navigate to the right folder, or close VS Code and reopen it by right-clicking the workshop folder and choosing "Open with Code".

---

## Exit Criteria

You've completed Lab 1 when:

- ✅ Python 3.10+ installed and verified
- ✅ VS Code open with Copilot installed
- ✅ `demo.py` runs successfully and prints "Hello, World!"
- ✅ You understand the basics of using Copilot with one-line prompts

You're ready for the next challenge!
