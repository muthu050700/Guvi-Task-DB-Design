1. Student Entity
   Fields: studentId, fullName, email, password, batch, task, mentorId, coordinatorId, capstoneProject.

Key Relationships:
Linked to a mentor, batch, tasks, coordinator, queries created by the student, and capstone project.

2. Mentor Entity
   Fields: mentorId, fullName, email, password, batchs, batchTask.

Key Relationships:
Manages batches, is responsible for tasks, evaluates capstone projects, and is assigned queries.

3. Coordinator Entity
   Fields: \_Id, fullName, email, password, batchs.

Key Relationships:
Manages multiple batches but doesn't have explicit relationships with students or tasks directly.

4. Batch Entity
   Fields: batchId, batchTitle, students, assignedTo, TotalClass.

Key Relationships:
Contains students, is assigned to a mentor, and relates to classes and capstone projects.

5. Class Entity
   Fields: \_id, batch, noOfDays.

Key Relationships:
Linked to a batch, showing how long the class runs.

6. Query Entity
   Fields: \_id, topic, language, querieTitle, querieDescription, availableTime, createdAt, createdBy, assignedTo, complete.

Key Relationships:
Created by students, assigned to mentors.

7. Task Entity
   Fields: \_id, createdBy, assignedTo, subTasks.

Key Relationships:
Created by students, assigned to mentors, contains subtasks.

8. SubTask Entity
   Fields: \_id, submittedAt, submittedBy, assignedTo, subTaskTitle, grade, comment, submittedOn.

Key Relationships:
Part of tasks, submitted by students, graded by mentors.

9. Capstone Entity
   Fields: \_id, projectTitle, projectDescription, frontendDevelopment, backendDevelopment, submittedOn, batch, score, assignedTo, evaluatedBy.
   Key Relationships:
   Assigned to students, evaluated by mentors, related to batches.
