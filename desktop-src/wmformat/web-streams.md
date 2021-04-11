---
title: Webstreams
description: Webstreams
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media-Format-SDK, Webstreams
- Advanced Systems Format (ASF), Webstreams
- ASF (Advanced Systems Format), Webstreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Webstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036891"
---
# <a name="web-streams"></a>Webstreams

Ein Webstream ist wie ein Dateistream, in dem er Datendateien enthält. In einem Webstream sind diese Dateien in der Regel HTML-Seiten und zugehörige Grafiken im GIF-oder JPEG-Format.

Webstreams können besonders nützlich für ASF-Dateien sein, die als Präsentationen verwendet werden. Vor der Unterstützung von Webstreams hätten Präsentationen URLs in Skript Datenströmen innerhalb einer Datei, damit eine Webseite zu einem vordefinierten Zeitpunkt geladen wird. Die Schwierigkeit bestand darin, dass die Netzwerk Überlastung Verzögerungen verursachen könnte und eine schlechte Anzeige der Anzeige Leistung zur Folge hat.

Bei Webstreams können die Bestandteile von Webseiten in der ASF-Datei als Datenstrom enthalten sein. Wenn die Dateien empfangen werden, können Sie zwischengespeichert werden, sodass, wenn der Befehl zum Anzeigen (oder Rendering) einer URL zugestellt wird, sofort ein Browser darauf zugreifen kann. Dies ermöglicht eine reibungslose, konsistente Wiedergabe. Der Rendering-Befehl wird im Webstream selbst übermittelt, nicht als Skript Befehl in einem separaten Datenstrom.

Es wird empfohlen, dass Webstreams, die mithilfe des SDK der Windows Media-Serie 9 oder höher erstellt wurden, die Versionsnummer 1 erhalten. Dieser Wert wird in der [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Struktur im **wversion** -Member angegeben. Das SDK selbst führt keine Aktion aus, um diese Version zu erzwingen.

> [!Note]  
> Beim Herstellen einer Verbindung mit Live Broadcast Datenströmen, die über Webstreams verfügen, kann der Benutzer möglicherweise einen Rendering-Befehl erhalten, bevor sich die angegebene Datei tatsächlich im lokalen Cache befindet. Wenn die Anwendung diese Bedingung nicht erfüllt, wird im Browser der Fehler "Seite nicht gefunden" angezeigt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Konfigurieren von Webstreams**](configuring-web-streams.md)
</dt> </dl>

 

 




