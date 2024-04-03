# Pop_Up
testing pop up and save reults

import tkinter as tk
import random
import time

def flash_color():
    colors = ["light blue",  "violet"]
    random_color = random.choice(colors)
    label.config(bg=random_color)
    root.after(1000,flash_color)

# Create the main window
root = tk.Tk()
root.title("Flashing Colors")

# Create a label for the text
label = tk.Label(root, text="This app is broken, please try again later", font=("Helvetica", 24))
label.pack(expand=True, fill="both")

# Start flashing colors
flash_color()

# Run the application
root.mainloop()


