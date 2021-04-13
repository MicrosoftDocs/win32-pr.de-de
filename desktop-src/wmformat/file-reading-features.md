---
title: Funktionen zum Lesen von Dateien
description: Funktionen zum Lesen von Dateien
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media-Format-SDK, Datei Lesefunktionen
- Windows Media-Format-SDK, asynchrones Lesen von Dateien
- Windows Media-Format-SDK, synchrone Datei Lesevorgänge
- Advanced Systems Format (ASF), Datei Lesefunktionen
- ASF (Advanced Systems Format), Datei Lesefunktionen
- Advanced Systems Format (ASF), asynchrones Lesen von Dateien
- ASF (Advanced Systems Format), asynchrones Lesen von Dateien
- Advanced Systems Format (ASF), synchrones Lesen von Dateien
- ASF (Advanced Systems Format), synchrones Lesen von Dateien
- asynchrones Lesen von Dateien
- synchrone Datei Lesevorgänge
- synchrone Reader, Datei Lesefunktionen
- Datei Lesevorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311268"
---
# <a name="file-reading-features"></a>Funktionen zum Lesen von Dateien

Das Lesen von ASF-Dateien ist eines der wichtigsten Features des Windows Media-SDK. Zwei Lese Typen werden unterstützt: asynchron und synchron. Asynchrones Lesen von Dateien wird vom Reader-Objekt verarbeitet. Das synchrone Reader-Objekt wird verwendet, um Dateien synchron zu lesen. Weitere Informationen zu den unterschiedlichen Lese Objekten finden Sie unter [Reader-Objekt](reader-object.md) und [synchrones Reader-Objekt](synchronous-reader-object.md).

Im grundlegendsten asynchronen Datei Lese Szenario müssen Sie eine Rückruf Methode implementieren, die vom Reader-Objekt aufgerufen wird, wenn Beispiele bereit sind. Nachdem Sie mit dem Lesen einer Datei begonnen haben, wartet die Anwendung darauf, dass die Beispiele an Ihre Rückruf Methode übermittelt werden. Asynchrones Lesen ist für Player Anwendungen nützlich und unterstützt Funktionen, die mit synchronem lesen nicht verfügbar sind. Wenn Ihre Anwendung Dateien von einem Netzwerk Speicherort lesen oder mit einem Server interagieren muss, auf dem Windows Media Services ausgeführt wird, müssen Sie das Reader-Objekt verwenden. Der Nachteil des Reader-Objekts besteht darin, dass ein separater Thread für jede gelieferte Ausgabe verwendet wird. Außerdem ist das Reader-Objekt nicht so flexibel wie der synchrone Reader in der Möglichkeit, Beispiele zu liefern.

Mit dem synchronen Reader müssen keine Rückruf Methoden verwendet werden. Stattdessen wählen Sie einen Teil der Datei aus, um die Beispiele einzeln mit Methoden aufrufen zu lesen und abzurufen. Der synchrone Reader eignet sich gut für die Anforderungen von Anwendungen zur Inhalts Bearbeitung, bei denen der schnelle Zugriff auf bestimmte Beispiele unabdingbar ist. Da vom synchronen Reader keine Rückruf Methoden verwendet werden, können Sie Anwendungen zum Lesen von ASF-Dateien mit minimalem Codierungsaufwand erstellen. Der synchrone Reader kann jedoch keine Datei von einem Netzwerk Speicherort öffnen oder mit einem Server interagieren, auf dem Windows Media Services ausgeführt wird, oder Dateien lesen, die mit [*DRM*](wmformat-glossary.md)geschützt sind.

In den folgenden Themen werden die Funktionen des Readers und des synchronen Readers erläutert.



| Thema                                                              | BESCHREIBUNG                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Vom Benutzer zugewiesene Beispiel Unterstützung](user-allocated-sample-support.md) | Erläutert die Puffer Zuordnung im Reader und im synchronen Reader und wie die Benutzer Zuordnung die Leistung verbessern kann. |
| [Ausgabe Format-Enumeration](output-format-enumeration.md)         | Erläutert die Enumeration des Ausgabeformats.                                                                               |



 

Außerdem gelten die folgenden Themen aus dem Abschnitt Schreiben von Features auch für das Lesen von Dateien:

-   [Ändern der Größe von Videos](video-resizing.md)
-   [Farb Raum Konvertierung](color-space-conversion.md)
-   [Audioprobennahme](audio-resampling.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aspekte**](features.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




