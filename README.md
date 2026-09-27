# StudyPulse

A privacy-first, offline-first class routine Progressive Web App (PWA) for students.

Upload your class routine as a PDF or image, detect the routine table locally, review the detected classes, confirm the routine, and get automatic class reminders.

## 🚀 Live App

👉 **Use Class Routine:**  
[https://YOUR-APP-LINK-HERE](https://drive.google.com/file/d/1yf26KYQx5cChv2FHpw9Mrb0YNqStQBED/view?usp=sharing)

> Replace the link above with your deployed app URL.

---

## ✨ Features

### 📄 Routine Import

Upload your routine as:

- PDF
- JPG
- JPEG
- PNG
- Other supported image formats

The app focuses on the actual routine table and attempts to detect:

- Course Code
- Course Name
- Section
- Day
- Room
- Start Time
- End Time

It also supports routines containing merged cells and multiple class sessions.

### 🔍 Table-First Detection

The parser is designed to analyze the routine table instead of blindly reading the entire document.

It attempts to:

1. Detect the routine table.
2. Detect rows and columns.
3. Identify column headers.
4. Read individual cells.
5. Handle merged cells.
6. Build individual class sessions.
7. Validate the extracted information.
8. Show possible errors for manual correction.

### 👀 Review Before Saving

Detected classes are shown in a review screen before they are saved.

You can:

- View the original PDF/image
- Zoom and pan the document
- Navigate between PDF pages
- Review every detected class
- Edit individual fields
- Check warnings
- Correct incorrect values

The routine is saved only after pressing:

**Confirm Routine**

### ⏰ Automatic Class Reminders

Set reminders for:

- 10 minutes before class
- 5 minutes before class
- At class start

Each reminder can be enabled or disabled independently.

### 🏠 Home Dashboard

The Home screen shows:

- Current class
- Next class
- Course
- Section
- Room
- Class time
- Live countdown

### 📅 Routine Views

View your routine as:

- Today's schedule
- Completed classes
- Current class
- Upcoming classes
- Full weekly schedule

Classes are sorted according to their actual time.

### ✏️ Manual Class Management

You can manually:

- Add a class
- Edit a class
- Delete a class

This is useful if a routine changes or if a particular class could not be detected correctly.

### 🔄 Replace Routine

You can completely replace your existing routine.

Replacing a routine:

1. Removes the old routine.
2. Clears old reminders.
3. Imports the new routine.
4. Creates new reminders.

### 🌙 Theme

Choose between:

- Light
- Dark
- System

---

# 🔒 Privacy

Class Routine is designed to work locally.

Your routine data stays on your device.

The application does **not** send your routine to:

- OpenAI
- Google Gemini
- Cloud OCR services
- External OCR APIs
- A remote database

OCR and PDF processing are performed locally in the browser.

Your routine is stored locally using browser storage such as IndexedDB/localStorage.

---

# 📴 Offline First

Class Routine is built as an offline-first Progressive Web App.

After the application has been loaded and cached once, supported features can continue working without an internet connection.

The app uses:

- Service Worker
- PWA caching
- IndexedDB/localStorage
- Local OCR
- Local PDF processing

Internet access may still be required for the initial application load or when a new version of the application needs to be downloaded.

---

# 📱 Install the App

Class Routine can be installed as a PWA.

## Android

1. Open the app in Chrome.
2. Open the browser menu.
3. Select **Install App** or **Add to Home screen**.
4. Confirm installation.

The app will appear on your Android home screen like a normal application.

## iPhone / iPad

1. Open the app in Safari.
2. Tap the **Share** button.
3. Select **Add to Home Screen**.
4. Tap **Add**.

## Desktop

On supported browsers:

1. Open the Class Routine website.
2. Look for the install icon in the browser address bar.
3. Select **Install**.

---

# 📖 User Manual

## 1. Open Class Routine

Open the application from the live app link.

You can use it directly from your browser or install it as a PWA.

---

## 2. Upload Your Routine

Go to the routine import option.

Upload your routine:

- PDF
- JPG
- JPEG
- PNG

For better detection, use a clear and high-resolution routine.

Avoid heavily blurred, rotated, or extremely low-resolution images.

---

## 3. Wait for Table Detection

The application processes the uploaded document locally.

For PDFs containing multiple pages, each page is analyzed.

The parser attempts to identify only the actual routine table and ignore unrelated content such as:

- Logos
- Page titles
- Headers
- Footers
- Unrelated text

---

## 4. Review Detected Classes

After processing, the application displays the detected classes.

Each class contains:

**Course**

**Section**

**Day**

**Room**

**Time**

Check every class carefully.

If something is incorrect, tap the field and edit it.

---

## 5. Check Warnings

The application may show:

**✓ Looks correct**

or

**⚠ Check Course**

**⚠ Check Room**

**⚠ Check Time**

Warnings mean that the application detected something that may require manual verification.

Do not ignore warnings if the detected information looks incorrect.

---

## 6. Confirm the Routine

After checking the detected classes, press:

**Confirm Routine**

Only after confirmation will the routine become the active routine.

Notifications will also be scheduled according to your settings.

---

# 🔔 Notification Setup

Go to:

**Settings → Notifications**

Enable the reminders you want.

Available reminder options:

- 10 minutes before class
- 5 minutes before class
- At class start

Your browser/device may ask for notification permission.

Select **Allow** if you want to receive notifications.

---

# ⚠️ PWA Notification Limitations

Notifications depend on the browser, operating system, PWA support, and device settings.

Background notifications are not guaranteed to behave exactly like notifications from a native Android/iOS application.

For reliable notifications:

- Allow notifications.
- Do not disable notifications for the app.
- Keep the PWA installed when possible.
- Avoid aggressive battery-saving restrictions.
- Make sure the browser/PWA is allowed to run required background services.

iOS and Android may apply their own background execution and notification restrictions.

The application therefore treats background notifications as **best-effort PWA notifications**, not as a guaranteed replacement for a native alarm application.

---

# 📅 Viewing Your Routine

## Home

The Home screen shows the most relevant class.

If a class is currently running, it displays:

**NOW**

Otherwise, it displays:

**NEXT CLASS**

Information includes:

- Course
- Section
- Room
- Time
- Countdown

---

## Today's Routine

Open the Routine section to see today's classes.

Classes are organized as:

- Completed
- Current
- Upcoming

---

## Weekly Routine

The weekly view displays the complete routine.

Classes are sorted by:

**Day → Actual Start Time**

---

# ✏️ Editing Classes Manually

Go to:

**Settings → Classes**

You can:

- Add a new class
- Edit an existing class
- Delete a class

A class contains:

```text
Course Code
Course Name
Section
Day
Room
Start Time
End Time
