# .NET Solution Templates & Shared Configuration

This repo contains standard, pre-configured setup files for .NET solutions. Following **Microsoft best practices and industry standards**, you just need to drop these files into your project's root folder to enforce strict code formatting, enable modern central package management, and unify build properties across all sub-projects. 

Using this setup ensures your codebase is production-ready, highly maintainable, and optimized for CI/CD DevOps pipelines.

## How to Use

1. Copy all these files directly into your root directory (where your `.sln` file lives).
2. Open `Directory.Build.props` and adjust the target .NET framework version if needed (e.g., `net8.0` or `net9.0`).
3. Open the solution with your favorite IDE. The standard formatting and central NuGet configurations will apply automatically.

## What's Included (Industry Standard Best Practices)

* **.editorconfig**
  * **Best Practice:** Enforces consistent C# coding styles and Roslyn static code analysis rules across the entire team. This eliminates "tab vs space" debates and keeps the codebase clean, no matter if devs use Visual Studio, VS Code, or Rider.
* **.gitignore**
  * **Standard Setup:** Pre-configured specifically for modern .NET workflows. It safely blocks build artifacts (`bin/`, `obj/`), IDE-specific user settings (`.vs/`), and local configuration secrets (`appsettings.Development.json`) from leaking into source control.
* **Directory.Build.props**
  * **Enterprise Architecture:** A shared MSBuild file to declare global properties—like `TargetFramework`, `Nullable`, `ImplicitUsings`, or strict `AnalysisLevel`—for all projects at once. It follows the DRY (Don't Repeat Yourself) principle, so you edit once here instead of modifying every single `.csproj` file.
* **Directory.Packages.props**
  * **Modern NuGet Management:** Enables Central Package Management (CPM), which is the current industry standard recommended by Microsoft. It allows you to manage and upgrade third-party library versions from a single place, completely preventing dependency hell and version drift mismatches between sub-projects.
