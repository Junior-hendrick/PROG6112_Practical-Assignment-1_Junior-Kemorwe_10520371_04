# PROG6112_Practical-Assignment-1_Junior-Kemorwe_10520371_04
PracticalAssignment
Name : Junior Kemorwe
Group : 04
Student no. : ST10520371
Lecturer : Tshembhani Shibiti
# Medicare Hospital Patient Admission System

## 1. Project Description

The Medicare Hospital Patient Admission System is a console-based Java
application developed to replace a paper-based patient admission process.

The system allows hospital administrative staff to:

- Register patients
- Search for patients
- Update patient information
- Delete patients
- Display all patients
- Allocate beds
- Release beds
- Display the ward layout
- Display available beds
- Display occupied beds
- Generate ward reports
- Sort patients by surname
- Sort patients by patient ID

The application stores information in memory while the program is running.

---

## 2. System Assumptions

The following assumptions were made:

1. The hospital contains one ward.
2. The ward contains exactly 20 beds.
3. The beds are arranged in a 4 x 5 layout.
4. Beds are numbered B01 to B20.
5. Only inpatients can receive a hospital bed.
6. Each inpatient can occupy only one bed.
7. A bed can only be assigned to one patient.
8. Outpatients do not require a hospital bed.
9. Emergency patients do not require a hospital bed.
10. All information is stored in memory.
11. Information is lost when the application is closed.
12. Patient IDs must be unique.

---

## 3. Technologies Used

- Java
- Object-Oriented Programming
- ArrayList
- Arrays
- Two-dimensional arrays
- Three-dimensional arrays
- Enum
- Inheritance
- Method overriding
- Exception handling
- JUnit 5

---

## 4. Classes

### Patient

The Patient class is the superclass.

It stores:

- Patient ID
- First name
- Last name
- Age
- Gender
- Medical condition
- Patient category

The fields are private to demonstrate information hiding.

### Inpatient

The Inpatient class extends Patient.

Additional fields include:

- Ward number
- Bed number

The class uses `super()` to initialise inherited fields.

It also overrides `displayDetails()`.

### PatientCategory

An enum representing:

- INPATIENT
- OUTPATIENT
- EMERGENCY

### PatientManager

This class manages registered patients.

It provides methods for:

- Registering patients
- Searching for patients
- Updating patients
- Deleting patients
- Sorting patients
- Displaying patients

An ArrayList is used to store patients.

### HospitalWard

This class manages the 20 hospital beds.

A 4 x 5 two-dimensional array is used to represent the ward.

It provides methods for:

- Allocating beds
- Releasing beds
- Displaying the ward
- Displaying available beds
- Displaying occupied beds
- Calculating occupancy

### HospitalSystem

This class controls the menu-driven console application.

### Main

The Main class starts the application.

---

## 5. Running the Application

1. Open the project in IntelliJ IDEA, NetBeans, Eclipse or another Java IDE.
2. Make sure all Java files are located in the correct source folder.
3. Run `Main.java`.
4. The hospital system menu will appear.
5. Select an option by entering the corresponding number.

---

## 6. Menu Options

1. Register new patient
2. Search for patient
3. Update patient
4. Delete patient
5. Display all patients
6. Allocate bed
7. Release bed
8. Display ward layout
9. Display available beds
10. Display occupied beds
11. Generate ward report
12. Sort patients by surname
13. Sort patients by patient ID
14. Demonstrate 3D array
0. Exit

---

## 7. Bed Allocation

Only patients whose category is INPATIENT can be allocated a bed.

A patient cannot:

- Occupy more than one bed
- Occupy an already occupied bed
- Be allocated a bed when all 20 beds are occupied

---

## 8. Ward Layout

The ward contains 20 beds:

B01 B02 B03 B04 B05

B06 B07 B08 B09 B10

B11 B12 B13 B14 B15

B16 B17 B18 B19 B20

---

## 9. Exception Handling

The system uses exception handling to prevent invalid program input from
causing the application to terminate.

For example, entering text when a number is required is handled using:

`NumberFormatException`

---

## 10. Unit Testing

JUnit 5 tests are provided for:

- Registering a patient
- Searching for a patient
- Updating patient details
- Deleting a patient
- Allocating a bed
- Releasing a bed
- Preventing duplicate patient IDs
- Preventing allocation of occupied beds
- Preventing allocation when all beds are occupied
- Sorting patients by surname
- Sorting patients by patient ID

---

## 11. Object-Oriented Programming Concepts

The application demonstrates:

### Encapsulation

Patient fields are private and accessed through getters and setters.

### Inheritance

`Inpatient` inherits from `Patient`.

### Polymorphism

An `Inpatient` object can be stored and treated as a `Patient`.

### Method Overriding

`Inpatient` overrides `displayDetails()`.

### Constructor Chaining

The `super()` keyword is used to call the superclass constructor.

---

## 12. Limitations

The system does not use a database.

Patient information is stored only while the application is running.

When the application closes, all information is lost.

The application is also designed for one ward containing exactly 20 beds.

---

## 13. Future Improvements

Future versions could include:

- Database storage
- User login
- Staff accounts
- Multiple hospital wards
- Patient discharge dates
- Admission dates
- Medical history
- Doctor information
- Printable reports
- Graphical user interface
- Backup and restore functionality
