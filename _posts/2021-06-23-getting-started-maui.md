---
title: Getting Started with .NET MAUI
tags: DotNET CSharp MAUI CrossPlatform
readtime:
key: getting-started-maui
canonical:
---

> <i class="fas fa-exclamation-circle"></i> .NET MAUI is still in Preview, and the team at Microsoft continuously release changes. Some tools, features, and steps may change or not work as expected.

This tutorial provides an overview of how to get started with [.NET MAUI](https://github.com/dotnet/maui), the .NET Multi-platform APP UI (MAUI), a cross-platform framework for creating native mobile and desktop apps using C# and XAML. .NET MAUI is the evolution of Xamarin.Forms and currently available in [Preview 5](https://devblogs.microsoft.com/dotnet/announcing-net-maui-preview-5/).

To find out more about what is .NET MAUI and how it came to be, I recommend reading my blog post [Aloha! Welcome to .NET MAUI](https://melissahoughton.dev/2021/06/13/aloha-maui.html) before continuing with this tutorial.

We will cover:

- Setting up your environment
- Creating your first .NET MAUI application
- Adding a feature to the application

## Environment Setup

Before starting with a .NET MAUI project, we need to install all the proper dependencies. Microsoft has made this easy for us with a `dotnet tool` that evaluates your system. The tool will detect any problems and offer to try to fix them for you or suggest a way to fix them yourself.

First install the tool: (source: <https://github.com/Redth/dotnet-maui-check>)

```bash
dotnet tool install -g Redth.Net.Maui.Check
```

Run the tool using the command:

```bash
maui-check
```

Follow the instructions given in the tool to get everything you need to start working with .NET MAUI.

![MAUI Check tool screenshot](https://melissadevstorage.blob.core.windows.net/melissadevblob/maui/maui-check.png)

For the best development experience with .NET MAUI, it is recommended you use Visual Studio.

At the time of writing, Microsoft recommends starting with [Visual Studio 2019 16.11 Preview 2](https://visualstudio.microsoft.com/vs/preview/) to develop .NET MAUI applications. Full support for .NET MAUI will be available in [Visual Studio 2022](https://devblogs.microsoft.com/visualstudio/visual-studio-2022/), now in Preview.

Install the following workloads with Visual Studio:

- Mobile development with .NET
- Universal Windows Platform development
- Desktop development with C++
- .NET Desktop Development

![Visual Studio workloads](https://docs.microsoft.com/en-us/dotnet/maui/get-started/installation-images/vs-workloads.png)<em class="sub-title center">Source: [Microsoft](https://docs.microsoft.com/en-us/dotnet/maui/get-started/installation)</em>

To run and debug in an Android emulator, setup an emulator within Visual Studio following this guide <https://docs.microsoft.com/en-us/xamarin/android/get-started/installation/android-emulator/>

Once you have installed all that and the `maui-check` succeeds, you are ready to create your first .NET MAUI application!

## Create a new MAUI app

This guide will use Visual Studio to create our first .NET MAUI application. However, you can also create a new .NET MAUI application from the command line.

In Visual Studio 16.11 Preview 2, select `Create a new project`, then search for `MAUI` or choose `Project Type > MAUI` from the dropdown.

![Create project](https://melissadevstorage.blob.core.windows.net/melissadevblob/maui/new-project.png)

The generated template contains two projects:

1. .NET MAUI project - targetting Android, iOS, and MacCatalyst
2. WinUI Project - for Windows desktop applications

![New project structure](https://melissadevstorage.blob.core.windows.net/melissadevblob/maui/maui-app.png)

The team is working hard to consolidate all the projects into one to build and deploy across all platforms. The final consolidation will come in later versions.

Run the application by selecting the target device, such as `Android Emulator`, in the Visual Studio toolbar dropdown next to the `Start` button.

The application is a simple Hello World counter app with a button to increase the counter.

![Template app image](https://melissadevstorage.blob.core.windows.net/melissadevblob/maui/template-app.png)

Congratulations! You have created and run your first .NET MAUI application!

> <i class="fas fa-exclamation-circle"></i> At the time of writing, there are a few bugs in the layout of the template application. [(issue #1382)](https://github.com/dotnet/maui/issues/1382)

### Fix the layout issues

The two issues in the template application are:

- Image does not show
- Numbers with multiple digits are cut off at the first digit

To fix this, we can change the layout from the `StackLayout` to a `VerticalStackLayout`, newly introduced in .NET MAUI and remove each `Grid.Row`.

Checkout this [commit](https://github.com/melissahoughton/GettingStartedMaui/commit/969e1b9946a0b3460348b0774444f26997c2a2cf) on my github for the full details of the change.

### Troubleshooting

As is to be expected with any preview, there are some issues you may have to address before you can fully get the project up and running. Below are the issues I ran into when writing this blog post.

#### Issue: Android Emulator crashes after launch

To fix this, disable XAML Hot Reload in Visual Studio, follow the instructions in [this comment](https://github.com/dotnet/maui/issues/1361#issuecomment-864393535) from the existing issue: <https://github.com/dotnet/maui/issues/1361>

#### Issue: Previous installations of .NET 6 Preview 4 cause issues in .NET 6 Preview 5

See the Microsoft documentation here: <https://github.com/dotnet/core/blob/main/release-notes/6.0/known-issues.md#preview-5>

I expect the team will continue to work through all the [issues](https://github.com/dotnet/maui/issues) leading up to General Availablity in November.

## Adding a Feature

Let's add our first feature.

// TODO
