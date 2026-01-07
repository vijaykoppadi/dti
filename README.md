# dti

https://classroom.github.com/a/6qpf5dvg




import tkinter as tk
from tkinter import messagebox

def analyze_usage():
    hours = float(entry.get())

    if hours < 2:
        msg = "✅ Good usage! Keep it balanced."
    elif hours <= 5:
        msg = "⚠️ Moderate usage. Take small breaks."
    else:
        msg = "🚨 High screen time! Consider digital detox."

    messagebox.showinfo("Digital Wellbeing Result", msg)

# GUI Window
root = tk.Tk()
root.title("AI-Inspired Digital Wellbeing Tracker")
root.geometry("350x200")

tk.Label(root, text="📱 Screen Time Today (Hours)", font=("Arial", 12)).pack(pady=10)

entry = tk.Entry(root)
entry.pack()

tk.Button(root, text="Analyze Usage", command=analyze_usage).pack(pady=20)

root.mainloop()
