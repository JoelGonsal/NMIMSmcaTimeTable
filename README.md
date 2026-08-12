Link to Website : https://nmimsmca.netlify.app/
# 📚 Timetable JSON Repository

This repository contains the timetable data used by my **MCA Semester 3 Timetable App**.

The timetable is stored as a JSON file and is fetched by the website dynamically. This allows me to update the timetable by simply modifying the JSON file in this repository — without changing the website's source code.

## 🚀 How It Works

```text
Timetable JSON
      ↓
   GitHub
      ↓
Timetable Website
      ↓
Updated Schedule
```

The website reads the timetable data directly from the JSON file hosted in this repository.

Whenever the timetable changes:

1. Update the JSON file.
2. Commit and push the changes to GitHub.
3. The website fetches the updated timetable.
4. The new timetable is displayed automatically.

## 📁 Repository Structure

```text
timetable/
│
├── timetable.json
└── README.md
```

### `timetable.json`

Contains the complete timetable organized by day.

Each timetable entry contains:

| Field     | Description                            |
| --------- | -------------------------------------- |
| `start`   | Class start time                       |
| `end`     | Class end time                         |
| `time`    | Display time                           |
| `subject` | Subject, practical, break, or activity |

## 📝 JSON Format

```json
{
  "Monday": [
    {
      "start": "8:00 AM",
      "end": "6:00 PM",
      "time": "8:00 AM - 6:00 PM",
      "subject": "Capstone Project"
    }
  ],
  "Tuesday": [
    {
      "start": "8:00 AM",
      "end": "9:00 AM",
      "time": "8:00 AM - 9:00 AM",
      "subject": "Devops - CR 504"
    }
  ]
}
```

## ✏️ Updating the Timetable

To change a class, edit the corresponding entry in `timetable.json`.

For example:

```json
{
  "start": "10:00 AM",
  "end": "11:00 AM",
  "time": "10:00 AM - 11:00 AM",
  "subject": "Break"
}
```

can be changed to:

```json
{
  "start": "10:00 AM",
  "end": "11:00 AM",
  "time": "10:00 AM - 11:00 AM",
  "subject": "Machine Learning - CR 504"
}
```

After pushing the change to GitHub, the website can retrieve the updated JSON.

## ⚠️ Important

When editing the JSON:

* Keep the JSON syntax valid.
* Keep the day names consistent.
* Keep the required fields: `start`, `end`, `time`, and `subject`.
* Use valid time formats.
* Make sure strings are enclosed in double quotes.
* Don't add comments inside the JSON file.

You can validate the JSON before committing it using any JSON validator.

## 🌐 Purpose

The main purpose of this repository is to separate the **timetable data** from the **website code**.

Instead of modifying and redeploying the entire application whenever the timetable changes, the timetable can be maintained independently through this repository.

This makes timetable updates:

* ⚡ Faster
* 🛠️ Easier to maintain
* 🔄 Easy to update
* 📦 Independent from the frontend code
* 🌐 Accessible to the timetable website

## 🎓 Current Timetable

The current timetable contains schedules for:

* Monday
* Tuesday
* Wednesday
* Thursday
* Friday

It includes lectures, practical sessions, breaks, Capstone Project sessions, and separate B1/B2 schedules.

## 🔗 Website

The JSON repository acts as the data source for the timetable website.

> Update the JSON → Push to GitHub → Website gets the updated timetable.

---

Made for managing my MCA Semester 3 timetable 📚
