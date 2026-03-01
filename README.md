# To-Do List Application

A simple to-do list app built with .NET MAUI and ListView. Add, edit, and delete tasks with a clean interface.

## Features

- Add new tasks with title and details
- Edit existing tasks
- Delete tasks with confirmation
- View all tasks in a list
- Data stored in memory (no database needed)
- Input validation for task titles

## Requirements

- Visual Studio 2022
- .NET 8 SDK or later
- MAUI workload installed

## Installation and Running

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/ToDoMaui_Listview.git
   cd ToDoMaui_Listview
   ```

2. Install MAUI workload if needed
   ```bash
   dotnet workload install maui
   ```

3. Restore dependencies
   ```bash
   dotnet restore
   ```

4. Build the project
   ```bash
   dotnet build
   ```

5. Run the application
   ```bash
   dotnet maui run
   ```
   Or press F5 in Visual Studio

## How to Use

Adding a task:
- Type a task title (required, up to 50 characters)
- Add optional details (up to 240 characters)
- Click Add Task
- Task appears in the list

Editing a task:
- Click on any task in the list
- Edit the title or details in the input fields
- Click Update button
- Click Cancel to discard changes

Deleting a task:
- Click the trash button next to the task
- Confirm deletion
- Task is removed

## Project Structure

- Models/ToDoClass.cs - Task model with property binding
- MainPage.xaml - UI layout with ListView
- MainPage.xaml.cs - Event handlers and logic
- App.xaml, App.xaml.cs - Application setup
- AppShell.xaml, AppShell.xaml.cs - Navigation
- MauiProgram.cs - MAUI configuration
- ToDoMaui_Listview.csproj - Project file

## Troubleshooting

Project won't build:
- Run: dotnet workload install maui

ListView not showing items:
- Check that ItemsSource is set to todoList

Delete button not working:
- Verify ClassId="{Binding id}" in MainPage.xaml

Changes not updating:
- Make sure using ObservableCollection instead of List

## License

MIT License
