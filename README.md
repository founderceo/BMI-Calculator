# BMI-Calculator
Walkthrough project - first ever
#Start Code
from cProfile import label
from distutils import command
import tkinter
import tkinter.messagebox

root = tkinter.Tk()
root.title("BMI Calculator")

#BMI Calculating function
def calculate_bmi():
    kg = float(entry_kg.get())
    height = float(entry_height.get())
    bmi = round(kg / (height ** 2), 2)
    label_result['text'] = f"BMI: {bmi}"

#Create the GUI
label_kg = tkinter.Label(root, text = "KG: ")
label_kg.grid(column=0, row=0)
entry_kg = tkinter.Entry(root)
entry_kg.grid(column=1, row=0)

label_height = tkinter.Label(root, text = "HEIGHT: ")
label_height.grid(column=0, row=1)
entry_height = tkinter.Entry(root)
entry_height.grid(column=1, row=1)

label_result = tkinter.Label(root, text = "BMI Shown Here ")
label_result.grid(column=1, row=2)

calc_button = tkinter.Button(root, text = "CALCULATE", command=calculate_bmi)
calc_button.grid(column=0, row=2)


root.mainloop()
