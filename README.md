# RzError
Sample showcasing error with Razden Blazor Studio

Global usings were added to RzError.csproj

```
<ItemGroup>
    <Using Include="Radzen" />
    <Using Include="Radzen.Blazor" />

    <Using Include="Microsoft.JSInterop" />
    <Using Include="Microsoft.AspNetCore.Components" />
    <Using Include="Microsoft.AspNetCore.Components.Web" />
</ItemGroup>
```

Those same usings were removed from Pages/Test.razor.cs

```
using Microsoft.AspNetCore.Components;
using Microsoft.AspNetCore.Components.Web;
using Microsoft.JSInterop;
using Radzen;
using Radzen.Blazor;
```

When I try view Test.razor in preview mode by double-clicking on Test.razor, and error is thrown.


Page threw exception during rendering.

```
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(11,19): error CS0246: The type or namespace name 'IJSRuntime' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(14,19): error CS0246: The type or namespace name 'NavigationManager' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(17,19): error CS0246: The type or namespace name 'DialogService' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(20,19): error CS0246: The type or namespace name 'TooltipService' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(23,19): error CS0246: The type or namespace name 'ContextMenuService' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(26,19): error CS0246: The type or namespace name 'NotificationService' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(10,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(10,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(13,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(13,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(16,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(16,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(19,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(19,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(22,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(22,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(25,10): error CS0246: The type or namespace name 'InjectAttribute' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor.cs(25,10): error CS0246: The type or namespace name 'Inject' could not be found (are you missing a using directive or an assembly reference?)
C:\Users\Brad\source\repos\rzError\Pages\Test.razor(110,65): error CS0144: Cannot create an instance of the abstract type or interface 'IJSRuntime'
C:\Users\Brad\source\repos\rzError\Pages\Test.razor(111,72): error CS0144: Cannot create an instance of the abstract type or interface 'NavigationManager'
C:\Users\Brad\source\repos\rzError\Pages\Test.razor(112,72): error CS7036: There is no argument given that corresponds to the required formal parameter 'uriHelper' of 'DialogService.DialogService(NavigationManager, IJSRuntime)'
C:\Users\Brad\source\repos\rzError\Pages\Test.razor(113,73): error CS7036: There is no argument given that corresponds to the required formal parameter 'uriHelper' of 'TooltipService.TooltipService(NavigationManager)'
C:\Users\Brad\source\repos\rzError\Pages\Test.razor(114,77): error CS7036: There is no argument given that corresponds to the required formal parameter 'uriHelper' of 'ContextMenuService.ContextMenuService(NavigationManager)'

   at Radzen.Server.ProjectContext.Compile(Compilation compilation, AssemblyLoadContext context) in /Users/korchev/github/radzen-next/Radzen.Server/ProjectContext.cs:line 180
   at Radzen.Server.ProjectServer.Compile(String fileName, String source, RazorProjectEngine projectEngine) in /Users/korchev/github/radzen-next/Radzen.Server/ProjectServer.cs:line 776
   at Radzen.Server.ProjectServer.CompilePage(String fileName, String source, RazorProjectEngine engine) in /Users/korchev/github/radzen-next/Radzen.Server/ProjectServer.cs:line 318
   at Radzen.Server.ProjectServer.Render(String fileName, String source) in /Users/korchev/github/radzen-next/Radzen.Server/ProjectServer.cs:line 392
   at Radzen.Server.ProgramController.Render(RenderRequest request) in /Users/korchev/github/radzen-next/Radzen.Server/ProgramController.cs:line 325
   ```
   
