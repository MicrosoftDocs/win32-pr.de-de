---
description: Ein Bitmap-Objekt ist eines der GDI-Objekte, das in einen Gerätekontext (DC) ausgewählt werden kann.
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Informationen zu Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dbba516734dc255ce33005a7a9073865765785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527707"
---
# <a name="about-bitmaps"></a>Informationen zu Bitmaps

Ein Bitmap-Objekt ist eines der GDI-Objekte, das in einen *Gerätekontext* (DC) ausgewählt werden kann. [Geräte Kontexte](device-contexts.md) sind Strukturen, die eine Gruppe von Grafikobjekten und ihren zugeordneten Attributen definieren, sowie Grafikmodi, die die Ausgabe beeinflussen. In der folgenden Tabelle werden die GDI-Objekte beschrieben, die in einem Gerätekontext ausgewählt werden können.



| Grafik Objekt                         | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmaps](bitmaps.md)                 | Erstellt, manipuliert (Skalieren, scrollen, drehen und zeichnen) und speichert Bilder als Dateien auf einem Datenträger.                                                                                                       |
| [Pinsel](brushes.md)                 | Zeichnet das Innere von Polygonen, Ellipsen und Pfaden.                                                                                                                                                |
| [Schriftarten](fonts-and-text.md)            | Zeichnet Text in Video anzeigen und anderen Ausgabegeräten.                                                                                                                                               |
| [Logische Palette](logical-palette.md) | Eine Farbpalette, die von einer Anwendung erstellt und einem bestimmten Gerätekontext zugeordnet ist.                                                                                                                |
| [Paths](paths.md)                     | Eine oder mehrere Abbildungen (oder Formen), die ausgefüllt und/oder beschrieben werden.                                                                                                                                     |
| [Stifte](pens.md)                       | Ein Grafik Tool, das eine Anwendung zum Zeichnen von Linien und Kurven verwendet.                                                                                                                                   |
| [Regionen](regions.md)                 | Ein Rechteck, ein Polygon oder eine Ellipse (oder eine Kombination aus mindestens zwei Formen), die ausgefüllt, gezeichnet, invertiert, gerahmt und zum Ausführen von Treffer Tests (Testen der Cursorposition) verwendet werden können. |



 

Aus der Perspektive eines Entwicklers besteht eine Bitmap aus einer Auflistung von-Strukturen, die die folgenden Elemente angeben oder enthalten:

-   Ein Header, der die Auflösung des Geräts, auf dem das Rechteck von Pixeln erstellt wurde, die Abmessungen des Rechtecks, die Größe des Bits-Arrays usw. beschreibt.
-   Eine logische Palette.
-   Ein Array von Bits, das die Beziehung zwischen Pixeln im bitzugeordneten Bild und Einträgen in der logischen Palette definiert.

Eine Bitmapgröße bezieht sich auf den Typ des darin enthaltenen Bilds. Bitmap-Bilder können entweder Mono oder Color sein. In einem Bild entspricht jedes Pixel einem oder mehreren Bits in einer Bitmap. Monochrome Abbilder haben ein Verhältnis von 1 Bit pro Pixel (BPP). Die Farb Abbild Erstellung ist komplexer. Die Anzahl von Farben, die von einer Bitmap angezeigt werden können, ist gleich zwei, die auf die Anzahl der Bits pro Pixel festgelegt ist. Daher erfordert eine 256-farbige Bitmap 8 bpp (2 ^ 8 = 256).

System Steuerungsanwendungen sind Beispiele für Anwendungen, die Bitmaps verwenden. Wenn Sie für den Desktop einen Hintergrund (oder ein Hintergrundbild) auswählen, wählen Sie tatsächlich eine Bitmap aus, die vom System zum Zeichnen des Desktop Hintergrunds verwendet wird. Das System erstellt das ausgewählte Hintergrundmuster durch wiederholtes Zeichnen eines 32-by-32-Pixel Musters auf dem Desktop.

Die folgende Abbildung zeigt die Perspektive des Entwicklers der Bitmap, die in der Datei Redbrick.bmp gefunden wurde. Es zeigt ein palettenarray, ein 32-bis-32 Pixel-Rechteck und das Index Array, das Farben aus der Palette den Pixeln im Rechteck zuordnet.

![Abbildung des Pixel Rechtecks, Palette Arrays und des Index Arrays von redbrick.bmp](images/csbmp-01.png)

Im vorherigen Beispiel wurde das Rechteck der Pixel auf einem VGA-Anzeigegerät mithilfe einer Palette von 16 Farben erstellt. Eine 16-farbige Palette erfordert 4-Bit-Indizes. Daher besteht das Array, das Palettenfarben zu Pixel Farben zuordnet, auch aus 4-Bit-Indizes. (Weitere Informationen zu logischen Farbpaletten finden Sie unter [Farben](colors.md).)

> [!Note]
>
> In der obigen Bitmap ordnet das System Indizes zu Pixeln zu, beginnend mit der untersten Überprüfungs Linie des rechteckigen Bereichs und endet mit der obersten Scan Zeile. Eine *Scan Linie* ist eine einzelne Zeile mit angrenzenden Pixeln in einer Videoanzeige. Die erste Zeile des Arrays (Zeile 0) entspricht z. b. der untersten Zeile der Pixel, Scan Zeile 31. Dies liegt daran, dass es sich bei der obigen Bitmap um eine geräteunabhängige Bitmap (DIB) im unteren Bereich handelt, eine gängige bitmapart. In von oben nach unten und in geräteabhängigen Bitmaps (DDB) ordnet das System Indizes zu Pixeln zu, beginnend mit der obersten Überprüfungs Zeile.

 

In den folgenden Themen werden die verschiedenen Bereiche von Bitmaps beschrieben.

-   [Bitmap-Klassifizierungen](bitmap-classifications.md)
-   [Bitmap-Header Typen](bitmap-header-types.md)
-   [JPEG-und PNG-Erweiterungen für bestimmte Bitmap-Funktionen und-Strukturen](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Bitmaps, Geräte Kontexte und Zeichnungs Oberflächen](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Bitmap-Erstellung](bitmap-creation.md)
-   [Bitmap-Drehung](bitmap-rotation.md)
-   [Bitmapskalierung](bitmap-scaling.md)
-   [Bitmaps als Pinsel](bitmaps-as-brushes.md)
-   [Bitmapspeicher](bitmap-storage.md)
-   [Bitmapkomprimierung](bitmap-compression.md)
-   [Alpha Blending](alpha-blending.md)
-   [Smooth-Schattierung](smooth-shading.md)
-   [ICM-aktivierte Bitmap-Funktionen](icm-enabled-bitmap-functions.md)

 

 



