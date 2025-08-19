# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a .NET 9 Blazor Server application that demonstrates configuration-driven UI rendering. The core concept allows pages to be built dynamically using configuration objects rather than static markup.

## Development Commands

**Build and Run:**
```bash
cd BlazorAsConfiguration/BlazorAsConfiguration
dotnet build
dotnet run
```

**Development Server:**
- HTTP: http://localhost:5141
- HTTPS: https://localhost:7048

**Project Structure Commands:**
```bash
dotnet build BlazorAsConfiguration/BlazorAsConfiguration.sln
dotnet run --project BlazorAsConfiguration/BlazorAsConfiguration/BlazorAsConfiguration.csproj
```

## Architecture

**Configuration-Driven UI System:**
- `UIConfig` DTO defines UI elements with Type, Data, and Action properties
- `AppConfigLayout` component renders UI elements based on configuration arrays
- Supports dynamic rendering of h1, button, p, and break elements
- Actions are bound as C# delegates for interactive elements

**Key Components:**
- `UIConfig.cs`: Core DTO for UI configuration (Type, Data, Action)
- `AppConfigLayout.razor`: Dynamic rendering engine using switch statements
- `Home.razor`: Example implementation showing configuration array usage

**Blazor Configuration:**
- Interactive Server Components enabled
- .NET 9 with nullable reference types
- Static file serving and antiforgery protection configured
- Standard Blazor project structure with Components, Pages, Layout folders

The application demonstrates how UI can be constructed programmatically through configuration objects, allowing for flexible and dynamic page layouts without hardcoded markup.