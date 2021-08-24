---
description: Lernen Sie in diesem Abschnitt die Grundlagen der Entwicklung hervorragender Desktop-Apps.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Erste Schritte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f791589d73447798a7721c52164a2002b48a792959c698b835039293ce6004d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755010"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Erste Schritte mit Desktop-Windows-Apps, die die Win32-API verwenden

Die Win32-API (auch als Windows-API bezeichnet) ist die ursprüngliche Plattform für native C/C++-Windows-Anwendungen, die direkten Zugriff auf Windows und Hardware erfordern. Es bietet eine erstklassige Entwicklungsumgebung ohne Abhängigkeit von einer verwalteten Laufzeitumgebung wie .NET und WinRT (für UWP-Apps für Windows 10). Dadurch ist die Win32-API die Plattform der Wahl für Anwendungen, die das höchste Maß an Leistung und den direkten Zugriff auf die Systemhardware benötigen.

> [!NOTE]
> In dieser Dokumentation wird beschrieben, wie Sie Desktop-Windows-Apps mit der Win32-API erstellen. Die Win32-API ist eine von mehreren App-Plattformen, die Sie zum Erstellen von Desktop-Apps Windows können. Weitere Informationen zu anderen App-Plattformen finden Sie unter [Auswählen Ihrer Plattform.](/windows/apps/desktop/choose-your-platform)

## <a name="get-set-up"></a>Vorbereiten

Befolgen Sie diese Anweisungen, und beginnen Sie mit dem Erstellen von Desktop-Apps für Windows 10, die die Win32-API verwenden.

1. Laden Sie das Update Visual Studio 2019 herunter, oder aktualisieren Sie es. Wenn Sie Visual Studio 2019 noch nicht verwenden, können Sie Microsoft Visual Studio Community 2019 kostenlos installieren. Wenn Sie die Visual Studio installieren, stellen Sie sicher, dass Sie die **Option Desktopentwicklung mit C++** auswählen. Downloadlinks finden Sie auf unserer [Downloadseite.](https://developer.microsoft.com/windows/downloads)

    > [!NOTE]
    > Wenn Sie Visual Studio installieren, können Sie optional die **Entwicklungsoptionen .NET-Desktopentwicklung** und **Universelle Windows-Plattform** für den Zugriff auf andere Projekttypen und App-Plattformen zum Erstellen von Desktop- und Windows auswählen.

2. Wenn Sie Ihre Desktop-App in ein [MSIX-Paket](/windows/msix/desktop/desktop-to-uwp-root) erstellen und die gepackte App auf Ihrem Entwicklungscomputer testen oder debuggen möchten, müssen Sie den Entwicklermodus auf Ihrem [Computer aktivieren.](/windows/uwp/get-started/enable-your-device-for-development)

> [!NOTE]
> Informationen zu Skripts, mit derenHilfe Sie Ihren Entwicklungscomputer einrichten und andere Features oder Pakete installieren können, finden Sie [in GitHub Projekt](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Erfahren Sie, wie Sie Desktop-Apps mit der Win32-API erstellen.

Wenn Sie noch nicht mit dem Erstellen von Desktop-Apps mit der Win32-API beginnen, helfen Ihnen die folgenden Tutorials und Artikel beim Einstieg.

| Thema        | Beschreibung      |
|---------------|-----------------|
| [Erstellen Ihrer ersten C++-Win32-App](LearnWin32/learn-to-program-for-windows.md)    | In diesem Tutorial erfahren Sie, wie Sie ein Windows in C++ schreiben, indem Sie Win32- und COM-APIs verwenden.  |
| [Erstellen Ihrer ersten App mit DirectX](direct3dgetstarted/building-your-first-directx-app.md) | In diesem einfachen Tutorial erhalten Sie Informationen zu den ersten Schritte bei der Entwicklung von DirectX-Apps.            |
| [Programmierhandbuch für 64-Bit-Windows](WinProg64/programming-guide-for-64-bit-windows.md)    | Beschreibt die Programmierung für 64-Bit-Versionen des Windows Betriebssystems. |
| [Verwenden der Windows Header](WinProg/using-the-windows-headers.md)     | Bietet eine Übersicht über einige der Konventionen, die in den Headerdateien Windows werden. |

Sie können auch die [Desktop-App-Beispiele durchsuchen.](https://github.com/Microsoft/Windows-classic-samples)

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernisieren Ihrer Desktop-Apps für Windows 10

Wenn Sie über eine vorhandene Desktop-Win32-App verfügen, gibt es viele Features in der universellen Windows-Plattform (UWP), mit denen Sie die bestmögliche Benutzererfahrung auf der Windows 10. Beispielsweise können Sie ab Windows 10 Version 1903 UWP-XAML-Steuerelemente in Ihrer Win32-Desktop-App hosten, indem Sie ein Feature namens XAML Islands verwenden.

Die meisten dieser UWP-Features sind als modulare Komponenten verfügbar, die Sie in Ihrer Desktop-App in Ihrem eigenen Tempo übernehmen können, ohne die gesamte Anwendung neu schreiben zu müssen. Sie können Ihre vorhandene Desktop-App verbessern, indem Sie auswählen, welche Teile Windows 10 und UWP übernehmen.

Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-Apps](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Optional können Sie Ihren Entwicklungscomputer für die Verwendung von [C++/WinRT konfigurieren.](/windows/uwp/cpp-and-winrt-apis/) C++/WinRT ist eine vollständig standardmäßige moderne C++17-Sprachprojektion, mit der Sie ganz einfach Windows-Runtime-APIs Windows Runtime-APIs (WinRT)-APIs aus Ihrer C++-Win32-Desktopanwendung nutzen können. C++/WinRT wird als headerdateibasierte Bibliothek implementiert.

Konfigurieren Ihres Projekts für C++/WinRT:

* Für neue Projekte können Sie die [C++/WinRT-Visual Studio-Erweiterung (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) installieren und eine der in dieser Erweiterung enthaltenen C++/WinRT-Projektvorlagen verwenden.
* Für vorhandene Windows Desktopanwendungsprojekte können Sie [Microsoft.Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) NuGet Paket im Projekt.

Weitere Informationen zu diesen Optionen finden Sie in [diesem Artikel](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Neues bei Win32-APIs in Windows 10

Informationen zu neuen Win32-APIs, die in Windows 10 wurden, finden Sie unter [Neues.](whats-new.md)

## <a name="get-started-with-win32-features-and-technologies"></a>Erste Schritte mit Win32-Features und -Technologien

Win32-APIs stehen für viele Features und Technologien in Windows 10 zur Verfügung, einschließlich Kern-Benutzeroberflächen- und Fenster-APIs, Audio- und Grafik- und Netzwerkfunktionen. Anleitungen und Codebeispiele zur Verwendung dieser APIs finden Sie [in unserem Index für Features und Technologien.](desktop-app-technologies.md)

## <a name="related-topics"></a>Zugehörige Themen

* [Entwickeln von Desktop-Apps](/windows/apps/desktop)
* [Windows API-Referenz](/windows/desktop/api/)
* [Windows-API-Index](/windows/desktop/apiindex/api-index-portal)
* [Windows C++-Referenz zur Laufzeit](/windows/desktop/winrt/reference)
