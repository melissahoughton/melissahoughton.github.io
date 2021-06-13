---
title: Aloha! Welcome to .NET MAUI
tags: DotNET CSharp MAUI CrossPlatform
readtime: 6
key: aloha-maui
canonical: https://melissahoughton-dev.medium.com/aloha-welcome-to-net-maui-46274235abb9
---

Aloha! Welcome to .NET MAUI! The all-new .NET Multi-platform App UI (MAUI). Announced at [Microsoft Build 2020](https://news.microsoft.com/build-2020-book-of-news/), Microsoft has evolved Xamarin.Forms and taken the next step in the [.NET unification](https://channel9.msdn.com/Events/Build/2020/BOD106) to give you a cross-platform mobile-first framework for Android, iOS, macOS, and Windows. .NET MAUI will introduce new ways to build applications. Available in [.NET 6](https://dotnet.microsoft.com/download/dotnet/6.0), in preview now!

![.NET MAUI](https://melissadevstorage.blob.core.windows.net/melissadevblob/dotnet maui.png)<em class="sub-title center" >.NET MAUI (source: [Microsoft](https://youtu.be/GJ_PaRNDe9E))</em>

## What is .NET MAUI?

> .NET Multi-platform App UI (MAUI) is the evolution of Xamarin.Forms extended from mobile to desktop scenarios with UI controls rebuilt from the ground up for performance and extensibility

_Maddy Leger, Program Manager Xamarin/.NET MAUI Team "[The Future of Native Apps Development in .NET 6](https://youtu.be/fPEdgXeqhE4)"_

MAUI will help you deliver high-performance, cross-platform, native desktop and mobile apps from a single codebase. With .NET MAUI, you can build your apps for any device from a single codebase and project system, using one language, one set of libraries, and one UI stack for all.

### What are Xamarin and Xamarin.Forms?

The most common descriptor for MAUI is _the evolution of Xamarin.Forms_, but what are Xamarin and Xamarin.Forms?

Xamarin is an open-source .NET platform for building iOS, Andriod, macOS, and Windows applications. Introduced in 2011, Xamarin allows you to share business logic across platforms using .NET while creating a native UI for each. Xamarin allows developers to share an average of [90% of their application across platforms](https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin)).

![.NET Mobile Apps with Xamarin](https://melissadevstorage.blob.core.windows.net/melissadevblob/xamarin.png)<em class="sub-title center">.NET Mobile Apps with Xamarin (source: [Microsoft](https://channel9.msdn.com/Events/Build/2020/BOD107))</em>

To help with the overhead of creating native UI's for each platform, we have Xamarin.Forms.

Xamarin.Forms is an open-source UI framework that allows you to combine the code for Xamarin.Android, Xamarin.iOS, Xamarin.Mac and Windows applications into a single shared codebase.

![Xamarin Forms Architecture](https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin-forms-images/xamarin-forms-architecture.png)<em class="sub-title center">What is Xamarin.Forms (source: [Microsoft](https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin-forms))</em>

Microsoft aims to create a unified .NET platform, replacing .NET Framework, .NET Core, and Xamarin. .NET MAUI is the next step in unifying .NET, replacing Xamarin.Forms. It addresses some of the issues and downsides of Xamarin.Forms while providing an updated architecture on top of the new generation of .NET and project system.

### What about my Xamarin.Forms skills and applications?

Think of .NET MAUI as a new version of Xamarin.Forms. Microsoft has assured us that our Xamarin.Forms skills are transferable.

> Xamarin.Forms developers will hit the ground running with new projects in .NET MAUI, using all the same controls and APIs they have grown to know and love. _[source](https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin-forms)_

There will also be tools and guidance to help migrate applications. The team expect to have a version of the .NET Upgrade Assistant that can migrate Xamarin and Xamarin.Forms projects to .NET 6 and .NET MAUI in the [July 2021 Preview 6 release](https://github.com/dotnet/maui/wiki/Roadmap#net-maui-in-net-6-preview-6-july-2021).

## What is different about MAUI?

If we already have Xamarin.Forms, what is so special about .NET MAUI? Microsoft is rebuilding the core of Xamarin.Forms, bringing us performance improvements, consistent design systems, and an extension from mobile to desktop.

Key Improvements in MAUI:

- Single project experience across platforms
- .NET Hot Reload
- Modern App Patterns

### Single Project Experience

.NET MAUI allows us to have a single project experience instead of one project for each target platform. A single project improves the developer experience by enabling developers to target and debug different devices without switching between projects or navigating the idiosyncrasies of each platform. We can use one language across our application to target all the supported platforms and easily share resources across while maintaining an option for platform-specific code.

### .NET Hot Reload

Hot reload increases productivity for .NET developers, allowing instant updates to running applications with new code changes. Removing the build and deploy interruptions saves time and allows the development flow to continue. In .NET, they are expanding Hot Reload, bringing complete support to .NET MAUI along with other workloads.

### Modern App Patterns

Model-View-ViewModel (MVVM) and XAML pattern, used in existing Xamarin.Forms applications, will continue to be supported and improved with the evolution. .NET MAUI will introduce further support for the Model-View-Update (MVU) development pattern, popular in C#, enabling developers to write fluent C# UI, creating a code-first development experience.

## What's new from Microsoft Build 2021?

During Microsoft Build 2021, Microsoft announced the availability of [.NET MAUI Preview 4](https://devblogs.microsoft.com/dotnet/announcing-net-maui-preview-4/). Each preview provides us with more features and tools with general availability scheduled for November 2021 at [.NET Conf](https://www.dotnetconf.net/).

With the release of Preview 4, you can now create functional applications across all supported platforms using .NET MAUI. In addition, they have added new capabilities to support running Blazor on desktop using .NET MAUI, allowing the reuse of Blazor UI components across native desktop and web applications.

![Weather Twenty One .NET MAUI Preview 4](https://github.com/davidortinau/WeatherTwentyOne/blob/main/images/maui-weather-hero-sm.png?raw=true)<em class="sub-title center">Weather Twenty One .NET MAUI Preview 4 Demo (source: [David Ortinau](https://github.com/davidortinau/WeatherTwentyOne))</em>

Alongside Preview 4 is the release of [Visual Studio 2019 version 16.11 Preview](https://visualstudio.microsoft.com/vs/preview/). The Visual Studio 2019 16.11 Preview enables .NET Hot Reload for MAUI and provides productivity features for developing .NET MAUI projects. A project template option for a .NET MAUI application is now available in the 16.11 Preview, encompassing the new solution format with the multi-targeted project.

To see what is coming in future releases, visit the MAUI [product roadmap](https://github.com/dotnet/maui/wiki/roadmap).

## How can you get started?

Before you get started, Microsoft has created a `dotnet tool` called `maui-check` that evaluates your system for development in .NET MAUI. The tool will scan for the required dependencies and try to fix any issues for you or suggest a way to fix them yourself.

Tool source: [https://github.com/Redth/dotnet-maui-check](https://github.com/Redth/dotnet-maui-check)

```bash
dotnet tool install -g Redth.Net.Maui.Check
maui-check
```

Once you have the complete .NET MAUI development environment setup, you can create your first app by running:

```bash
dotnet new maui -n AlohaMaui
```

Congratulations! You have a new .NET MAUI application.

---

## Resources

Check out the resources below to find out more about .NET MAUI and the exciting future in the .NET ecosystem. Mahalo!

- [https://github.com/dotnet/maui](https://github.com/dotnet/maui)
- [https://github.com/dotnet/maui/wiki/Getting-Started](https://github.com/dotnet/maui/wiki/Getting-Started)
- [https://devblogs.microsoft.com/dotnet/announcing-net-maui-preview-4/](https://devblogs.microsoft.com/dotnet/announcing-net-maui-preview-4/)
- [https://docs.microsoft.com/en-us/events/build-may-2021/azure/breakouts/od485/](https://docs.microsoft.com/en-us/events/build-may-2021/azure/breakouts/od485/)
- [https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin-forms](https://docs.microsoft.com/en-us/xamarin/get-started/what-is-xamarin-forms)
- [https://devblogs.microsoft.com/xamarin/the-new-net-multi-platform-app-ui-maui/](https://devblogs.microsoft.com/xamarin/the-new-net-multi-platform-app-ui-maui/)
- [https://channel9.msdn.com/Events/Build/2020/BOD107](https://channel9.msdn.com/Events/Build/2020/BOD107?ocid=AID3012654&WT.mc_id=build2020-azuredevtips-micrum)
- [https://channel9.msdn.com/Events/Build/2020/BOD106](https://channel9.msdn.com/Events/Build/2020/BOD106)
- [https://channel9.msdn.com/Shows/On-NET/A-Journey-to-NET-MAUI](https://channel9.msdn.com/Shows/On-NET/A-Journey-to-NET-MAUI)
