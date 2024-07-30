# Programming-languages

#include <stdio.h>


char calculateGrade(int marks) {
    if (marks >= 90) {
        return 'A';
    } else if (marks >= 80) {
        return 'B';
    } else if (marks >= 70) {
        return 'C';
    } else if (marks >= 60) {
        return 'D';
    } else {
        return 'F';
    }
}


int inputMarks(int subjectNumber) {
    int marks;
    printf("Enter marks for Subject %d: ", subjectNumber);
    scanf("%d", &marks);
    return marks;
}


void printTranscript(int marks1, char grade1, int marks2, char grade2, int marks3, char grade3) {
    printf("\n--- Transcript ---\n");
    printf("Subject 1: Marks = %d, Grade = %c\n", marks1, grade1);
    printf("Subject 2: Marks = %d, Grade = %c\n", marks2, grade2);
    printf("Subject 3: Marks = %d, Grade = %c\n", marks3, grade3);
}

int main() {
    int marks1, marks2, marks3;
    char grade1, grade2, grade3;

    
    marks1 = inputMarks(1);
    marks2 = inputMarks(2);
    marks3 = inputMarks(3);

    
    grade1 = calculateGrade(marks1);
    grade2 = calculateGrade(marks2);
    grade3 = calculateGrade(marks3);

    
    printTranscript(marks1, grade1, marks2, grade2, marks3, grade3);

    return 0;
}
