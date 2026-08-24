# PROG6112_Practical-Assignment-1_Junior-Kemorwe_10520371_04
PracticalAssignment
ails
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
