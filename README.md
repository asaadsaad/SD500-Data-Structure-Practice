# SD500-Data-Structure-Practice
Create a TypeScript workspace, and implement CRUD operations for following data structures. All functions return a boolean, except those who read the data. 
  
To gain deeper understanding to the course concepts, consider solving the questions with:
* regular function vs encapsulate the data as a private member in a class and provide public methods to read and manipulate the data.
* convert the functions to run asyncronously using Promise.
* perform the changes with mutation vs. in immutable way.

```typescript
type Item = { id: string, title: string; };

// add item (if id does not exist)
// update the title (if id exist)
// delete the item (if id exist)
// read title by id (if id exist)
const data1: Item[] = [];

// the item id is used as key, and the item title is the value
// add item (if id does not exist)
// update the item title (if id exist)
// delete item (if id exist)
// read title by id (if id exist)
type Data2 = { [id: string]: string; };
const data2: Data2 = {};

// the item id is used as key, and the item value is an object that contains the title
// add item (if id does not exist)
// update title (if id exist)
// delete item (if id exist)
// read title by id (if id exist)
type Data3 = { [id: string]: { title: string; }; };
const data3: Data3 = {};

// add student (if group id exist, and student_id does not exist)
// update student full name (if group id exist, and student_id exist)
// delete student (if group id exist, and student_id exist)
// read student full name by student_id, and group id (if group id exist, and student_id exist)
type Student = { student_id: string, firstname: string; lastname: string; };
type Group = { [id: string]: Student[]; };
const data4: Course = {};

// add student in course (if course id exist, and student_id does not exist)
// update student full name in course (if course id exist, and student_id exist)
// delete student from a course (if course id exist, and student_id exist)
// read student full name by student_id, and course id (if course id exist, and student_id exist)
type Course = { [id: string]: { title: string, students: Student[]; }; };
const data5: Course = {};

// add course (if course id does not exist)
// update course title (if course id exist)
// delete course (if course id exist)
// read course title by course id (if course id exist)
// add student in course (if course id exist, and student_id does not exist)
// update student full name in course (if course id exist, and student_id exist)
// delete student from a course (if course id exist, and student_id exist)
// read student full name by student_id, and course id (if course id exist, and student_id exist)
const data6: Course[] = [];

```

