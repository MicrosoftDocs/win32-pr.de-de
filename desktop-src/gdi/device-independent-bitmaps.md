---
description: Eine geräteunabhängige Bitmap (DIB) enthält eine Farbtabelle.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Bitmaps Device-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa35201a9a27c2d16a5a18b0125d25a3938890c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130800"
---
# <a name="device-independent-bitmaps"></a>Bitmaps Device-Independent

Eine geräteunabhängige Bitmap (DIB) enthält eine *Farbtabelle*. In einer Farbtabelle wird beschrieben, wie Pixelwerte *RGB* -Farbwerten entsprechen, die Farben beschreiben, die durch Ausgeben von Licht erzeugt werden. Daher kann ein DIB das richtige Farbschema auf jedem Gerät erreichen. Ein DIB enthält die folgenden Farb-und Dimensions Informationen:

-   Das Farb Format des Geräts, auf dem das rechteckige Bild erstellt wurde.
-   Die Auflösung des Geräts, auf dem das rechteckige Image erstellt wurde.
-   Die Palette für das Gerät, auf dem das Image erstellt wurde.
-   Ein Array von Bits, das rote, grüne, blaue ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) )-drei-und Pixel im rechteckigen Bild zuordnet.
-   Ein Bezeichner für die Datenkomprimierung, der das Daten Komprimierungs Schema (sofern vorhanden) angibt, mit dem die Größe des Bits-Arrays reduziert wird.

Die Farb-und Dimensions Informationen werden in einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur gespeichert, die aus einer [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur gefolgt von zwei oder mehr [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen besteht. Die **BITMAPINFOHEADER** -Struktur gibt die Abmessungen des Pixel Rechtecks an, beschreibt die Farb Technologie des Geräts und identifiziert die Komprimierungs Schemas, die verwendet werden, um die Größe der Bitmap zu verringern. Die **rgbquad** -Strukturen identifizieren die Farben, die im Pixel Rechteck angezeigt werden.

Es gibt zwei Arten von Disb:

-   Ein Bottom-up-DIB, bei dem der Ursprung in der unteren linken Ecke liegt.
-   Eine Top-Down-DIB, bei der sich der Ursprung in der linken oberen Ecke befindet.

Wenn die Höhe eines DIB, wie durch das **height** -Element der Bitmap-Informations Header Struktur angegeben, ein positiver Wert ist, ist es ein unterer DIB. Wenn die Höhe ein negativer Wert ist, ist Sie eine Top-Down-DIB. Top-Down-Disb können nicht komprimiert werden.

Das Farb Format wird in Bezug auf die Anzahl von Farbebenen und Farbbits angegeben. Die Anzahl von Farbebenen ist immer 1. die Anzahl der Farbbits ist 1 für monochrome Bitmaps, 4 für VGA-Bitmaps und 8, 16, 24 oder 32 für Bitmaps auf anderen Farb Geräten. Eine Anwendung ruft die Anzahl der Farbbits ab, die eine bestimmte Anzeige (oder ein Drucker) verwendet, indem Sie die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen und bitspixel als zweites Argument angibt.

Die Auflösung eines Anzeige Geräts wird in Pixel pro Meter angegeben. Eine Anwendung kann die horizontale Auflösung für eine Videoanzeige oder einen Drucker abrufen, indem Sie diesen dreistufigen Prozess folgt.

1.  Aufrufen der [**getde vicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion, wobei horzres als zweites Argument angegeben werden.
2.  Ruft [**getde vicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) ein zweites Mal auf, wobei horzsize als zweites Argument angegeben wird.
3.  Dividiert den ersten Rückgabewert durch den zweiten Rückgabewert.

Die Anwendung kann die vertikale Auflösung abrufen, indem Sie den gleichen dreistufigen Prozess mit unterschiedlichen Parametern verwendet: "vertres" anstelle von "horzres" und "vertsize" anstelle von "horzsize".

Die Palette wird durch ein Array von [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen dargestellt, die die roten, grünen und blauen Intensität-Komponenten für die einzelnen Farben in der Farbpalette eines Anzeige Geräts angeben. Jeder Farbindex im Palette-Array ist einem bestimmten Pixel im rechteckigen Bereich zugeordnet, der der Bitmap zugeordnet ist. Die Größe dieses Arrays in Bits entspricht der Breite des Rechtecks in Pixel, multipliziert mit der Höhe des Rechtecks in Pixel, multipliziert mit der Anzahl der Farbbits für das Gerät. Eine Anwendung kann die Größe der Gerätepalette abrufen, indem Sie die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen und dabei numcolors als zweites Argument angibt.

Windows unterstützt die Komprimierung des Palette-Arrays für 8-bpp-und 4-bpp-nach-oben-DIB. Diese Arrays können mithilfe des RLE-Schemas (Run-Length Encoding) komprimiert werden. Das RLE-Schema verwendet 2-Byte-Werte, das erste Byte, das die Anzahl der aufeinander folgenden Pixel angibt, die einen Farbindex verwenden, und das zweite Byte, das den Index angibt. Weitere Informationen zur Bitmapkomprimierung finden Sie in der Beschreibung der Strukturen [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)und [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .

Eine Anwendung kann ein DIB aus einer DDB erstellen, indem Sie die erforderlichen Strukturen initialisiert und die [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) -Funktion aufruft. Um zu ermitteln, ob ein Gerät diese Funktion unterstützt, können Sie die [**getdebug**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen und die RC \_ di- \_ Bitmap als RasterCaps-Flag angeben.

Eine Anwendung, die eine Bitmap kopieren muss, kann mithilfe von [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) alle Pixel in einer Quell Bitmap in eine Ziel Bitmap kopieren, ausgenommen die Pixel, die der transparenten Farbe entsprechen.

Eine Anwendung kann einen DIB verwenden, um Pixel auf dem Anzeigegerät durch Aufrufen der [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) -oder der [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) -Funktion festzulegen. Um zu ermitteln, ob ein Gerät die **SetDIBitsToDevice** -Funktion unterstützt, können Sie die [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen und RC \_ dibtodev als RasterCaps-Flag angeben. Geben \_ Sie RC stretchdib als RasterCaps-Flag an, um zu bestimmen, ob das Gerät **StretchDIBits** unterstützt.

Eine Anwendung, die lediglich ein bereits vorhandenes DIB anzeigen muss, kann die [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) -Funktion verwenden. Beispielsweise kann eine Tabellenkalkulationsanwendung vorhandene Diagramme öffnen und mithilfe der **SetDIBitsToDevice** -Funktion in einem Fenster anzeigen. Zum wiederholten Neuzeichnen einer Bitmap in einem Fenster sollte die Anwendung jedoch die [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) -Funktion verwenden. Beispielsweise könnte eine Multimedia-Anwendung, die animierte Grafiken mit Sound kombiniert, von dem Aufruf der **BitBLT** -Funktion profitieren, da Sie schneller als **SetDIBitsToDevice** ausgeführt wird.

 

 
