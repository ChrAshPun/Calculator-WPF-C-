# Calculator-WPF-CSharp
A Windows Presentation Foundation/C# Application

## A list of the WPF & C# concepts covered with this project

### 1. How XAML and C# Linking Works
`MainWindow.xaml.cs` is able access the elements in `MainWindow.xaml` due to the autogenerated file 
called `MainWindow.g.i.cs` located in the `obj` folder. Since MainWindow is a partial class, it's 
class definitions are spread across multiple files.

### 2. Two methods for creating Event Handlers
You can assign event handlers inline: `<Button x:Name="plusButton" Content="+" Click="OperationButton_Click"/>` or
you can assign event handlers inside the constructor: `plusButton.Click += OperationButton_Click;`

### 3. XAML Static Resources
The order of precendence is `inline styling > explicit styling > implicit styling`

`Inline styling` takes the highest precedence and applies only to the specific instance of the control that it's defined on.  
`Explicit styling` applies to controls that have an explicitly specified style, and completely replaces any implicit styles that would otherwise apply.  
`Implicit styling` applies to all controls of a certain type that don't have an explicit style set, and can be overridden by explicit styles.

Resources defined in `Application.Resources` can be accessed by any element in the entire application.

### 4. The out modifier
The variable used as the `out` parameter must be declared before it is passed as an argument to the method.
It must be assigned a value before it comes out of the function.
```
String a, b;
Split(“Stevie Ray Vaughn”, out a, out b);
Console.WriteLine (a); // Stevie Ray
Console.WriteLine (b); // Vaughn
```
