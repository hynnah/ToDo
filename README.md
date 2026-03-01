# MAUI To-Do List Application

A simple and elegant To-Do List application built with **.NET MAUI** and **ListView**. This project demonstrates MVVM concepts with data binding, input validation, and CRUD operations without requiring a database.

## 📱 Features

✅ **Add Tasks** - Create new to-do items with title and optional details  
✅ **Edit Tasks** - Click any task to edit and update its content  
✅ **Delete Tasks** - Remove tasks with confirmation dialog  
✅ **ListView Display** - Clean, modern UI to view all tasks  
✅ **Data Binding** - Uses ObservableCollection for real-time updates  
✅ **Input Validation** - Prevents empty task titles  
✅ **No Database** - All data stored in memory using ObservableCollection  

## 🛠️ Tech Stack

- **.NET 8** or later
- **.NET MAUI** (Multi-platform App UI)
- **C#** programming language
- **XAML** for UI layout
- **MVVM Pattern** with INotifyPropertyChanged

## 📂 Project Structure

```
ToDoMaui_Listview/
├── Models/
│   └── ToDoClass.cs          # To-Do model with property binding
├── MainPage.xaml             # UI layout with ListView
├── MainPage.xaml.cs          # Code-behind with event handlers
├── App.xaml                  # Application configuration
├── App.xaml.cs               # Application code-behind
├── AppShell.xaml             # App shell configuration
├── MauiProgram.cs            # MAUI app configuration
├── ToDoMaui_Listview.csproj  # Project file
└── README.md                 # This file
```

## 🚀 Getting Started

### Prerequisites

- Visual Studio 2022 (Community, Professional, or Enterprise)
- .NET 8 SDK or later
- MAUI workload installed

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/ToDoMaui_Listview.git
   cd ToDoMaui_Listview
   ```

2. **Install MAUI Workload** (if not already installed)
   ```bash
   dotnet workload install maui
   ```

3. **Restore Dependencies**
   ```bash
   dotnet restore
   ```

4. **Build the Project**
   ```bash
   dotnet build
   ```

5. **Run the Application**
   ```bash
   dotnet maui run
   ```
   Or press **F5** in Visual Studio

## 💡 How to Use

### Adding a Task
1. Enter a **Task Title** (required, max 50 characters)
2. Enter **Task Details** (optional, max 240 characters)
3. Click the **"Add Task"** button
4. Task appears in the list below

### Editing a Task
1. **Click** on any task in the list
2. The task details will populate in the input fields
3. **Modify** the title or details
4. Click the **"Update"** button
5. Click **"Cancel"** to discard changes

### Deleting a Task
1. Click the **🗑️ (trash)** button next to any task
2. Confirm the deletion in the dialog
3. Task is removed from the list

## 📝 Code Structure

### ToDoClass.cs
- Implements `INotifyPropertyChanged` for data binding
- Properties: `id`, `title`, `detail`
- Automatically notifies UI when properties change

### MainPage.xaml
- **Input Section**: Entry for title, Editor for details, buttons for actions
- **ListView**: Displays all tasks with title, details, and delete button
- Uses **Data Binding** to connect UI to data

### MainPage.xaml.cs
- **AddToDoItem()**: Adds new task to collection
- **EditToDoItem()**: Updates selected task
- **DeleteToDoItem()**: Removes task with confirmation
- **TodoLV_OnItemSelected()**: Handles task selection for editing
- **ClearInputs()**: Resets input fields
- **ShowAddButton()** / **ShowEditButton()**: Manages button visibility

## 🎨 UI Design

- **Color Scheme**: Modern blue, green, and red accents
- **Responsive Layout**: Works on phones, tablets, and desktop
- **Material Design**: Clean frames with shadows and rounded corners
- **Three-Column Button Layout**: Add, Update, Cancel buttons

## 🔄 Data Flow

```
User Input → MainPage.xaml.cs Event Handler 
    ↓
ToDoClass Instance Created/Updated
    ↓
Added/Modified in ObservableCollection
    ↓
ListView Automatically Updates (via Binding)
```

## 🐛 Troubleshooting

### Issue: Project won't build
**Solution**: Install MAUI workload
```bash
dotnet workload install maui
```

### Issue: ListView shows no items
**Solution**: Ensure ItemsSource is set to the ObservableCollection
```csharp
todoLV.ItemsSource = todoList;
```

### Issue: Delete button doesn't work
**Solution**: Verify ClassId binding in XAML
```xml
ClassId="{Binding id}"
```

### Issue: Changes not reflecting in ListView
**Solution**: Use ObservableCollection instead of List<T>
```csharp
todoList = new ObservableCollection<ToDoClass>();
```

## 📚 Learning Resources

- [Microsoft MAUI Documentation](https://learn.microsoft.com/en-us/dotnet/maui/)
- [MVVM Pattern in MAUI](https://learn.microsoft.com/en-us/dotnet/maui/fundamentals/mvvm)
- [Data Binding in MAUI](https://learn.microsoft.com/en-us/dotnet/maui/fundamentals/data-binding/)
- [ListView Control](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/controls/listview)

## 🚀 Future Enhancements

- Add SQLite database for data persistence
- Implement task categories/tags
- Add due dates and reminders
- Add task priority levels
- Implement search and filtering
- Dark/Light theme support
- Task completion checkboxes
- Data export to CSV

## 👤 Author

Created for learning MAUI development

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## 📞 Support

If you encounter any issues or have questions:
1. Check the Troubleshooting section
2. Review the code comments
3. Open an issue on GitHub
4. Refer to the official MAUI documentation

---

**Happy Coding! 🎉**
