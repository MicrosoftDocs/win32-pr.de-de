---
title: Beispiel für eine Desktop Anwendung
description: Beispiel für eine Desktop Anwendung
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- wmdmapp-Beispielanwendung
- Beispiele, Desktop Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388361"
---
# <a name="sample-desktop-application"></a>Beispiel für eine Desktop Anwendung

Der Windows Media Device Manager wird mit einer Beispiel-Desktop Anwendung namens wmdmapp ausgeliefert. Diese Anwendung verfügt über eine grafische Benutzeroberfläche, die Ihnen das Durchsuchen verbundener Geräte, das Erstellen von Wiedergabelisten auf dem Gerät und das Ziehen von Mediendateien auf das Gerät ermöglicht.

Diese Beispielanwendung besteht aus zwei Teilen:

-   wmdapp.exe, eine ausführbare Datei, die ein Fenster anzeigt und die meisten Benutzeroberflächen und grundlegenden Funktionen des Programms ausführt, und
-   proghelp.dll, eine Hilfs-DLL, die Hilfsprogrammfunktionen für die Anwendung ausführt. Sie müssen diese DLL nach der Projekt Erstellung registrieren.

Sie können Visual Studio verwenden, um die Beispielanwendung zu kompilieren. Im folgenden Abschnitt wird beschrieben, wie dies geschieht:

-   [Kompilieren der Beispielanwendung mit Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Nachdem Sie das Projekt kompiliert haben, registrieren Sie die proghelp.dll Datei. Um diese DLL zu registrieren, öffnen Sie eine Eingabeaufforderung, navigieren Sie zu dem Verzeichnis, das diese DLL enthält, und geben Sie ein `regsvr32 proghelp.dll` .

 

 




