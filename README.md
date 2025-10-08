# 🕊️ Shorebird Configuration in Flutter

Easily enable **Over-The-Air (OTA)** updates for your Flutter apps using [Shorebird](https://shorebird.dev).  
Follow the steps below to configure Shorebird in your Flutter project.

---

## 🚀 Step 1: Sign in to Shorebird Console

Create or log in to your Shorebird account:  
👉 [https://console.shorebird.dev/](https://console.shorebird.dev/)

---

## ⚙️ Step 2: Install Shorebird CLI

### For macOS / Linux:
```bash
curl --proto '=https' --tlsv1.2 https://raw.githubusercontent.com/shorebirdtech/install/main/install.sh -sSf | bash
```
### For Windows (PowerShell):
```bash
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iwr -UseBasicParsing 'https://raw.githubusercontent.com/shorebirdtech/install/main/install.ps1' | iex
```
### 🧭 Step 3: Add Shorebird to Environment Path
Make sure the Shorebird CLI is accessible from your terminal by adding its path to your system environment variables.

### 🧪 Step 4: Verify Installation
Run the following commands to ensure everything is set up correctly:
```bash
shorebird doctor
```
If any issue found, follow below command to fix
```bash
shorebird doctor --fix
```
To see the shorebird version
```bash
shorebird --version
```
### 🔐 Step 5: Log in to Shorebird
Authenticate your CLI with your Shorebird account:
```bash
shorebird login
```
### 📂 Step 6: Initialize Shorebird in Your Flutter Project
Navigate to your Flutter project directory and initialize Shorebird:
```bash
cd your_flutter_project
```
```bash
shorebird init
```
### ✅ Configuration Completed!
After successful initialization:

A new file shorebird.yaml will be created in your project root.

Your app will be registered with Shorebird.

OTA patching support will be enabled.

You can now build and patch your Flutter app using:
```bash
# Create a release build
shorebird release android
```
```bash
# Push a Dart-only update (patch)
shorebird patch android
```
### 🧠 Notes
Only Dart code changes can be patched.

Native code or asset changes still require a full store update.

For more details, visit the official Shorebird documentation.

## Thank you. If you feel this helps you, then give me a star.
