---
description: Wenn Sie nur die obere linke Ecke eines Bilds an die DrawImage-Methode übergeben, Windows GDI+ das Bild skalieren, was die Leistung beeinträchtigen würde.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Verbessern der Leistung durch Vermeiden der automatischen Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac74fbf636f3f1cbdf088939ad76732907c15228e66662a7246b3f0c0313c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778730"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Verbessern der Leistung durch Vermeiden der automatischen Skalierung

Wenn Sie nur die obere linke Ecke eines Bilds an die **DrawImage-Methode** übergeben, Windows GDI+ das Bild skalieren, was die Leistung beeinträchtigen würde.

Der folgende Aufruf der **DrawImage-Methode** gibt eine linke obere Ecke von (50, 30) an, aber kein Zielrechteck:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Obwohl dies die einfachste Version der **DrawImage-Methode** in Bezug auf die Anzahl der erforderlichen Argumente ist, ist sie nicht unbedingt die effizienteste. Wenn sich die Anzahl der Punkte pro Zoll auf dem aktuellen Anzeigegerät von der Anzahl der Punkte pro Zoll auf dem Gerät, auf dem das Bild erstellt wurde, unterscheiden, skaliert GDI+ das Bild so, dass seine physische Größe auf dem aktuellen Anzeigegerät so nah wie möglich an seiner physischen Größe auf dem Gerät liegt, auf dem es erstellt wurde.

Wenn Sie eine solche Skalierung verhindern möchten, übergeben Sie die Breite und Höhe eines Zielrechtecks an die **DrawImage-Methode.** Im folgenden Beispiel wird das gleiche Bild zweimal ge zeichnet. Im ersten Fall werden Breite und Höhe des Zielrechtecks nicht angegeben, und das Bild wird automatisch skaliert. Im zweiten Fall werden Die Breite und Höhe (gemessen in Pixel) des Zielrechtecks mit der Breite und Höhe des ursprünglichen Bilds identisch sein.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



Die folgende Abbildung zeigt das zweimal gerenderte Bild.

![Screenshot eines Fensters, das zwei Versionen eines Bilds in unterschiedlichen Skalierungen enthält](images/scaledtexture1.png)

 

 



