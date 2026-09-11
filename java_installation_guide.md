# Linux Manual Java Installation & Setup Note

### 1. The Archive Extraction Reality
When you extract a Java `.tar.gz` file (like `OpenJDK8U-jdk_x64_linux_hotspot_8u504b01.tar.gz`), extracting it directly or moving its raw contents into `/usr/lib/jvm/` means the core folders like `bin/`, `lib/`, and `jre/` will sit directly inside the `/usr/lib/jvm/` root directory.
* **Core Java Path:** `/usr/lib/jvm/bin/java`
* **Core Compiler Path:** `/usr/lib/jvm/bin/javac`

### 2. System Registration (Commands)
To make Ubuntu recognize this manual installation as the official system Java, run these registration commands:

```bash
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/bin/java 1
sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/bin/javac 1
```

### 3. Setting Default Version
If multiple Java versions exist, select the manual installation by running:
```bash
sudo update-alternatives --config java
```
*Choose the selection number pointing to `/usr/lib/jvm/bin/java`.*

### 4. Verification
```bash
java -version
```
*Expected output should show the correct version (e.g., `1.8.0_504`).*

---

# 🚀 Burp Suite Pro Alias Setup

Because you operate out of the `root` terminal user, the alias needs to be added to the **root profile** so it doesn't return a "command not found" error.

### Step-by-Step Configuration:
1. Open the root configuration profile:
   ```bash
   nano /root/.bashrc
   ```
2. Scroll to the very bottom of the file and paste this exact line:
   ```bash
   alias burpro="/usr/lib/jvm/bin/java -Xbootclasspath/p:'/home/user/Downloads/Burp Suite Pro/burp-loader-keygen.jar' -jar '/home/user/Downloads/Burp Suite Pro/burpsuite_pro_v1.7.37.jar'"
   ```
3. Save and Exit (`Ctrl + O`, then `Enter`, then `Ctrl + X`).
4. Reload the terminal environment:
   ```bash
   source /root/.bashrc
   ```

### Execution
From now on, no matter what folder your terminal is open to, you can launch your environment simply by typing:
```bash
burpro
```
