---
description: Eine Bitmap ist eines der GDI-Objekte, die in einem Gerätekontext (DC) ausgewählt werden können.
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Informationen zu Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb155a2d96b32303c38438663cb7cc9b893a1560e8f33956ff894d309f055010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355510"
---
# <a name="about-bitmaps"></a>Informationen zu Bitmaps

Eine Bitmap ist eines der GDI-Objekte, die in einem *Gerätekontext* (DC) ausgewählt werden können. [Gerätekontexte](device-contexts.md) sind Strukturen, die eine Reihe von Grafikobjekten und deren zugeordnete Attribute definieren, sowie Grafikmodi, die sich auf die Ausgabe auswirken. In der folgenden Tabelle werden die GDI-Objekte beschrieben, die in einem Gerätekontext ausgewählt werden können.



| Grafikobjekt                         | Beschreibung                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmaps](bitmaps.md)                 | Erstellt, bearbeitet (skalieren, scrollen, drehen und zeichnen) und speichert Bilder als Dateien auf einem Datenträger.                                                                                                       |
| [Pinsel](brushes.md)                 | Zeichnet das Innere von Polygonen, Ellipsen und Pfaden.                                                                                                                                                |
| [Schriftarten](fonts-and-text.md)            | Zeichnet Text auf Videoanzeigen und anderen Ausgabegeräten.                                                                                                                                               |
| [Logische Palette](logical-palette.md) | Eine farbliche Palette, die von einer Anwendung erstellt und einem bestimmten Gerätekontext zugeordnet ist.                                                                                                                |
| [Paths](paths.md)                     | Eine oder mehrere Zahlen (oder Formen), die gefüllt und/oder konturiert sind.                                                                                                                                     |
| [Stifte](pens.md)                       | Ein Grafiktool, das eine Anwendung zum Zeichnen von Linien und Kurven verwendet.                                                                                                                                   |
| [Regionen](regions.md)                 | Ein Rechteck, Polygon oder eine Ellipse (oder eine Kombination aus zwei oder mehr dieser Formen), das gefüllt, gezeichnet, invertiert, gerahmen und zum Ausführen von Treffertests verwendet werden kann (Testen der Cursorposition). |



 

Aus Sicht eines Entwicklers besteht eine Bitmap aus einer Auflistung von Strukturen, die die folgenden Elemente angeben oder enthalten:

-   Ein Header, der die Auflösung des Geräts beschreibt, auf dem das Pixelrechteck erstellt wurde, die Abmessungen des Rechtecks, die Größe des Arrays von Bits usw.
-   Eine logische Palette.
-   Ein Array von Bits, das die Beziehung zwischen Pixeln im Bitmapbild und Einträgen in der logischen Palette definiert.

Eine Bitmapgröße hängt mit dem Typ des enthaltenen Bilds zusammen. Bitmapbilder können monocolore oder color sein. In einem Bild entspricht jedes Pixel einem oder mehreren Bits in einer Bitmap. Monocolore Bilder weisen ein Verhältnis von 1 Bit pro Pixel (bpp) auf. Die Farbbilderstellung ist komplexer. Die Anzahl der Farben, die von einer Bitmap angezeigt werden können, ist gleich zwei, die auf die Anzahl der Bits pro Pixel erhöht werden. Daher erfordert eine Bitmap mit 256 Farben 8 BPP (2^8 = 256).

Systemsteuerung Anwendungen sind Beispiele für Anwendungen, die Bitmaps verwenden. Wenn Sie einen Hintergrund (oder Hintergrundbild) für Ihren Desktop auswählen, wählen Sie tatsächlich eine Bitmap aus, die das System verwendet, um den Desktophintergrund zu zeichnen. Das System erstellt das ausgewählte Hintergrundmuster, indem es wiederholt ein 32 x 32 Pixel großes Muster auf dem Desktop zeichnet.

Die folgende Abbildung zeigt die Perspektive des Entwicklers der Bitmap in der Datei Redbrick.bmp. Es zeigt ein Palettenarray, ein 32 x 32 Pixel großes Rechteck und das Indexarray, das Farben aus der Palette Pixeln im Rechteck zuweist.

![Abbildung des Pixelrechtecks, Palettenarrays und Indexarrays von redbrick.bmp](images/csbmp-01.png)

Im vorherigen Beispiel wurde das Rechteck von Pixeln auf einem VGA-Anzeigegerät mit einer Palette von 16 Farben erstellt. Eine 16-Farbpalette erfordert 4-Bit-Indizes. Daher besteht das Array, das Palettenfarben Pixelfarben zuweist, ebenfalls aus 4-Bit-Indizes. (Weitere Informationen zu logischen Farbpaletten finden Sie unter [Farben](colors.md).)

> [!Note]
>
> In der obigen Bitmap ordnet das System Indizes Pixeln zu, beginnend mit der unteren Scanzeile des rechteckigen Bereichs und endend mit der oberen Scanlinie. Eine *Scanzeile* ist eine einzelne Zeile mit angrenzenden Pixeln auf einer Videoanzeige. Beispielsweise entspricht die erste Zeile des Arrays (Zeile 0) der unteren Zeile von Pixeln, Scanzeile 31. Dies liegt daran, dass es sich bei der obigen Bitmap um eine geräteunabhängige Bottom-Up-Bitmap (DIB) handelt, eine gängige Art von Bitmap. In DIBs von oben nach unten und in geräteabhängigen Bitmaps (DDB) ordnet das System Indizes Pixeln zu, die mit der oberen Scanzeile beginnen.

 

In den folgenden Themen werden verschiedene Bereiche von Bitmaps beschrieben.

-   [Bitmapklassifizierungen](bitmap-classifications.md)
-   [Bitmapheadertypen](bitmap-header-types.md)
-   [JPEG- und PNG-Erweiterungen für bestimmte Bitmapfunktionen und -strukturen](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Bitmaps, Gerätekontexte und Zeichnungsoberflächen](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Bitmaperstellung](bitmap-creation.md)
-   [Bitmaprotation](bitmap-rotation.md)
-   [Bitmapskalierung](bitmap-scaling.md)
-   [Bitmaps als Pinsel](bitmaps-as-brushes.md)
-   [Bitmap-Storage](bitmap-storage.md)
-   [Bitmapkomprimierung](bitmap-compression.md)
-   [Alphablending](alpha-blending.md)
-   [Smooth Shading](smooth-shading.md)
-   [ICM-fähige Bitmapfunktionen](icm-enabled-bitmap-functions.md)

 

 



