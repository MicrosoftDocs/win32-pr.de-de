---
title: Kompilieren der Beispielanwendung mit Visual Studio
description: Kompilieren der Beispielanwendung mit Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media Geräte-Manager, Beispiele
- Geräte-Manager, Beispiele
- Desktopanwendungen, Beispiele
- Windows Beispiel für Medien-Geräte-Manager,Desktopanwendung
- beispiel für Geräte-Manager,Desktopanwendung
- Beispiele,Desktopanwendungen
- Beispiele,Kompilieren mit Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8b32cd5931a88bc41b8eee7171b6ab4ab18b629a8108007d68094180efaa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586251"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Kompilieren der Beispielanwendung mit Visual Studio

Das Windows Media Geräte-Manager SDK enthält eine Visual Studio-Lösung, die mit Microsoft Visual Studio 2005 kompatibel ist.

Bevor Sie die Beispielanwendung kompilieren, müssen Sie die Headerdatei shtypes.h umbenennen, um Konflikte mit einer Datei mit dem gleichen Namen zu vermeiden, die sich im Microsoft Platform SDK befindet. Beispielsweise können Sie <*SDK-Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes.h in <*SDK-Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes.h.backup umbenennen.

Um die Anwendung zu erstellen, starten Sie eine Instanz von Visual Studio 2005, öffnen Sie die Projektmappendatei wmdmapp.sln, die sich im Ordner <*SDK-Installationspfad* > \\ WMFSDK11 \\ apps wmdmapp befindet, und wählen Sie die Option \\ **Projektmappe erstellen/erstellen** aus. Dadurch werden zwei Projektdateien erstellt: das Hilfsprojekt proghelp.vcproj sowie die Hauptanwendung wmdmapp.vcproj. Darüber hinaus werden die Statushilfs-DLL und die Hauptanwendung (WMDMApp.exe) erstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispieldesktopanwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




