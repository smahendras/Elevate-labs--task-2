# 🏫 College Database Records

This project demonstrates basic SQL operations for managing student and guardian records in a college database using MySQL.

## 📋 Data Inserted

### `studentRecord` Table
Inserted 10 student records with the following fields:
- `enroll`: Enrollment number (Primary Key)
- `fname`, `lname`: Student's first and last name
- `address`: Residential address
- `DOB`: Date of birth
- `religion`: Religion
- `adhaarNo`: Aadhaar number

### `guardian` Table
Inserted 10 guardian records linked to students via `enroll`:
- `enroll`: Foreign key referencing `studentRecord`
- `fatherName`, `motherName`: Guardian names
- `fatherOccupation`: Occupation of the father
- `familyContact`: Contact number

## 🔧 Table Modification
- Altered `familyContact` column in `guardian` table from `INT` to `BIGINT` to support 10-digit mobile numbers and prevent out-of-range errors.

## 🗑️ Data Deletion

To delete the student record with `enroll = 1006`, the following steps were taken:

1. **Deleted the guardian record first**:
   ```sql
   DELETE FROM guardian WHERE enroll = 1006;

2. **Then deleted the record from student table**:
  ```sql
   DELETE FROM studentRecord WHERE enroll = 1006;

   

