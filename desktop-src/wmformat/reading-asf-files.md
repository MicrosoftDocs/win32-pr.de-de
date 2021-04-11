---
title: Lesen von ASF-Dateien
description: Lesen von ASF-Dateien
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media-Format-SDK, Lesen von ASF-Dateien
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311008"
---
# <a name="reading-asf-files"></a>Lesen von ASF-Dateien

Das SDK für den Windows Media-Format kann verwendet werden, um Medien Beispiele aus einer ASF-Datei bereitzustellen. Zum Abrufen von Beispielen werden zwei-Objekte verwendet: das Reader-Objekt und das synchrone Reader-Objekt.

Das Reader-Objekt ist das ursprüngliche Lese Objekt im Windows Media-Format-SDK. Das Reader-Objekt verwendet eine asynchrone Architektur, um Beispiele per Push an eine Anwendung zu übersetzen. Anwendungen, die mithilfe des Reader-Objekts erstellt wurden, müssen Rückruf Funktionen implementieren, die auf die verschiedenen Nachrichten und Ereignisse reagieren, die sich aus diesem multithreadmodell ergeben. Aus Gründen der Übersichtlichkeit wird in diesem Abschnitt auf das Reader-Objekt als asynchroner Reader verwiesen.

Das synchrone Reader-Objekt ist neu in dieser Version des Windows Media-Format-SDKs. Der synchrone Reader verwendet bei der Verarbeitung von Beispielen aus den ASF-Dateien nicht mehrere Threads. Eine Anwendung, die mithilfe des synchronen Readers erstellt wurde, ruft nach Bedarf Beispiele ab, anstatt darauf zu warten, dass der Reader Sie sendet.

Wenn Sie eine Anwendung zum Lesen von ASF-Dateien erstellen, müssen Sie das zu verwendende Reader-Objekt auswählen. Im Allgemeinen sollten Anwendungen, die für die Bereitstellung von Windows Media-basierten Inhalten entworfen wurden, mithilfe des asynchronen Readers erstellt werden, während Anwendungen, die zum Bearbeiten von ASF-Dateien entworfen wurden, mit dem synchronen Reader erstellt werden.

In der folgenden Tabelle werden die Hauptfunktionen der beiden Reader-Objekte aufgelistet. Verwenden Sie diese Tabelle, um zu bestimmen, welches Objekt für die Anwendung verwendet werden soll.



| Funktion                                                                    | Async-Reader | Synchronisierungs Leser |
|----------------------------------------------------------------------------|--------------|-------------|
| Nicht komprimierte Beispiele nach Ausgabe Nummer lesen                                 | Ja          | Ja         |
| Komprimierte Beispiele nach streamnummer lesen                                   | Ja          | Ja         |
| Nicht komprimierte Beispiele nach streamnummer lesen                                 | Nein           | Ja         |
| Aus Internet Website lesen                                                    | Ja          | Nein          |
| Lesen von Metadaten                                                              | Ja          | Ja         |
| Präsentationszeit suchen                                                  | Ja          | Ja         |
| Nach Frame suchen                                                              | Ja          | Ja         |
| Nach Marker suchen                                                             | Ja          | Nein          |
| Wechsel zwischen komprimierter und unkomprimierter Beispiel Übermittlung während der Wiedergabe | Nein           | Ja         |
| Öffnen von Dateien mithilfe der **IStream** -Schnittstelle                                     | Ja          | Ja         |



 

In den folgenden Abschnitten finden Sie weitere Informationen zum Arbeiten mit den beiden Reader-Objekten.



| `Section`                                                                                      | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Arbeiten mit Ausgaben](working-with-outputs.md)                                             | Beschreibt, wie Ausgaben verwendet und bearbeitet werden. Gilt für beide Reader-Objekte.                                                            |
| [Puffer für Datei Lesevorgänge werden zugewiesen.](allocating-buffers-for-file-reading.md)               | Beschreibt, wie Sie Ihren eigenen Pufferpool zum Speichern von Beispielen verwenden, die vom Reader oder dem synchronen Reader bereitgestellt werden.                            |
| [Lesen von Metadaten bei der Wiedergabe](reading-metadata-at-playback.md)                             | Beschreibt, wie Sie die Metadatenunterstützung bei der Wiedergabe nutzen können. Gilt für beide Reader-Objekte.                                        |
| [Erhalten von Profilinformationen bei der Wiedergabe](getting-profile-information-at-playback.md)       | Beschreibt, wie auf Profilinformationen für geöffnete Dateien zugegriffen wird. Gilt für beide Reader-Objekte.                                           |
| [Lesen von Multichannel-Audiodateien](reading-multichannel-audio.md)                                 | Beschreibt, wie der Writer zum ordnungsgemäßen Decodieren von Multichannel-Audiodaten konfiguriert wird.                                                            |
| [Rendern von Inhalten](rendering-content.md)                                                   | Erläutert die Probleme im Zusammenhang mit dem Rendern nicht komprimierter Beispiele. Gilt für beide Reader-Objekte.                                         |
| [Erzielen Sie das beste Video für die Suche nach Leistung](getting-the-best-video-seeking-performance.md) | Beschreibt Möglichkeiten zum Verbessern der Video Suchleistung.                                                                                    |
| [Lesen von Dateien mit dem asynchronen Reader](reading-files-with-the-asynchronous-reader.md) | Beschreibt das Lesen von ASF-Dateien mithilfe des asynchronen Reader-Objekts.                                                                   |
| [Lesen von Dateien mit dem synchronen Reader](reading-files-with-the-synchronous-reader.md)   | Beschreibt das Lesen von ASF-Dateien mit dem synchronen Reader-Objekt.                                                                    |
| [Aktivieren der DirectX-Video Beschleunigung](enabling-directx-video-acceleration.md)               | Beschreibt, wie eine DirectX-Videobeschleunigung implementiert wird, um die Hardware Beschleunigungs Features einiger Grafikkarten für das Decodieren von Videos zu verwenden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




