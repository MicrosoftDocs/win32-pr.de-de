---
title: Image Streams
description: Image Streams
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Medienformat-SDK, Bildstreams
- Advanced Systems Format (ASF), Imagestreams
- ASF (Advanced Systems Format), Imagestreams
- Windows Medienformat-SDK,Streams
- Advanced Systems Format (ASF),streams
- ASF (Advanced Systems Format), Streams
- Imagestreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702864"
---
# <a name="image-streams"></a>Image Streams

Ein Bildstream ist ein spezieller Streamtyp, der noch Bilder enthält, die Präsentationszeiten zugewiesen sind. Eine Anwendung kann die Bilder wie gewünscht in einem Bildstream anzeigen, aber die typische Implementierung besteht in der Anzeige jedes Bilds, bis das nächste Bild übermittelt wird, z. B. eine Diashow. In der Regel wird ein Bildstream in einer Datei mit einem Audiostream codiert, um eine einfache Darstellung von Bildern zu erzeugen, die mit Musik oder Sprache synchronisiert werden.

Bildstreams sind wie Videostreams, da sie aus unkomprimierten Beispielen erstellt werden, die im Rahmen des Dateischreibenprozesses komprimiert werden. Sie sind jedoch auch wie beliebige Streams, da Sie dem Inhalt eine Bitrate und ein Pufferfenster zuweisen müssen, ohne codec-zugewiesene Eigenschaften zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Audio- und Streams**](audio-and-video-streams.md)
</dt> <dt>

[**Schreiben von Streams**](writing-image-streams.md)
</dt> </dl>

 

 




