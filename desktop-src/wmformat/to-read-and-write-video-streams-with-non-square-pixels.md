---
title: So lesen und schreiben Sie Streams mit nicht quadratischen Pixeln
description: So lesen und schreiben Sie Streams mit nicht quadratischen Pixeln
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows Medienformat-SDK, Lesen von Videostreams
- Windows Medienformat-SDK, Schreiben von Videostreams
- Windows Medienformat-SDK, Videostreams
- Windows Medienformat-SDK, nicht quadratische Pixel
- Windows Medienformat-SDK, Pixel (nicht quadratisch)
- Advanced Systems Format (ASF), Lesen von Videostreams
- ASF (Advanced Systems Format), Lesen von Videostreams
- Advanced Systems Format (ASF), Schreiben von Videostreams
- ASF (Advanced Systems Format), Schreiben von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht quadratische Pixel
- Advanced Systems Format (ASF), Pixel (nicht quadratisch)
- ASF (Advanced Systems Format), Pixel (nicht quadratisch)
- Lesen von Videostreams
- Schreiben von Videostreams
- Videostreams,Lesen
- Videostreams,Schreiben
- Videostreams, nicht quadratische Pixel
- Nicht-Quadratpixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdcd5ef5292cc06c78b10916177c48db04547dfcbda4505cfeec93951a054cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699334"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a>So lesen und schreiben Sie Streams mit nicht quadratischen Pixeln

Computermonitore haben quadratische Pixel, aber andere Arten von Videobildschirmen, einschließlich NTSC-Fernsehsendungen, haben rechteckige oder nicht quadratische Pixel. Darüber hinaus haben einige Eingabegeräte, z. B. DV-Kameras (Digital Video), gerätespezifische Geräte mit nicht quadratischen Pixeln in Rechnung gestellt. Wenn Sie Dateien schreiben, die entweder auf Quelldaten ohne Quadratpixel basieren oder für die Anzeige auf Geräten mit nicht quadratischen Pixeln vorgesehen sind, müssen die Informationen zum Pixel-Seitenverhältnis in die ASF-Datei aufgenommen werden. Leseranwendungen müssen diese Informationen untersuchen und verwenden, um das Seitenverhältnis des Videorechtecks nach Bedarf anzupassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Weiterführende Themen**](advanced-topics.md)
</dt> <dt>

[**Lesen Streams mit nicht quadratischen Pixeln**](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[**Schreiben Streams mit nicht quadratischen Pixeln**](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




