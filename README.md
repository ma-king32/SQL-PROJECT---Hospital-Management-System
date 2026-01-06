# SQL-PROJECT---Hospital-Management-System

A new hospital requires assistance in creating and maintaining a database to manage its local
community’s patients. This hospital does not perform surgeries, but instead focuses on
diagnosing patients and prescribing them with medication when necessary. The hospital also has
staff that needs to be allocated to their respective functions within this new database, eg.
receptionist to the appointment system. This database also needs to be consistently updated, such
as when appointments are made and finished or when patient health records need to be changed.
To be included in our database are tables: staff, receptionist, nurse, doctor, appointment, visit,
patient, treatment history, treatment type, prescription, prescription history, pharmacy, payment,
and insurance provider.

RDM
Staff - (StaffID, Name, Role, Department)
Receptionist - (StaffID, OfficeNo, Contact_Num)
Nurse - (StaffID, FloorNo, DeskNo)
Doctor - (StaffID, Specialization, RoomNo)
Patient - (PatientID, Fname, Lname, DOB)
Appointment - (AppointmentID, AptDate, AptTime, Status, PatientID(FK), StaffID(FK))
Visit - (VisitID, VisDate, ViTime, Outcome,StaffID(FK),InsuranceID (FK),
AppointmentID(FK))
Insurance _Provider - (InsuranceID, ProviderName, Coverage)
Payment - (PaymentID, Amount, PaymentDate, InsuranceID(FK), VisitID(FK))
Treatment_History - (TreatmentHistoryID, StartDate, EndDate,VisitID (FK))
Treatment_Type - (TreatmentTypeID, Description, TreatmentHistoryID(FK))
Prescription - (PrescriptionID, Medication, Dosage, Freq, VisitID(FK))
Prescription_History - (PrescriptionHistoryID, StartDate, EndDate, PrescriptionID(FK),
PharmacyID(FK))
Pharmacy - (PharmacyID, Name, Address)
