---
description: Wenn Sie nur die linke obere Ecke eines Bilds an die DrawImage-Methode übergeben, kann Windows GDI+ das Image skalieren, wodurch die Leistung beeinträchtigt wird.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Verbessern der Leistung durch vermeiden der automatischen Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979008"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Verbessern der Leistung durch vermeiden der automatischen Skalierung

Wenn Sie nur die linke obere Ecke eines Bilds an die **DrawImage** -Methode übergeben, kann Windows GDI+ das Image skalieren, wodurch die Leistung beeinträchtigt wird.

Der folgende Rückruf der **DrawImage** -Methode gibt eine linke obere Ecke von (50, 30) an, gibt jedoch kein Ziel Rechteck an:


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Obwohl es sich hierbei um die einfachste Version der **DrawImage** -Methode im Hinblick auf die Anzahl der erforderlichen Argumente handelt, ist dies nicht unbedingt die effizienteste Methode. Wenn sich die Anzahl der Punkte pro Zoll auf dem aktuellen Anzeigegerät von der Anzahl der Punkte pro Zoll auf dem Gerät unterscheidet, auf dem das Abbild erstellt wurde, skaliert GDI+ das Abbild so, dass seine physische Größe auf dem aktuellen Anzeigegerät so nah wie möglich auf dem Gerät ist, auf dem es erstellt wurde.

Wenn Sie eine solche Skalierung vermeiden möchten, übergeben Sie die Breite und Höhe eines Ziel Rechtecks an die **DrawImage** -Methode. Im folgenden Beispiel wird das gleiche Bild zweimal gezeichnet. Im ersten Fall werden die Breite und Höhe des Ziel Rechtecks nicht angegeben, und das Bild wird automatisch skaliert. Im zweiten Fall werden Breite und Höhe (gemessen in Pixel) des Ziel Rechtecks als identisch mit der Breite und Höhe des ursprünglichen Bilds angegeben.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



In der folgenden Abbildung wird das Bild zweimal gerendert.

![Screenshot eines Fensters, das zwei Versionen eines Bilds in unterschiedlichen Skalen enthält](images/scaledtexture1.png)

 

 



