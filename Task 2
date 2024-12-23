import tkinter as tk
from tkinter import messagebox

class StudentGradeTracker:
    def __init__(self, root):
        """Initialize the grade tracker and GUI."""
        self.grades = {}  # Dictionary to store subjects and their grades
        self.root = root
        self.root.title("Student Grade Tracker")
        self.root.geometry("400x500")

        # Widgets for the GUI
        self.title_label = tk.Label(root, text="Student Grade Tracker", font=("Helvetica", 16, "bold"))
        self.title_label.pack(pady=10)

        self.subject_label = tk.Label(root, text="Enter Subject:")
        self.subject_label.pack()
        self.subject_entry = tk.Entry(root, width=30)
        self.subject_entry.pack(pady=5)

        self.grade_label = tk.Label(root, text="Enter Grade (0-100):")
        self.grade_label.pack()
        self.grade_entry = tk.Entry(root, width=30)
        self.grade_entry.pack(pady=5)

        self.add_button = tk.Button(root, text="Add/Update Grade", command=self.add_grade)
        self.add_button.pack(pady=10)

        self.display_button = tk.Button(root, text="Display Summary", command=self.display_summary)
        self.display_button.pack(pady=10)

        self.exit_button = tk.Button(root, text="Exit", command=root.quit)
        self.exit_button.pack(pady=10)

        self.output_text = tk.Text(root, height=15, width=40, state="disabled", wrap="word")
        self.output_text.pack(pady=10)

    def add_grade(self):
        """Add or update a grade for a subject."""
        subject = self.subject_entry.get().strip()
        try:
            grade = float(self.grade_entry.get().strip())
            if not (0 <= grade <= 100):
                raise ValueError("Grade must be between 0 and 100.")
            self.grades[subject] = grade
            messagebox.showinfo("Success", f"Grade for '{subject}' has been added/updated.")
            self.subject_entry.delete(0, tk.END)
            self.grade_entry.delete(0, tk.END)
        except ValueError as e:
            messagebox.showerror("Error", f"Invalid input: {e}")

    def calculate_average(self):
        """Calculate the average of all grades."""
        if not self.grades:
            return 0
        return sum(self.grades.values()) / len(self.grades)

    def get_letter_grade(self, average):
        """Convert numeric average to a letter grade."""
        if average >= 90:
            return "A"
        elif average >= 80:
            return "B"
        elif average >= 70:
            return "C"
        elif average >= 60:
            return "D"
        else:
            return "F"

    def get_gpa(self, average):
        """Convert numeric average to GPA (scale: 4.0)."""
        if average >= 90:
            return 4.0
        elif average >= 80:
            return 3.0
        elif average >= 70:
            return 2.0
        elif average >= 60:
            return 1.0
        else:
            return 0.0

    def display_summary(self):
        """Display the grade summary."""
        if not self.grades:
            messagebox.showinfo("Summary", "No grades entered yet.")
            return

        summary = "Grade Summary:\n"
        for subject, grade in self.grades.items():
            summary += f" - {subject}: {grade}\n"

        average = self.calculate_average()
        letter_grade = self.get_letter_grade(average)
        gpa = self.get_gpa(average)

        summary += f"\nOverall Average: {average:.2f}\n"
        summary += f"Letter Grade: {letter_grade}\n"
        summary += f"GPA: {gpa:.2f}\n"

        self.output_text.configure(state="normal")
        self.output_text.delete("1.0", tk.END)
        self.output_text.insert(tk.END, summary)
        self.output_text.configure(state="disabled")

# Main program
if __name__ == "__main__":
    root = tk.Tk()
    tracker = StudentGradeTracker(root)
    root.mainloop()
