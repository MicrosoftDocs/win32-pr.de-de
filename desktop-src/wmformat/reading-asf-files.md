---
title: Lesen von ASF-Dateien
description: Lesen von ASF-Dateien
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Medienformat-SDK, Lesen von ASF-Dateien
- Windows Medienformat-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01f417cafad4e125c6c176ac35e95ff3ab8f08c4f600b811865a9fb6ae51362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197518"
---
# <a name="reading-asf-files"></a>Lesen von ASF-Dateien

Das Windows Media Format SDK kann verwendet werden, um Medienbeispiele aus einer ASF-Datei zu übermitteln. Zum Abrufen von Beispielen werden zwei Objekte verwendet: das Readerobjekt und das synchrone Readerobjekt.

Das Readerobjekt ist das ursprüngliche Leseobjekt im Windows Media Format SDK. Das Readerobjekt verwendet eine asynchrone Architektur, um Beispiele per Push an eine Anwendung zu pushen. Anwendungen, die mithilfe des Readerobjekts erstellt wurden, müssen Rückruffunktionen implementieren, die auf die verschiedenen Nachrichten und Ereignisse reagieren, die sich aus diesem Multithreadmodell ergeben. Aus Gründen der Übersichtlichkeit bezieht sich dieser Abschnitt auf das Readerobjekt als asynchronen Reader.

Das synchrone Readerobjekt ist für diese Version des Windows Media Format SDK neu. Der synchrone Reader verwendet nicht mehrere Threads bei der Verarbeitung von Beispielen aus ASF-Dateien. Eine Anwendung, die mit dem synchronen Reader erstellt wurde, ruft Stichproben bei Bedarf ab, anstatt darauf zu warten, dass der Reader sie sendet.

Beim Erstellen einer Anwendung zum Lesen von ASF-Dateien müssen Sie das zu verwendende Readerobjekt auswählen. Im Allgemeinen sollten Anwendungen, die entwickelt wurden, um Windows medienbasierten Inhalt bereitzustellen, mit dem asynchronen Reader erstellt werden, während Anwendungen, die zum Bearbeiten von ASF-Dateien entwickelt wurden, mit dem synchronen Reader erstellt werden sollten.

In der folgenden Tabelle sind die Hauptfunktionen beider Readerobjekte aufgeführt. Verwenden Sie diese Tabelle, um zu bestimmen, welches Objekt für Ihre Anwendung verwendet werden soll.



| Feature                                                                    | Asynchroner Reader | Synchronisierungsleser |
|----------------------------------------------------------------------------|--------------|-------------|
| Unkomprimierte Beispiele nach Ausgabenummer lesen                                 | Ja          | Ja         |
| Lesen komprimierter Beispiele nach Streamnummer                                   | Ja          | Ja         |
| Unkomprimierte Beispiele nach Streamnummer lesen                                 | Nein           | Ja         |
| Lesen von Internetwebsites                                                    | Ja          | Nein          |
| Lesen von Metadaten                                                              | Ja          | Ja         |
| Suchen nach Präsentationszeit                                                  | Ja          | Ja         |
| Suchen nach Frame                                                              | Ja          | Ja         |
| Suchen nach Markern                                                             | Ja          | Nein          |
| Wechseln zwischen komprimierter und nicht komprimierter Beispielübermittlung während der Wiedergabe | Nein           | Ja         |
| Öffnen von Dateien über **die IStream-Schnittstelle**                                     | Ja          | Ja         |



 

Die folgenden Abschnitte enthalten weitere Informationen zum Arbeiten mit den beiden Readerobjekten.



| `Section`                                                                                      | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Arbeiten mit Ausgaben](working-with-outputs.md)                                             | Beschreibt, wie Ausgaben verwendet und bearbeitet werden. Gilt für beide Readerobjekte.                                                            |
| [Zuordnen von Puffern zum Lesen von Dateien](allocating-buffers-for-file-reading.md)               | Beschreibt, wie Sie Ihren eigenen Pufferpool verwenden, um vom Reader oder synchronen Reader bereitgestellte Beispiele zu speichern.                            |
| [Lesen von Metadaten bei der Wiedergabe](reading-metadata-at-playback.md)                             | Beschreibt, wie die Metadatenunterstützung bei der Wiedergabe genutzt wird. Gilt für beide Readerobjekte.                                        |
| [Abrufen von Profilinformationen bei der Wiedergabe](getting-profile-information-at-playback.md)       | Beschreibt, wie auf Profilinformationen für geöffnete Dateien zugegriffen wird. Gilt für beide Readerobjekte.                                           |
| [Lesen von Multichannelaudio](reading-multichannel-audio.md)                                 | Beschreibt, wie der Writer so konfiguriert wird, dass multichannel-Audio ordnungsgemäß decodiert wird.                                                            |
| [Rendern von Inhalten](rendering-content.md)                                                   | Erläutert die Probleme im Zusammenhang mit dem Rendern von unkomprimierten Beispielen. Gilt für beide Readerobjekte.                                         |
| [Abrufen der besten Videosucheleistung](getting-the-best-video-seeking-performance.md) | Beschreibt Möglichkeiten, die Leistung der Videosuche zu verbessern.                                                                                    |
| [Lesen von Dateien mit dem asynchronen Reader](reading-files-with-the-asynchronous-reader.md) | Beschreibt, wie ASF-Dateien mithilfe des asynchronen Readerobjekts gelesen werden.                                                                   |
| [Lesen von Dateien mit dem synchronen Reader](reading-files-with-the-synchronous-reader.md)   | Beschreibt, wie ASF-Dateien mithilfe des synchronen Readerobjekts gelesen werden.                                                                    |
| [Aktivieren der DirectX-Videobeschleunigung](enabling-directx-video-acceleration.md)               | Beschreibt, wie Die DirectX-Videobeschleunigung implementiert wird, um die Hardwarebeschleunigungsfeatures einiger Grafikkarten zum Decodieren von Videos zu verwenden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




