---
title: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)
description: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media-Format-SDK, Bausteine von Filter Diagrammen (qasf)
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Schreiben von ASF-Dateien (qasf)
- Advanced Systems Format (ASF), Bausteine von Filter Diagrammen (qasf)
- ASF (Advanced Systems Format), Bausteine von Filter Diagrammen (qasf)
- Advanced Systems Format (ASF), schreiben (qasf)
- ASF (Advanced Systems Format), schreiben (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Bausteine von Filter Diagrammen (qasf)
- DirectShow, Schreiben von ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337962"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)

Anwendungen, die auf DirectShow basieren, verwenden in der Regel einen von drei grundlegenden Arten von Filter Diagrammen, wenn Sie Windows Media – basierten Inhalt erstellen:

-   Filtern Sie Diagramme zum Umwandeln oder transcodieren von Inhalten aus einem anderen Format in das Windows Media-Format.
-   Filtern Sie Diagramme für das Einfügen von Inhalten, die nicht auf Windows-Medien basierende (Native Streamformate) sind, in ASF-Dateien.
-   Filtern Sie Diagramme, um Livedaten zu erfassen und direkt in das Windows Media-Format zu codieren, bevor Sie Sie auf einem Datenträger

Jeder Filter Diagrammtyp wird in den folgenden Abschnitten ausführlicher beschrieben.



| `Section`                                                                                                             | BESCHREIBUNG                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcoding-Dateien (qasf)](transcoding-files--qasf.md)                                                             | Beschreibt, wie Datei-transcodierungsfilterdiagramme erstellt werden.                                               |
| [Einfügen von nativen streamformaten in ASF-Dateien (qasf)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Beschreibt, wie jeder Typ von komprimierten oder nicht komprimierten Audiodaten oder Videodaten in eine ASF-Datei platziert wird. |
| [Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Beschreibt das Erstellen von Erfassungs Filter Diagrammen, die an eine ASF-Datei ausgegeben werden.                             |



 

 

 




