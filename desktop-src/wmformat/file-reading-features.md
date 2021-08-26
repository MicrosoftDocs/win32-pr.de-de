---
title: Funktionen zum Lesen von Dateien
description: Funktionen zum Lesen von Dateien
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Medienformat-SDK, Features zum Lesen von Dateien
- Windows Medienformat-SDK, asynchrones Lesen von Dateien
- Windows Medienformat-SDK, synchrones Lesen von Dateien
- Advanced Systems Format (ASF), Features zum Lesen von Dateien
- ASF (Advanced Systems Format), Features zum Lesen von Dateien
- Advanced Systems Format (ASF), asynchrones Lesen von Dateien
- ASF (Advanced Systems Format), asynchrones Lesen von Dateien
- Advanced Systems Format (ASF), synchrones Lesen von Dateien
- ASF (Advanced Systems Format), synchrones Lesen von Dateien
- asynchrones Lesen von Dateien
- Synchrones Lesen von Dateien
- synchrone Reader, Features zum Lesen von Dateien
- Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8efb7bc0fca898c1a63db586b158b39b4bb9daa9ad051e7a61fe8c4a5d6b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930530"
---
# <a name="file-reading-features"></a>Funktionen zum Lesen von Dateien

Das Lesen von ASF-Dateien ist eines der hauptfeatures des Windows Media Format SDK. Zwei Lesetypen werden unterstützt: asynchron und synchron. Das asynchrone Lesen von Dateien wird vom Readerobjekt verarbeitet. Das synchrone Readerobjekt wird verwendet, um Dateien synchron zu lesen. Weitere Informationen zu den verschiedenen Leseobjekten finden Sie unter [Reader-Objekt](reader-object.md) und [synchrones Readerobjekt.](synchronous-reader-object.md)

Im einfachsten asynchronen Dateileseszenario müssen Sie eine Rückrufmethode implementieren, die das Readerobjekt aufruft, wenn Die Beispiele bereit sind. Nachdem Sie mit dem Lesen einer Datei begonnen haben, wartet Ihre Anwendung, bis die Beispiele an Ihre Rückrufmethode übermittelt werden. Asynchrones Lesen ist für Playeranwendungen nützlich und unterstützt Features, die beim synchronen Lesen nicht verfügbar sind. Wenn Ihre Anwendung Dateien von einem Netzwerkspeicherort lesen oder mit einem Server interagieren muss, auf dem Windows Media-Dienste ausgeführt wird, müssen Sie das Readerobjekt verwenden. Der Nachteil des Readerobjekts besteht darin, dass für jede übermittelte Ausgabe ein separater Thread verwendet wird. Darüber hinaus ist das Readerobjekt nicht so flexibel wie der synchrone Reader in bezug auf die Bereitstellung von Beispielen.

Mit dem synchronen Reader müssen Sie keine Rückrufmethoden verwenden. Stattdessen wählen Sie einen Teil der Datei aus, um die Beispiele einzeln mit Methodenaufrufen zu lesen und abzurufen. Der synchrone Reader eignet sich gut für die Anforderungen von Inhaltsbearbeitungsanwendungen, bei denen der schnelle Zugriff auf bestimmte Beispiele unerlässlich ist. Da vom synchronen Reader keine Rückrufmethoden verwendet werden, können Sie Anwendungen erstellen, um ASF-Dateien mit minimalem Codierungsaufwand zu lesen. Der synchrone Reader kann jedoch keine Datei von einem Netzwerkspeicherort öffnen, mit einem Server interagieren, auf dem Windows Media-Dienste ausgeführt wird, oder Dateien lesen, die mit [*DRM*](wmformat-glossary.md)geschützt sind.

In den folgenden Themen werden die Features des Readers und des synchronen Readers behandelt.



| Thema                                                              | Beschreibung                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Vom Benutzer zugewiesene Beispielunterstützung](user-allocated-sample-support.md) | Erläutert die Pufferzuordnung im Reader und synchronen Reader und erläutert, wie die Benutzerzuordnung die Leistung verbessern kann. |
| [Ausgabeformatenumeration](output-format-enumeration.md)         | Erläutert die Ausgabeformatenumeration.                                                                               |



 

Darüber hinaus gelten die folgenden Themen aus dem Abschnitt mit den Schreibfeatures auch für das Lesen von Dateien:

-   [Ändern der Größe von Videos](video-resizing.md)
-   [Farbraumkonvertierung](color-space-conversion.md)
-   [Audio-Resampling](audio-resampling.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Features**](features.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




