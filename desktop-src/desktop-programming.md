---
description: Beginnen Sie mit dem Erlernen der Grundlagen der Einführung von hervorragend Desktop-Apps in diesem Abschnitt.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Erste Schritte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343996"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Einstieg in Windows-Desktop-Apps, die die Win32-API verwenden

Die Win32-API (auch als Windows-API bezeichnet) ist die ursprüngliche Plattform für native C/C++-Windows-Anwendungen, die direkten Zugriff auf Windows und Hardware erfordern. Sie bietet eine erstklassige Entwicklungsumgebung ohne Abhängigkeit von einer verwalteten Laufzeitumgebung wie .net und WinRT (für UWP-Apps für Windows 10). Dadurch ist die Win32-API die Plattform der Wahl für Anwendungen, die das höchste Maß an Leistung und den direkten Zugriff auf die Systemhardware benötigen.

> [!NOTE]
> In dieser Dokumentation wird das Erstellen von Windows-Desktop-Apps mit der Win32-API behandelt. Die Win32-API ist eine von mehreren App-Plattformen, die Sie zum Erstellen von Windows-Desktop Anwendungen verwenden können. Weitere Informationen zu anderen APP-Plattformen finden [Sie unter Auswählen Ihrer Plattform](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Vorbereiten

Befolgen Sie diese Anweisungen, und beginnen Sie mit dem Erstellen von Desktop-Apps für Windows 10, die die Win32-API

1. Laden Sie Visual Studio 2019 herunter, oder aktualisieren Sie es. Wenn Sie Visual Studio 2019 noch nicht verwenden, können Sie Microsoft Visual Studio Community 2019 kostenlos installieren. Wenn Sie Visual Studio installieren, stellen Sie sicher, dass Sie die Option " **Desktop Entwicklung mit C++** " auswählen. Download Links finden Sie auf der Seite [Downloads](https://developer.microsoft.com/windows/downloads) .

    > [!NOTE]
    > Wenn Sie Visual Studio installieren, können Sie optional die Optionen für die **.net-Desktop Entwicklung** und **universelle Windows-Plattform Entwicklung** für den Zugriff auf andere Projekttypen und App-Plattformen für die Erstellung von Windows-Desktop-Apps auswählen.

2. Wenn Sie Ihre Desktop-app in einem [msix-Paket](/windows/msix/desktop/desktop-to-uwp-root) erstellen und die APP auf dem Entwicklungs Computer testen oder debuggen möchten, müssen Sie den [Entwicklermodus auf Ihrem Computer aktivieren](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> Skripts, die Sie zum Einrichten des Entwicklungs Computers und zum Installieren anderer Features oder Pakete verwenden können, finden Sie in [diesem GitHub-Projekt](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Erfahren Sie, wie Sie Desktop-Apps mithilfe der Win32-API erstellen.

Wenn Sie noch nicht mit der Verwendung der Win32-API für Desktop-Apps vertraut sind, helfen Ihnen die folgenden Tutorials und Artikel beim Einstieg.

| Thema        | BESCHREIBUNG      |
|---------------|-----------------|
| [Erstellen Ihrer ersten C++ Win32-App](LearnWin32/learn-to-program-for-windows.md)    | In diesem Tutorial erfahren Sie, wie Sie ein Windows-Programm mit Win32-und com-APIs in C++ schreiben.  |
| [Erstellen Ihrer ersten App mithilfe von DirectX](direct3dgetstarted/building-your-first-directx-app.md) | In diesem grundlegenden Tutorial erhalten Sie einen Einstieg in die Entwicklung von DirectX-apps.            |
| [Programmierhandbuch für 64-Bit-Windows](WinProg64/programming-guide-for-64-bit-windows.md)    | Beschreibt die Programmierung für 64-Bit-Versionen des Windows-Betriebssystems. |
| [Verwenden der Windows-Header](WinProg/using-the-windows-headers.md)     | Bietet einen Überblick über einige der Konventionen, die in den Windows-Header Dateien verwendet werden. |

Sie können auch die [Desktop-App-Beispiele](https://github.com/Microsoft/Windows-classic-samples)durchsuchen.

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernisieren ihrer Desktop-Apps für Windows 10

Wenn Sie über eine vorhandene Win32-Desktop-App verfügen, stehen Ihnen viele Features in der universelle Windows-Plattform (UWP) zur Verfügung, die Sie verwenden können, um die bestmögliche Benutzer Leistung für Windows 10 bereitzustellen. Beispielsweise können Sie ab Windows 10, Version 1903, UWP-XAML-Steuerelemente in Ihrer Desktop-Win32-App mithilfe eines Features namens XAML-Inseln hosten.

Die meisten dieser UWP-Funktionen sind als modulare Komponenten verfügbar, die Sie in Ihrer Desktop-app in Ihrem eigenen Tempo übernehmen können, ohne die gesamte Anwendung neu schreiben zu müssen. Sie können Ihre vorhandene Desktop-App verbessern, indem Sie auswählen, welche Teile von Windows 10 und UWP übernommen werden.

Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-Apps](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Optional können Sie den Entwicklungs Computer so konfigurieren, dass er [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/)verwendet. C++/WinRT ist eine vollständig standardmäßige moderne C++ 17-sprach Projektion und ermöglicht Ihnen die einfache Nutzung von Windows-Runtime APIs Windows-Runtime (WinRT)-APIs aus Ihrer C++ Win32-Desktop Anwendung. C++/WinRT wird als auf Header Dateien basierende Bibliothek implementiert.

Konfigurieren Ihres Projekts für C++/WinRT:

* Für neue Projekte können Sie die [C++/WinRT-Visual Studio-Erweiterung (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) installieren und eine der in dieser Erweiterung enthaltenen C++/WinRT-Projektvorlagen verwenden.
* Für vorhandene Windows-Desktop Anwendungsprojekte können Sie das nuget-Paket [Microsoft. Windows. cppwinrt](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) im Projekt installieren.

Weitere Informationen zu diesen Optionen finden Sie in [diesem Artikel](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Neuerungen bei Win32-APIs in Windows 10

Weitere Informationen zu neuen Win32-APIs, die in Windows 10 eingeführt wurden, finden Sie unter [What es New](whats-new.md)(Neuerungen).

## <a name="get-started-with-win32-features-and-technologies"></a>Beginnen Sie mit Win32-Features und-Technologien

Win32-APIs sind für viele Features und Technologien in Windows 10 vorhanden, einschließlich der Kern Benutzeroberfläche und der windowingapis, Audiofunktionen und Grafiken sowie von Netzwerkfunktionen. Anleitungen und Codebeispiele zur Verwendung dieser APIs finden Sie in [unserem Funktions-und Technologien Index](desktop-app-technologies.md).

## <a name="related-topics"></a>Zugehörige Themen

* [Entwickeln von Desktop-Apps](/windows/apps/desktop)
* [Windows-API-Referenz](/windows/desktop/api/)
* [Windows-API-Index](/windows/desktop/apiindex/api-index-portal)
* [Windows-Runtime C++ Verweis](/windows/desktop/winrt/reference)
