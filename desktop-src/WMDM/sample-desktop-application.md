---
title: Beispieldesktopanwendung
description: Beispieldesktopanwendung
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Medien Geräte-Manager,Beispiele
- Geräte-Manager,Beispiele
- Desktopanwendungen,Beispiele
- Windows Beispiel für Geräte-Manager,Desktopanwendung
- Geräte-Manager,Desktopanwendungsbeispiel
- wmdmapp-Beispielanwendung
- Beispiele,Desktopanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e8037ccf963f26637711cd6d0e77ea7d2b4ff3cede72fcbded6600226d36c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584246"
---
# <a name="sample-desktop-application"></a>Beispieldesktopanwendung

Das Windows Media Geräte-Manager mit einer Beispieldesktopanwendung namens wmdmapp. Diese Anwendung verfügt über eine grafische Benutzeroberfläche, mit der Sie verbundene Geräte durchsuchen, Wiedergabelisten auf dem Gerät erstellen und Mediendateien auf das Gerät ziehen können.

Diese Beispielanwendung besteht aus zwei Teilen:

-   wmdapp.exe, eine ausführbare Datei, die ein Fenster anzeigt und den Großteil der Benutzeroberfläche und grundlegenden Funktionen des Programms ausführt, und
-   proghelp.dll, eine Hilfs-DLL, die Hilfsfunktionen für die Anwendung ausführt. Sie müssen diese DLL registrieren, nachdem Sie das Projekt erstellt haben.

Zum Kompilieren der Beispielanwendung können Sie Visual Studio. Im folgenden Abschnitt wird beschrieben, wie dies erfolgt:

-   [Kompilieren der Beispielanwendung mit Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Registrieren Sie nach dem Kompilieren des Projekts die proghelp.dll Datei. Öffnen Sie zum Registrieren dieser DLL eine Eingabeaufforderung, navigieren Sie zu dem Verzeichnis, das diese DLL enthält, und geben Sie `regsvr32 proghelp.dll` ein.

 

 




