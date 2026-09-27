# StudyPulse

**StudyPulse** is an offline-first class routine and study schedule PWA designed for students.

Upload a routine PDF/image, detect the table locally, review the extracted classes, confirm them, and receive automatic class reminders.

## 🚀 App

[Open StudyPulse](https://drive.google.com/file/d/1yf26KYQx5cChv2FHpw9Mrb0YNqStQBED/view?usp=sharing)

---

## ✨ Features

- 📄 Import routine from PDF or image
- 🔍 Table-first routine detection
- 🧠 Local OCR using Tesseract.js
- 📑 Local PDF processing using PDF.js
- ✏️ Review and edit detected classes
- 📅 Daily and weekly routine
- ⏰ Automatic class reminders
- 🔔 10-minute, 5-minute and start-time notifications
- 🌙 Light, Dark and System themes
- 📱 Android, iOS and Desktop support
- 📴 Offline-first PWA
- 🔒 Routine data stays on your device
- 💾 Local storage using IndexedDB/localStorage

---

# 🎯 Most Accurate Routine Import — JSON

For the **most accurate result**, StudyPulse also supports structured JSON import.

If you use a PDF or image, the app has to perform OCR and interpret the table. OCR can sometimes misread characters or table cells.

If you already have the routine converted into the required JSON format, StudyPulse can import the structured data directly.

### Why use JSON?

With valid JSON:

- No OCR is required.
- No table detection is required.
- No column guessing is required.
- Course code goes directly to Course Code.
- Course name goes directly to Course Name.
- Section goes directly to Section.
- Day goes directly to Day.
- Room goes directly to Room.
- Start time goes directly to Start Time.
- End time goes directly to End Time.

**If the JSON data itself is correct and follows the required format, StudyPulse will map the data directly without changing or guessing the values.**

---

# 📋 Required JSON Format

Use this exact structure:

```json
{
  "routine": [
    {
      "courseCode": "",
      "courseName": "",
      "section": "",
      "classes": [
        {
          "day": "",
          "room": "",
          "startTime": "",
          "endTime": ""
        }
      ]
    }
  ]
}
