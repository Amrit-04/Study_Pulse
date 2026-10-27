# StudyPulse 📚⏱️

### Native Android Academic Planning, Course Management & Study Effort Tracker

[![Android](https://img.shields.io/badge/Platform-Android%208.0+-3DDC84?style=flat&logo=android&logoColor=white)](https://developer.android.com)
[![Java](https://img.shields.io/badge/Language-Java-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://www.java.com/)
[![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=flat&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![Gradle](https://img.shields.io/badge/Build-Gradle-02303A?style=flat&logo=gradle&logoColor=white)](https://gradle.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

StudyPulse is a native Android application built to help high school and university students structure their academic schedules, track study commitments, and optimize time management.

---

## 📱 Features

- **📖 Course Organization:** Add and edit academic courses with course codes, credit hours, instructor details, and semester targets.
- **🧩 Learning Units Breakdown:** Divide each course syllabus into granular learning units to track progress topic-by-topic.
- **⏱️ Integrated Study Stopwatch:** Built-in timer (`NewLearningEffortStopwatch`) that allows students to time study sessions in real-time and log them automatically.
- **📈 Study Effort Tracking:** Record study sessions with notes, date stamps, and intensity ratings to review study habits over time.
- **👤 Personalized Profile:** Configure student study goals and target weekly hours (`NewEditProfile`).
- **💾 Offline-First Architecture:** Local persistence using an embedded SQLite database ensuring zero data loss and immediate access without network dependency.

---

## 🏗️ Architecture & Component Design

The app follows standard Android architectural best practices with clear separation between UI, business models, and data persistence:

- **UI Activities (`ui/`):**
  - `Welcome.java`: Application onboarding and entry.
  - `CourseList.java` & `CourseDetails.java`: Course browsing, searching, and management.
  - `LearningUnitDetails.java` & `NewEditLearningUnit.java`: Unit syllabus tracking.
  - `NewLearningEffortStopwatch.java`: Stopwatch timer and real-time session logging.
  - `NewEditLearningEffort.java`: Manual effort entry and session editing.
- **Data Access Layer (`db/`):**
  - SQLite database helper and data access objects (`CourseDataSource`, `LearningEffortDataSource`) providing robust CRUD transactions.
- **Adapters (`adapter/`):**
  - High-performance RecyclerView adapters (`CourseAdapter`, `LearningUnitAdapter`, `LearningEffortAdapter`).

---

## 🛠️ Building & Running

### Requirements
- [Android Studio](https://developer.android.com/studio) Ladybug or newer
- JDK 17+
- Android SDK 26 (Android 8.0) to 34 (Android 14)

### Steps
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Amrit-04/Study_Pulse.git
   ```
2. Open the project in **Android Studio**.
3. Allow Gradle to sync dependencies.
4. Select an emulator or physical device running Android 8.0 or higher.
5. Click **Run (`Shift + F10`)** to build and launch the app.

---

## 📄 License

This project is licensed under the MIT License.