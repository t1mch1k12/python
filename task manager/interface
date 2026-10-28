import tkinter as tk
from tkinter import ttk


class Interface:
    def __init__(self):
        # Создание главного окна приложения
        self.root = tk.Tk()
        self.root.title("Task Manager")
        self.root.geometry("600x400")
        self.root.minsize(400, 300)

        # Настройки главного окна
        self.root.configure(bg="#f0f0f0")

        # Заголовок приложения
        self.title_label = tk.Label(
            self.root,
            text="Task Manager",
            font=("Arial", 20, "bold"),
            bg="#f0f0f0"
        )
        self.title_label.pack(pady=20)

        # Поле для ввода задачи
        self.task_entry = tk.Entry(
            self.root,
            font=("Arial", 12),
            width=35
        )
        self.task_entry.pack(pady=10)

        # Кнопка добавления задачи
        self.add_button = tk.Button(
            self.root,
            text="Добавить задачу",
            font=("Arial", 11),
            command=self.add_task
        )
        self.add_button.pack(pady=5)

        # Список задач
        self.task_list = tk.Listbox(
            self.root,
            font=("Arial", 12),
            width=45,
            height=10
        )
        self.task_list.pack(pady=10)

    def add_task(self):
        task = self.task_entry.get().strip()

        if task:
            self.task_list.insert(tk.END, task)
            self.task_entry.delete(0, tk.END)

    def run(self):
        self.root.mainloop()
