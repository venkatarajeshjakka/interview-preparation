1. What is .NET Core, and how does it differ from the .NET Framework?
Explanation: .NET Core is an open-source, cross-platform development framework that is maintained by Microsoft. It is a modern, lightweight, and modular framework designed for building high-performance applications. Unlike the .NET Framework, .NET Core is cross-platform, meaning it can run on Windows, macOS, and Linux.

2. What are the benefits of using .NET Core?
Explanation: .NET Core offers several advantages, including:
- Cross-platform support
- Improved performance
- Modularity and lightweight nature
- Side-by-side versioning
- Open-source and community-driven development

3. What are the main components of .NET Core?
Explanation: The main components of .NET Core are the Common Language Runtime (CLR), Base Class Libraries (BCL), and the CoreFX framework.

4. Explain the .NET Standard.
Explanation: The .NET Standard is a formal specification of .NET APIs that are intended to be available on all .NET implementations. It allows libraries to be compatible with multiple .NET platforms, including .NET Core, .NET Framework, and Xamarin.

5. Describe Dependency Injection (DI) in .NET Core.
Explanation: Dependency Injection is a design pattern used in .NET Core to achieve loose coupling between classes. It allows you to inject dependencies into a class instead of hardcoding them. This promotes better testability, maintainability, and scalability of applications.

Example:
```csharp
// Service interface
public interface IMyService
{
    void DoSomething();
}

// Service implementation
public class MyService : IMyService
{
    public void DoSomething()
    {
        // Do something here
    }
}

// Controller using DI
public class MyController : ControllerBase
{
    private readonly IMyService _myService;

    public MyController(IMyService myService)
    {
        _myService = myService;
    }

    // Action method using the service
    public IActionResult MyAction()
    {
        _myService.DoSomething();
        return Ok();
    }
}
