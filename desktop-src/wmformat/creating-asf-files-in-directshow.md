---
title: Erstellen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)
description: Erstellen von ASF-Dateien in DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media-Format-SDK, Erstellen von ASF-Dateien in DirectShow
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), erstellen in DirectShow
- ASF (Advanced Systems Format), erstellen in DirectShow
- DirectShow, Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102663"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Erstellen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)

Mithilfe von DirectShow können Sie ASF-Dateien direkt aus Erfassungs Quellen, wie z. b. DV-Camcordern, erstellen oder andere Dateien in das Windows Media-Format transcodieren. In beiden Szenarien erstellen Anwendungen Filter Diagramme, die den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter als Renderer enthalten.

Der WM-ASF-Writer stellt einen partiellen Wrapper für das Windows Media-Format-SDK bereit. Anwendungen können die [**iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) -Schnittstelle des Filters verwenden, um ein Systemprofil (Version 4, 7 oder 8) zu übergeben, oder das Windows Media-Format-SDK direkt verwenden, um ein benutzerdefiniertes Profil zu erstellen, das an den Filter übergeben werden soll. Zum Hinzufügen von Metadaten und anderen Header Informationen verwendet die Anwendung die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle, die aus dem Filter abgerufen werden kann. Nachdem das Profil und die Metadaten konfiguriert wurden, kann die Anwendung einfach das Filter Diagramm ausführen. Intern verwendet der Filter das SDK für den Windows Media-Format, um die Datei zu schreiben. Der Filter behandelt alle Details der audiovideosynchronisierung, die andernfalls für die Anwendung verantwortlich sind.

Dieser Prozess wird in den folgenden Abschnitten ausführlicher erläutert.



| `Section`                                                                                                           | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Konfigurieren von WM ASF Writer (qasf)](configuring-the-wm-asf-writer--qasf.md)                                   | Beschreibt, wie der WM-ASF-Writer-Filter konfiguriert wird.                                   |
| [Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)](building-filter-graphs-to-write-asf-files--qasf.md)           | Hier wird beschrieben, wie Datei-und Erfassungs Diagramme erstellt werden.                           |
| [Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)](configuring-profiles-and-other-file-properties--qasf.md) | Hier wird beschrieben, wie verschiedene Aufgaben zur Konfiguration von ASF-Dateien mit dem WM-ASF-Writer ausgeführt werden. |



 

 

 
