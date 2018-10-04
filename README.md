# Coalesce KnockoutJS Dotnet CLI Template

[![Build status](https://ci.appveyor.com/api/projects/status/is5s6a178hitgonv/branch/master?svg=true)](https://ci.appveyor.com/project/IntelliTect/coalesce-knockoutjs-template/branch/master)

This template will set up a barebones Coalesce solution using the
KnockoutJS generators which you can build your app upon.

For more information on Coalesce, visit: [http://coalesce.intellitect.com/](http://coalesce.intellitect.com/)

For the Coalesce source code, visit: [https://github.com/IntelliTect/Coalesce](https://github.com/IntelliTect/Coalesce)

## Template Installation

From a command prompt, run:

`CMD> dotnet new --install IntelliTect.Coalesce.KnockoutJS.Template`

You should now see the template in the listing:

```
CMD> dotnet new --list

Templates                                             Short Name       Language          Tags
------------------------------------------------------------------------------------------------------------
Console Application                                   console          [C#], F#, VB      Common/Console
Class library                                         classlib         [C#], F#, VB      Common/Library
Unit Test Project                                     mstest           [C#], F#, VB      Test/MSTest
xUnit Test Project                                    xunit            [C#], F#, VB      Test/xUnit
ASP.NET Core Empty                                    web              [C#], F#          Web/Empty
ASP.NET Core Web App (Model-View-Controller)          mvc              [C#], F#          Web/MVC
IntelliTect Coalesce Web App KnockoutJS Template      coalesceko       [C#]              Web/MVC/KnockoutJS
ASP.NET Core Web App                                  razor            [C#]              Web/MVC/Razor Pages
ASP.NET Core with Angular                             angular          [C#]              Web/MVC/SPA
ASP.NET Core with React.js                            react            [C#]              Web/MVC/SPA
ASP.NET Core with React.js and Redux                  reactredux       [C#]              Web/MVC/SPA
ASP.NET Core Web API                                  webapi           [C#], F#          Web/WebAPI
global.json file                                      globaljson                         Config
NuGet Config                                          nugetconfig                        Config
Web Config                                            webconfig                          Config
Solution File                                         sln                                Solution
Razor Page                                            page                               Web/ASP.NET
MVC ViewImports                                       viewimports                        Web/ASP.NET
MVC ViewStart                                         viewstart                          Web/ASP.NET

```

## Creating a new Coalesce project using the template

1. Make a new folder and open it in a command prompt

1. Run: `CMD> dotnet new coalesceko [-n Optional.Name]`

If you don't specify a name, the template will infer one from the name of the folder you are in.

At this point, you can open up Visual Studio, restore npm packages and nuget pacakges, and then run the app. However, you will probably want to do the following before running:

1. Create an initial data model by adding EF entity classes to the data project and the corresponding `DbSet<>` properties to `AppDbContext`. You will notice that this project includes a single model, `ApplicationUser`, to start with.
1. Run the `coalesce` task in the Task Runner Explorer to trigger Coalesce's code generation (or run `dotnet coalesce` in the web project's path).
1. Run `dotnet ef migrations add Init` (`Init` can be any name) in the data project to create the initial database migration.

After you've started to grow content with your project, consider the following:

* Remove the dummy authentication from `Startup.cs` and implement a proper authentication scheme.

## Themeing
Visit [Bootswatch](https://bootswatch.com/3/) to see the different choices available for themes.  To change themes, simply change the name of the imports in site.scss in the two marked locations.
