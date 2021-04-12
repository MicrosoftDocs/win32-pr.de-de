---
title: Bildstreams
description: Bildstreams
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media-Format-SDK, bildstreams
- Advanced Systems Format (ASF), bildstreams
- ASF (Advanced Systems Format), bildstreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- bildstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310844"
---
# <a name="image-streams"></a>Bildstreams

Ein Bildstream ist ein spezieller Typ von Datenstrom, der weiterhin Bilder enthält, die Präsentations Zeiten zugewiesen sind. Eine Anwendung kann die Bilder wie gewünscht in einem Bildstream anzeigen, aber die typische Implementierung besteht darin, jedes Bild anzuzeigen, bis das nächste Bild übermittelt wird, wie z. b. eine Folien Anzeige. In der Regel wird ein Bildstream in einer Datei mit einem Audiostream codiert, um eine einfache Präsentation von Bildern zu schaffen, die mit Musik oder Sprache synchronisiert werden.

Bildstreams ähneln den Videostreams darin, dass Sie aus nicht komprimierten Beispielen erstellt werden, die im Rahmen des Datei Schreibvorgangs komprimiert werden, aber Sie sind auch beliebige Streams, da Sie dem Inhalt eine Bitrate und ein Puffer Fenster zuweisen müssen, ohne dass die vom Codec zugewiesenen Eigenschaften abhängig sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Audiodaten und Videostreams**](audio-and-video-streams.md)
</dt> <dt>

[**Schreiben von bildstreams**](writing-image-streams.md)
</dt> </dl>

 

 




