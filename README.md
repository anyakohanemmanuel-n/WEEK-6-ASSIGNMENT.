# WEEK-6-ASSIGNMENT.
assignment.js
// Student Records Manager

// 1. Array of student objects
const students = [
  { name: "Amina", age: 22, course: "Web Development", score: 72 },
  { name: "Chidi", age: 24, course: "Data Science", score: 65 },
  { name: "Ngozi", age: 21, course: "Cyber Security", score: 54 },
  { name: "Tunde", age: 23, course: "Mobile Development", score: 41 },
  { name: "Efe", age: 20, course: "UI/UX Design", score: 88 },
  { name: "Bola", age: 25, course: "Web Development", score: 49 },
];

// 2. Return a letter grade based on score
function getGrade(score) {
  if (score >= 70) return "A";
  if (score >= 60) return "B";
  if (score >= 50) return "C";
  return "F";
}

// 3. Log a sentence describing one student
function displayStudent(student) {
  console.log(
    `${student.name} (${student.age}) is studying ${student.course} and scored ${student.score} - Grade ${getGrade(student.score)}`
  );
}

// 4. Display every student using forEach
console.log("--- All Students ---");
students.forEach(displayStudent);

// 5. Filter students who passed (score of 50 or above)
const passedStudents = students.filter((student) => student.score >= 50);
console.log("\n--- Students Who Passed ---");
console.log(passedStudents);

// 6. Map to an array of student names
const studentNames = students.map((student) => student.name);
console.log("\n--- Student Names ---");
console.log(studentNames);

// 7. Bonus: average score of all students
function averageScore(students) {
  if (students.length === 0) return 0;
  const total = students.reduce((sum, student) => sum + student.score, 0);
  return total / students.length;
}

console.log("\n--- Average Score ---");
console.log(averageScore(students).toFixed(2));
