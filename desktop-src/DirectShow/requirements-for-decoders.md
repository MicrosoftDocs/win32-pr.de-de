---
description: Anforderungen für Decoder
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Anforderungen für Decoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84d02926b4ce36cea9e4221589d52690edb8e256b2f0f4863fa19fff5dc033
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697030"
---
# <a name="requirements-for-decoders"></a>Anforderungen für Decoder

Decoder, die Beispiele an die VMR liefern, müssen die folgenden Regeln beachten:

-   Für jeden Videoframe sollte ein Unterbildrahmen an die VMR übermittelt werden. Die beiden Frames sollten die gleichen Zeitstempel haben.
-   Wenn sich das Unterbild nicht geändert hat, verwenden Sie das AM \_ GBF \_ NOTASYNCPOINT-Flag in der [**IMemAllocator::GetBuffer-Methode,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) um zu erzwingen, dass die Zuweisung einen Puffer zurück gibt, der den letzten an die VMR übermittelten Frame enthält. Legen Sie einfach einen neuen Zeitstempel in das Beispiel ein, und stellen Sie ihn erneut an die VMR. Wenn das Unterbild "Blank" ist, sollten Sie es trotzdem ausliefern. Die VMR erkennt den leeren Frame und kombiniert ihn nicht mit dem Video. Dieser Test wird vom VGA-Chip ausgeführt und wirkt sich nicht auf die Wiedergabeleistung aus.
-   Allen Beispielen, mit Ausnahme von Livestreams, müssen gültige Start- und Stoppzeitstempel angefügt sein. (DVD ist kein Livestream.)
-   Die Zeitstempel für Medienbeispiele müssen zusammenhängend sein.
-   Der Decoder muss sich selbst als VMR-fähig für die Verwendung durch Graph-Generatoren identifizieren.
-   Der Unterbilddatenstrom sollte nun eingebettete Alphawerte pro Pixel enthalten. Der ARGB4444-Oberflächentyp eignet sich ideal für Unterzeichnungen.
-   Gehen Sie nicht davon aus, dass der Strich des Unterbilds mit der Breite der Oberfläche identisch ist. Dies ist bei der VMR nicht immer der Fall.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur DirectX-Videobeschleunigung](about-directx-video-acceleration.md)
</dt> </dl>

 

 



