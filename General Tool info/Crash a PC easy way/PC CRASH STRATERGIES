1. Batch File Loop (Windows) 
This creates a script that endlessly opens Command Prompt windows, consuming all available RAM and freezing the system. 
Open Notepad.
Type or paste the following:
batch
@echo off
:crash
start
goto crash
Click File -> Save As.
Name it crash.bat and change "Save as type" to All Files.
Double-clicking this file will immediately start the crash loop.
To stop it: You will likely have to force a shut down by holding the power button. 
2. The "Fork Bomb" (Linux/Unix/Windows PowerShell) 
A fork bomb is a form of denial-of-service attack where a process continually replicates itself to deplete system resources. 
YouTube
YouTube
Linux/Unix bash: :(){ :|:& };:
Windows PowerShell: while($true){start-process cmd.exe}
3. Keyboard Shortcut (Windows)
Windows has a built-in feature to force a Blue Screen of Death (BSOD) for debugging, which must be enabled in the registry.
Open Registry Editor (regedit).
Navigate to HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\kbdhid\Parameters (or i8042prt for PS/2 keyboards).
Create a new DWORD value named CrashOnCtrlScroll.
Set its value to 1.
Restart your computer.
To crash: Hold down the rightmost CTRL key and press Scroll Lock twice. 
Microsoft Learn
Microsoft Learn
 +2
4. Direct Kernel Crash (Windows)
You can directly command the kernel to shut down via command prompt, which is sometimes faster than a loop.
Open Command Prompt as Administrator.
Type: sc create crashsvc binpath="c:\windows\system32\ntoskrnl.exe" type=kernel start=demand
Type: sc start crashsvc
This will force an immediate kernel panic. 
5. Task Manager "End Task" (System Component) 
Killing essential Windows processes can freeze the operating system.
Press Ctrl + Shift + Esc to open Task Manager.
Go to the Details tab.
Find wininit.exe or csrss.exe.
Right-click and select End Task.
Note: Ending explorer.exe will just break the user interface (taskbar/desktop), but ending csrss.exe or wininit.exe will crash the whole system. 
