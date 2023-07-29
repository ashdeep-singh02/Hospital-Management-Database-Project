# Hospital Management Database
## MYSQL

Database Management Final Project

For a given hospital, our Hospital Management Database will organize given patient and doctor information. Using this information, doctors can not only access their employment information, but also view their patients’ details- like their previous health conditions, surgeries, medications they are taking, future appointments, etc. The system can also serve as an appointment guide to schedule appointments for patients and doctors. Finally, the doctor can keep track of the diagnosis they make and the medications they prescribed after their appointments.

## Atributes:
• Each patients must have
- Health Insurance ID
- Gender
- Name
- Phone Number
- Address
- Patient Medication (if available)
- Patient Appointment Data
- Prescription
- TypeofService

• Each Doctor must have:
- Doctor Name
- Doctor ID
- Doctor Specialty

## Features:
• Allows physicians to view/update their patients’ medical history.
• Allows Hospital Staff and the patient to view/update his/her appointment dates/times.
• Allows patients and doctors to view (doctors can view/update) patient prescriptions and diagnoses made after appointment.
• Allows Hospital Staff to view patient symptoms and concerns.
• Patients and hospital staff can view doctors' schedules.
• View the payment plan/details of patient services.

## ER Diagram:
![Screen Shot 2023-05-08 at 11 28 23 PM](https://user-images.githubusercontent.com/71999538/236986574-c164a59c-c6bf-466c-9b61-2ebda1401542.png)

## Creating Tables in MySQL:
![Screen Shot 2023-05-08 at 11 29 54 PM](https://user-images.githubusercontent.com/71999538/236986669-15510db9-a516-4da9-a31f-2018de5d7346.png)
 ![Screen Shot 2023-05-08 at 11 30 19 PM](https://user-images.githubusercontent.com/71999538/236986750-ce7394be-8fb3-49bc-b3f9-d0c0cb0a64a3.png)
![Screen Shot 2023-05-08 at 11 30 14 PM](https://user-images.githubusercontent.com/71999538/236986752-261938a2-99cc-49f4-b8b9-9c8af3230dd0.png)
![Screen Shot 2023-05-08 at 11 31 45 PM](https://user-images.githubusercontent.com/71999538/236987018-3b7316a5-2600-4c50-82b2-da83b9ec6405.png)
![Screen Shot 2023-05-08 at 11 31 51 PM](https://user-images.githubusercontent.com/71999538/236987019-1b66d99d-7e6b-4bc1-bbb4-c48cba699859.png)
![Screen Shot 2023-05-08 at 11 31 56 PM](https://user-images.githubusercontent.com/71999538/236987020-d582a0e0-6ec5-47c2-9397-8814a196f64b.png)
![Screen Shot 2023-05-08 at 11 31 59 PM](https://user-images.githubusercontent.com/71999538/236987021-b0c0b8c9-b80d-4c52-9481-841fd00a1e1f.png)
![Screen Shot 2023-05-08 at 11 32 03 PM](https://user-images.githubusercontent.com/71999538/236987022-b5ec3f05-b116-44b6-a840-cee19d3056d4.png)
![Screen Shot 2023-05-08 at 11 32 07 PM](https://user-images.githubusercontent.com/71999538/236987023-a3ad0caf-0371-49cd-8a9f-1fb937ade414.png)
![Screen Shot 2023-05-08 at 11 32 11 PM](https://user-images.githubusercontent.com/71999538/236987024-0500cb4c-f961-4c60-9f2d-b201f85465c4.png)
![Screen Shot 2023-05-08 at 11 32 14 PM](https://user-images.githubusercontent.com/71999538/236987025-4d95a0f4-7cd2-44ef-af5d-7d3b4dee09ad.png)
![Screen Shot 2023-05-08 at 11 32 18 PM](https://user-images.githubusercontent.com/71999538/236987027-c37c2061-2a40-4bdd-9d5e-86d252bd9e2b.png)

## MySQL Query #1:
![Screen Shot 2023-05-08 at 11 33 32 PM](https://user-images.githubusercontent.com/71999538/236987182-ce399d8b-6009-422b-b6b0-216e1cc595b5.png)
![Screen Shot 2023-05-08 at 11 33 46 PM](https://user-images.githubusercontent.com/71999538/236987218-4a608139-64a8-4ac5-9d00-f392969b2787.png)

## MySQL Query #2:
![Screen Shot 2023-05-08 at 11 34 08 PM](https://user-images.githubusercontent.com/71999538/236987256-5f881e1f-5681-44dd-8b6e-9f6959b1a838.png)
![Screen Shot 2023-05-08 at 11 34 14 PM](https://user-images.githubusercontent.com/71999538/236987264-dfa37a54-61ea-4a87-a0a0-036bce4be10a.png)

## More Queries:
`select patient_name, medication_id, count(*) as np from (select pt.patient_name, p.medication_id from consult as c natural join perscription as p natural join patient as pt) as x group by 1,2; `

`select patient_name, patient_condition from pmc natural join patient;`

`select patient_name, sum(cost) from (cost natural join service natural join consult natural join patient) group by patient_name;`
