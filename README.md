![Image](https://github.com/user-attachments/assets/ba0472be-ab89-4f02-8096-2c24ef2005ea)



Thank you for sharing the ER model. Based on the diagram, here is the relational model derived from it:


Relational Schema
1. Hotel Table
Columns: Hotel_Id (PK), Hotel_name
Primary Key: Hotel_Id


2. Type Table
Columns: Type_Id (PK), Type_Name
Primary Key: Type_Id


3. Room Table
Columns: Room_Id (PK), Floor, Hotel_Id (FK), Type_Id (FK)
Primary Key: Room_Id


Foreign Keys:
Hotel_Id (references Hotel table)
Type_Id (references Type table)


4. Category Table
Columns: Category_Id (PK), Category_Name, Price, Beds_numbers
Primary Key: Category_Id


5. Employee Table
Columns: Employee_Id (PK), Employee_Name, Employee_Speciality, Hotel_Id (FK)
Primary Key: Employee_Id
Foreign Key:
Hotel_Id (references Hotel table)


6. Relationships:
Hotel (Hotel_Id) ↔ Room (Hotel_Id as FK) [1:N]
Room (Type_Id) ↔ Type (Type_Id as FK) [1:1]
Room (Category_Id) ↔ Category (Category_Id as FK) [1:N]
Hotel (Hotel_Id) ↔ Employee (Hotel_Id as FK) [1:N]
Employee (Employee_Id) ↔ Leads Relationship (Hotel leads the employee) [1:1]


![Image](https://github.com/user-attachments/assets/73d2e639-ce91-4241-aae0-8803af48d294)

