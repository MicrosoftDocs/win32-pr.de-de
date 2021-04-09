---
title: Kompilieren der Beispielanwendung mit Visual Studio
description: Kompilieren der Beispielanwendung mit Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- Beispiele, Desktop Anwendungen
- Beispiele, Kompilieren mithilfe von Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036732"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Kompilieren der Beispielanwendung mit Visual Studio

Das Windows Media Device Manager SDK enthält eine Visual Studio-Projekt Mappe, die mit Microsoft Visual Studio 2005 kompatibel ist.

Bevor Sie die Beispielanwendung kompilieren, müssen Sie die Header Datei "shtypes. h" umbenennen, um Konflikte mit einer Datei mit demselben Namen zu vermeiden, die im Microsoft Platform SDK zu finden ist. Beispielsweise können Sie <SDK- *Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes. h in <*SDK-Installationspfad* > \\ WMFSDK11 \\ include \\ shtypes. h. Backup umbenennen.

Um die Anwendung zu erstellen, starten Sie eine Instanz von Visual Studio 2005, öffnen Sie die Projektmappendatei "wmdmapp. sln", die sich im Ordner <*SDK-Installationspfad* > \\ WMFSDK11 \\ apps \\ wmdmapp befindet, und wählen Sie die Option **Build/Build Solution** aus. Dadurch werden zwei Projektdateien erstellt: das Hilfsprojekt, proghelp. vcproj, und die Hauptanwendung wmdmapp. vcproj. Außerdem werden die Status-hilfsdll und die Hauptanwendung (WMDMApp.exe) erstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für eine Desktop Anwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




