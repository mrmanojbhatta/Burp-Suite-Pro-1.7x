# Burp Suite Pro v1.7.37 Legacy Release

This is my very old version of Burp Suite Pro v1.7.37. I bought it 6 years ago and now I want to share it with my fans. This release includes Java 8, Windows files, and Linux files.

Download Link: https://drive.google.com/drive/folders/1oXK3_e0H22x-lM9kwLUAhu5RHzTy4zA2

## Files Included

- OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz (Java 8 for Linux)
- jdk-8uXXX-windows-x64.exe (Java 8 for Windows)
- burpsuite_pro_v1.7.37.jar (Burp Suite Pro)
- burp-loader-keygen.jar (Loader and Keygen)

## Linux Setup Guide

1. Open Downloads folder
2. Open terminal in Downloads folder
3. Run: sudo su
4. Extract Java Archive file: tar -C /usr/lib/jvm -xzf OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz
5. Close Terminal
6. Extract Burp Archive file on Desktop
7. Open terminal in the same folder that is in Desktop
8. Run: sudo su
9. Run: java -jar burp-loader-keygen.jar
10. Open new terminal in the same folder that is in Desktop
11. Run: /usr/lib/jvm/jdk8u292-b10/bin/java -Xbootclasspath/p:burp-loader-keygen.jar -jar burpsuite_pro_v1.7.37.jar
12. Wait till burp loads and show the Enter License Key Screen
13. Now copy License from file burp-loader-keygen
14. Paste it in Burp Suite
15. Click on Next
16. Click on Manual Activation
17. Copy Activation Request from Burp Suite that is copy request
18. Paste it into burp-loader-keygen file
19. You will receive Activation Response
20. Copy Activation Response from burp-loader-keygen file and paste it in Burp Suite
21. Click on Next and then Finish
22. Now go to terminal
23. Run: nano ~/.zshrc
24. Scroll to the bottom of the file
25. Add: alias burpro="/usr/lib/jvm/jdk8u292-b10/bin/java -Xbootclasspath/p:/home/kali/Desktop/Burp\ Suite\ Pro/burp-loader-keygen.jar -jar /home/kali/Desktop/Burp\ Suite\ Pro/burpsuite_pro_v1.7.37.jar"
26. Note: Above path may be different for you. Please check and change it accordingly.
27. Save file: CTRL+O and Press Enter
28. Exit File: CTRL+X
29. Run: source ~/.zshrc
30. Close All terminals and Open new Terminal
31. Run: burpro

## Windows Setup Guide

1. Install Java 8 from the provided Windows file
2. Extract the Burp Suite archive to any folder
3. Open Command Prompt in that folder
4. Run: java -jar burp-loader-keygen.jar
5. Open a second Command Prompt in the same folder
6. Run: java -Xbootclasspath/p:burp-loader-keygen.jar -jar burpsuite_pro_v1.7.37.jar
7. Follow the same activation steps from step 12 to 21 in the Linux guide above

## Notes

- This version requires Java 8 only. It will not work with newer Java versions.
- If burpro alias does not work, run source ~/.zshrc again or reopen the terminal.
- Make sure the path in the alias matches your actual folder location.

##Thanks you
