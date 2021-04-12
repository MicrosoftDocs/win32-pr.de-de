---
description: Anforderungen für Decoders
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Anforderungen für Decoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481451"
---
# <a name="requirements-for-decoders"></a>Anforderungen für Decoders

Decoderer, die Beispiele für den VMR bereitstellen, müssen die folgenden Regeln beachten:

-   Für jeden Videoframe sollte ein Teil Bild Rahmen an den VMR übermittelt werden. Die beiden Frames sollten die gleichen Zeitstempel aufweisen.
-   Wenn das Teilbild nicht geändert wurde, verwenden Sie das am \_ GBF \_ notasyncpoint-Flag in der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode, um zu erzwingen, dass die Zuweisung einen Puffer mit dem letzten Frame zurückgibt, der an die VMR übermittelt wurde. Legen Sie einfach einen neuen Zeitstempel für das Beispiel fest, und übermitteln Sie ihn erneut an den VMR. Wenn das Bild des unter Bilds leer ist, sollten Sie es trotzdem übermitteln. VMR erkennt den leeren Frame und nicht mit dem Video. Dieser Test wird vom VGA-Chip durchgeführt und wirkt sich nicht auf die Wiedergabe Leistung aus.
-   Allen Beispielen, mit Ausnahme von Livestreams, müssen gültige Start-und Endzeit Stempel angefügt werden. (Die DVD ist kein Livestream.)
-   Die Zeitstempel für das Medien Beispiel müssen zusammenhängend sein.
-   Der Decoder muss sich selbst als VMR-fähig für die Verwendung durch Graph-Generatoren identifizieren.
-   Der unterbildstream sollte nun eingebettete Alpha Werte pro Pixel enthalten. Der ARGB4444-Oberflächen Typ ist ideal für unter Bilder.
-   Gehen Sie nicht davon aus, dass der Stride-Wert des Teil Bilds mit der Oberflächen Breite identisch ist. Dies ist bei VMR nicht immer der Fall.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur DirectX-Video Beschleunigung](about-directx-video-acceleration.md)
</dt> </dl>

 

 



