---
title: Erstellen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über das Erstellen von ASF-Dateien in DirectShow mit dem Windows Media Format 11 SDK. ASF ist ein Containerformat, das beliebige Datentypen enthalten kann.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, Erstellen von ASF-Dateien in DirectShow
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), erstellen in DirectShow
- ASF (Advanced Systems Format), erstellen in DirectShow
- DirectShow,Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406183"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Erstellen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)

Sie können DirectShow verwenden, um ASF-Dateien direkt aus Erfassungsquellen wie DV-Datenträgern zu erstellen oder andere Dateien in das Windows-Medienformat zu transcodieren. In beiden Szenarien erstellen Anwendungen Filterdiagramme, die den [WM ASF Writer-Filter](wm-asf-writer-filter.md) als Renderer enthalten.

Wm ASF Writer stellt einen Teilwrapper für das Windows Media Format SDK bereit. Anwendungen können die [**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) des Filters verwenden, um ein Systemprofil (Versionen 4, 7 oder 8) zu übergeben, oder das Windows Media Format SDK direkt verwenden, um ein benutzerdefiniertes Profil zu erstellen, das an den Filter übergeben wird. Um Metadaten und andere Headerinformationen hinzuzufügen, verwendet die Anwendung die [**IWMHeaderInfo-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) die aus dem Filter abgerufen werden kann. Nachdem das Profil und die Metadaten konfiguriert wurden, kann die Anwendung einfach das Filterdiagramm ausführen. Intern verwendet der Filter das Windows Media Format SDK, um die Datei zu schreiben. Der Filter verarbeitet alle Details zur Synchronisierung von Audiovideos, die andernfalls in der Verantwortung der Anwendung stehen würden.

Dieser Prozess wird in den folgenden Abschnitten ausführlicher erläutert.



| `Section`                                                                                                           | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Konfigurieren des WM ASF Writer (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Beschreibt, wie der WM ASF Writer-Filter konfiguriert wird.                                   |
| [Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Beschreibt das Erstellen von Dateitranscodierung und Erfassen von Diagrammen.                           |
| [Konfigurieren von Profilen und anderen Dateieigenschaften (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Beschreibt, wie verschiedene ASF-Dateikonfigurationsaufgaben mit dem WM ASF Writer ausgeführt werden. |



 

 

 
