# How to localize when resource file present in different assembly or default namespace is not same as assembly name
 
## WPF-localization-ResX-file
By default, SfDataGrid reads the localization resource files based on assembly name from its default namespace. If you are having the localization resource file other than the executing assembly (Assembly.GetExecutingAssembly())or other than default namespace, then you have to pass the **assembly having the resource file** and **it’s default namespace** to  **Syncfusion.UI.Xaml.Grid.GridResourceWrapper.SetResources** method.

## C#: 

```C#
public MainWindow()
{
  Syncfusion.UI.Xaml.Grid.GridResourceWrapper.SetResources(Application.Current.GetType().Assembly, "namespacename");
    InitializeComponent();
}
```
 