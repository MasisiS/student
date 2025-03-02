CREATE TABLE Student (
STU_NUM int(6) NOT NULL,
STU_SNAME varchar(15) NOT NULL,
STU_FNAME varchar(15) NOT NULL,
STU_INITIAL varchar(1),
STU_STARTDATE DATE ,
COURSE_CODE varchar(3),
PROJ_NUM int(2),
CONSTRAINT PK_Employee PRIMARY KEY (STU_NUM)
);

INSERT INTO Student(STU_NUM, STU_SNAME, STU_FNAME, STU_INITIAL, STU_STARTDATE, COURSE_CODE, PROJ_NUM)
VALUES (01, 'Snow', 'Jon', 'E', '2014-04-05', 201, 6),
       (02, 'Stark', 'Arya', 'C', '2017-07-12', 305, 11),
       (03, 'Lannister', 'Jamie', 'C', '2012-09-05', 101, 2),
       (04, 'Lannister', 'Cercei', 'J', '2012-09-05', 101, 2),
       (05, 'Greyjoy', 'Theon', 'I', '2015-12-09', 402, 14),
       (06, 'Tyrell', 'Margaery', 'Y', '2017-07-12', 305, 10),
       (07, 'Baratheon', 'Tommen', 'R', '2019-06-13', 201, 5);   
	   

SELECT * FROM Student
WHERE course_code = 305 -- Display student information of course code 305

UPDATE Student -- Request to update from Student table
SET course_code = 304
WHERE stu_num = 07;	   -- Request to update from the person whose student number is 07.

DELETE FROM Student
WHERE stu_sname = 'Lannister' AND stu_fname = 'Jamie' AND stu_startdate = '2012-09-05' AND course_code = 101 AND proj_num = 2;

UPDATE Student
set proj_num = 14
WHERE stu_startdate <= '2016-01-01' and course_code >= 201

TRUNCATE TABLE Student;
