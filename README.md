# Student Grade Tracker  

**Name:** Tejas Padaki  
**Company:** CODTECH IT SOLUTIONS  
**ID:** CT08EFO  
**Domain:** PYTHON PROGRAMMING  
**Duration:** 17th December to 17th January  

---

## Overview of the Project  

### **TASK TWO:**  
Develop a Python program to track and manage student grades. This program allows users to:  
- Input grades for different subjects or assignments.  
- Calculate the average grade.  
- Display the overall grade with additional details like letter grade and GPA.

---

## Features  

1. **Add/Update Grades:** Input grades for various subjects or assignments.  
2. **Grade Summary:** Calculate and display the average grade, letter grade, and GPA.  
3. **User-Friendly GUI:** Easy interaction using a Tkinter-based interface.  
4. **Error Handling:** Ensures invalid inputs are handled gracefully.  

---

## How It Works  

The program is built around the `StudentGradeTracker` class and uses **Tkinter** for the GUI.  

### **Key Functionalities:**  
1. **Adding Grades:**  
   - Users input a subject name and a grade (0–100).  
   - The grade is stored or updated in a dictionary.  

2. **Calculating Average:**  
   - The average of all grades is calculated using a simple formula.  

3. **Letter Grade & GPA Conversion:**  
   - Numeric grades are mapped to letter grades and GPA using predefined scales.  

4. **Displaying Summary:**  
   - A detailed summary of all subjects, grades, the overall average, letter grade, and GPA is displayed in a text widget.  

---

## Key Insights  

- **Simplifying GUI Development:** Tkinter makes it easy to create standalone Python applications with graphical interfaces.  
- **Practical Algorithms:** Calculating averages, letter grades, and GPA showcases real-world use cases for programming logic.  
- **Error Handling:** Proper input validation improves the reliability of the program.  

---

## Generate the Points  

### **Objective:**  
- Create a lightweight and easy-to-use grade management system.  
- Allow users to track, calculate, and display grades effortlessly.  

### **Key Activities:**  
1. Design a Tkinter GUI for user interaction.  
2. Add and update grades dynamically.  
3. Implement calculations for averages, letter grades, and GPA.  

### **Technologies Used:**  
- **Python**: Core programming language.  
- **Tkinter**: For creating the GUI.  

### **Scope:**  
- Useful for students and teachers for basic grade tracking.  
- Applicable to small-scale educational setups.  

### **Advantages:**  
- Simple, intuitive, and user-friendly design.  
- No external dependencies required.  
- Lightweight and fast to execute.  

### **Disadvantages:**  
- No data persistence (grades are not saved after the program exits).  
- Limited functionality for larger datasets or institutions.  

## Example Code Snippet  

##python
##def add_grade(self):
    """Add or update a grade for a subject."""
    ##subject = self.subject_entry.get().strip()
    try:
        grade = float(self.grade_entry.get().strip())
        if not (0 <= grade <= 100):
            raise ValueError("Grade must be between 0 and 100.")
        self.grades[subject] = grade
        messagebox.showinfo("Success", f"Grade for '{subject}' has been added/updated.")
    except ValueError as e:
        messagebox.showerror("Error", f"Invalid input: {e}")

## Code Explanation  

The `StudentGradeTracker` class is the core of the application.

### **Initialization:**
- A dictionary stores grades for each subject.
- Tkinter widgets like labels, entry boxes, and buttons are created for the GUI.

### **Adding/Updating Grades:**
- Users input grades which are validated and stored in the dictionary.

### **Displaying Summary:**
- The program calculates the average, letter grade, and GPA, and displays them with all subjects and grades.

### **Letter Grade and GPA Conversion:**
- Numeric grades are converted into letter grades (A–F) and GPA on a scale of 4.0.

---

## Future Improvements  
- Implement file-based or database storage for data persistence.
- Add support for importing/exporting grade data.
- Enhance UI/UX with visualizations like charts or graphs.
- Add role-based access for teachers and students.

---

## Example Output  

### **Adding a grade:**
- Enter subject: Math`
- Enter grade: 95`
- Output: "Grade for 'Math' has been added/updated."

### **Displaying summary:**
##yaml
##Grade Summary:
  ##- Math: 95
##Overall Average: 95.00
##Letter Grade: A
##GPA: 4.00


### Contact  

For any questions or feedback, feel free to reach out to:  
**Tejas Padaki**  
**Company:** CODTECH IT SOLUTIONS  
**Email:** [tejaspadaki33@gmail.com](mailto:tejaspadaki33@gmail.com)  
