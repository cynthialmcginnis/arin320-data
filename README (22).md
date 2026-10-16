# Medical Appointment No-Shows: Data and Notebook

A real dataset of 110,527 medical appointments, with a notebook that shows how to check, clean, explore, split, and test it. No coding experience is needed.

## Open the notebook

[Open in Google Colab](https://colab.research.google.com/github/cynthialmcginnis/arin320-data/blob/main/Exploring_Real_Data_NoShows.ipynb)

You need a free Google account. Nothing to install. To keep your own copy, select **File**, then **Save a copy in Drive**.

## Files

| File | What it is |
|---|---|
| `noshow_appointments.csv` | The dataset: a CSV (comma-separated values) file of about 11 megabytes |
| `Exploring_Real_Data_NoShows.ipynb` | The notebook. It loads the data from this repository automatically. |

To open the data without the notebook, download `noshow_appointments.csv` and open it in Excel or Google Sheets.

## About the data

Public health clinics in Vitória, Brazil, recorded every appointment from April 29 to June 8, 2016.

- **Rows:** 110,527. Each row is one appointment, not one patient.
- **Patients:** about 62,300. Many patients have more than one appointment.
- **Columns:** 14
- **Blank cells:** none. Some missing information is hidden in other ways. The notebook shows where.

### Columns

| Column | Meaning |
|---|---|
| `PatientId` | Patient identifier (ID) |
| `AppointmentID` | Appointment identifier |
| `Gender` | F or M |
| `ScheduledDay` | Date and time the appointment was booked |
| `AppointmentDay` | Date of the appointment. No time of day was recorded. |
| `Age` | Patient age in years |
| `Neighbourhood` | Neighborhood of the clinic |
| `Scholarship` | 1 if the patient is enrolled in Bolsa Família, a Brazilian welfare program for low-income families |
| `Hipertension` | 1 if the patient has hypertension (high blood pressure). Spelled as in the original file. |
| `Diabetes` | 1 if the patient has diabetes |
| `Alcoholism` | 1 if the patient has alcoholism |
| `Handcap` | Values 0 to 4, most likely a count of disabilities. Spelled as in the original file. |
| `SMS_received` | 1 if the patient got at least one SMS (Short Message Service) text reminder |
| `No-show` | **Read carefully:** `No` means the patient **showed up**. `Yes` means the patient **missed** the appointment. |

### Known problems in the data

The file is shared exactly as published, problems included, because finding them is part of the lesson.

- One age of -1, and seven ages over 100
- Five appointments dated before they were booked
- Five patient IDs with decimal parts
- A yes/no column (`Handcap`) that holds five different values
- 1,334 repeat bookings with different appointment IDs, 29 of them with conflicting labels
- Two misspelled column names, and a label that reads backwards

## What the notebook covers

1. **Check and clean:** find every problem first, then fix it and write down each decision.
2. **Explore:** who is in the data, what goes with a missed appointment, and a pattern that fools you.
3. **Split, train, and test:** split the data by patient, train a simple model, and see how a score can mislead.

## Source and license

**The dataset:** `noshow_appointments.csv` is the *Medical Appointment No Shows* dataset by Joni Hoppen and Aquarela Advanced Analytics, originally published on Kaggle (2016). It is shared here unchanged under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 License](https://creativecommons.org/licenses/by-nc-sa/4.0/) (CC BY-NC-SA 4.0). You may use it for noncommercial purposes with credit to the original authors, and anything you build from it must use the same license.

**The notebook:** by Cynthia McGinnis, under the MIT License in this repository. The MIT License covers the notebook only, not the dataset.
