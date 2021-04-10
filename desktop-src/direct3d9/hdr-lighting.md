---
description: Beleuchtung in der realen Welt enthält einen sehr hohen dynamischen Bereich (HDR) von Leuchtkraft Werten.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: HDR-Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213801"
---
# <a name="hdr-lighting-direct3d-9"></a>HDR-Beleuchtung (Direct3D 9)

Beleuchtung in der realen Welt enthält einen sehr hohen dynamischen Bereich (HDR) von Leuchtkraft Werten. Die reale Welt hat ungefähr 10 Aufträge des dynamischen Bereichs (Dr) für Glanzwerte, die auf das Spektrum von Dunkelheit und Helligkeit verteilt sind. Andererseits hat ein Computerbildschirm einen sehr begrenzten Anzeigebereich (oder Bereich von Leuchtkraft Werten): ungefähr zwei Aufträge des dynamischen Bereichs. Die Herausforderung bei der Erstellung von HDR-gerenderten Images besteht darin, die realen HDR-Werte in den begrenzten Bereich eines Computerbildschirms zuzuordnen.

Die Tonzuordnung ist das Verfahren, das von DirectX zum Mapping von HDR-Informationen in einem eingeschränkteren Bereich verwendet wird. Die auf CGI-Rendering angewendete Tonzuordnung kann die Menge der dargestellten Beleuchtungs Details erheblich verbessern, sodass Details in den dunkelsten Bereichen angezeigt werden, und der Kontrast in Bereichen, die so hell sind, wird angezeigt. Die resultierenden Szenen werden mit deutlich ausführlicheren Beleuchtungs Details dargestellt.

[Hdrbeleuchtungs Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) ist ein SDK-Beispiel, das die HDR-Beleuchtung veranschaulicht.

## <a name="tone-mapping"></a>Ton Zuordnung

Die Tone-Zuordnung simuliert in der Regel optische Phänomene, die nicht von der Dr des Monitors verursacht werden können. Beispiele hierfür sind Flares oder blühende (in der Regel Eigenschaften von-Linsen), die blaue Schicht, die in der menschlichen Perspektive in niedrigen Lichtbedingungen auftritt, und andere Anpassungen, die das Ergebnis der Biochemie der Augen sind. Wenn die Notfall Wiederherstellung groß genug wäre, wäre die Audiozuordnung nicht so notwendig, außer bei der Bereitstellung von künstlerischen Effekten oder einigen der Eigenschaften eines Kamerabildes oder eines gekoppelten Geräts ("-CCD").

Die Tone-Zuordnung dividiert den Bereich der Leuchtkraft Werte in einer Szene in eine Gruppe von Zonen. Jede Zone umfasst einen Bereich von Leuchtkraft Werten.

In HDR werden folgende Begriffe verwendet:

-   Zonen Bereich von Leuchtkraft Werten
-   Bereich für die Helligkeit der mittleren grauen Mitte der Szene
-   Dynamisches Bereichs Verhältnis der höchsten Szenen Beleuchtung zur untersten Szenen Beleuchtung
-   Schlüssel-subjektives Maß der Szenen Beleuchtung: Dies variiert zwischen Licht und Mittel bis dunkel

Um die Leuchtkraft aus RGB-Werten zu berechnen, verwenden Sie Folgendes:


```
L = 0.27R + 0.67G + 0.06B;
```



Die Protokoll durchschnittliche Leuchtkraft ist eine nützliche Näherung für den Schlüssel einer Szene. Eine allgemeine Gleichung sieht wie folgt aus:

L<sub>w</sub> = exp \[ 1/N (Summen \[ Protokoll (Delta + L<sub>w</sub>(x, y)) \] ) \]

Hierbei gilt:

-   L<sub>w</sub> -durchschnittliche Leuchtkraft für Protokoll
-   N-Anzahl der Pixel im Bild
-   Delta-ein kleiner Faktor, um Probleme mit schwarzen Pixeln zu vermeiden
-   L<sub>w</sub>(x, y)-die Welt Raumbeleuchtung für Pixel (x, y)

Um diese einem mittelgrauen Wert zuzuordnen, finden Sie hier einen "Leuchtkraft Skalierungs Operator":

L (x, y) = a \* L<sub>w</sub>(x, y)/L<sub>w</sub>

Hierbei gilt:

-   L (x, y): skalierte Leuchtkraft für Pixel (x, y)
-   Schlüsselwert eines Bilds nach dem Anwenden der Skalierung

Und schließlich ist hier ein einfacher tonzuordnungsoperator zum Komprimieren der hohen Leuchtkraft:

L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))

Hierbei gilt:

-   L<sub>d</sub>(x, y)-komprimierte und skalierte Leuchtkraft für Pixel (x, y)
-   Schlüsselwert eines Bilds nach dem Anwenden der Skalierung

Dieser Operator skaliert hohe Leuchtkraft um 1/L und niedrige Leucht Ordnungen um 1. Weitere Informationen finden Sie im folgenden Artikel.

Reinhard, Erik, Mike stark, Peter Shirley und James Ferwerda. ["Fototon-Reproduktion für digitale Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf). ACM-Transaktionen auf Grafiken (Info), das Sitzungsprotokoll der 29. jährlichen Konferenz zu Computer Grafiken und interaktiven Techniken (SIGGRAPH), pp. 267-276. New York, NY: ACM, 2002.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 



