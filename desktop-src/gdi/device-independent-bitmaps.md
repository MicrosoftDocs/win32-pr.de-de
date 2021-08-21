---
description: Eine geräteunabhängige Bitmap (DIB) enthält eine Farbtabelle.
ms.assetid: 56b39a3d-48a4-4620-9652-ec41ea4d6423
title: Device-Independent Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6672857aadda714e7016616ca78654d7da102b48c1229c5b322953fc716f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761389"
---
# <a name="device-independent-bitmaps"></a>Device-Independent Bitmaps

Eine geräteunabhängige Bitmap (DEVICE-Independent Bitmap, DIB) enthält eine *Farbtabelle.* In einer Farbtabelle wird beschrieben, wie Pixelwerte *RGB-Farbwerten* entsprechen, die Farben beschreiben, die durch das Austonen von Licht erzeugt werden. Daher kann ein DIB auf jedem Gerät das richtige Farbschema erzielen. Ein DIB enthält die folgenden Farb- und Dimensionsinformationen:

-   Das Farbformat des Geräts, auf dem das rechteckige Bild erstellt wurde.
-   Die Auflösung des Geräts, auf dem das rechteckige Bild erstellt wurde.
-   Die Palette für das Gerät, auf dem das Bild erstellt wurde.
-   Ein Array von Bits, das rot, grün, blau ( [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) ) Triplets zu Pixeln im rechteckigen Bild zu ordnet.
-   Ein Datenkomprimierungsbezeichner, der das Datenkomprimierungsschema angibt (falls möglich), das verwendet wird, um die Größe des Bitsarrays zu reduzieren.

Die Farb- und Dimensionsinformationen werden in einer [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) gespeichert, die aus einer [**BITMAPINFOHEADER-Struktur**](/previous-versions//dd183376(v=vs.85)) gefolgt von zwei oder mehr [**RGBQUAD-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) besteht. Die **BITMAPINFOHEADER-Struktur** gibt die Abmessungen des Pixelrechtecks an, beschreibt die Farbtechnologie des Geräts und identifiziert die Komprimierungsschemas, mit deren Hilfe die Größe der Bitmap reduziert wird. Die **RGBQUAD-Strukturen** identifizieren die Farben, die im Pixelrechteck angezeigt werden.

Es gibt zwei Varianten von DIBs:

-   Ein DIB von unten nach oben, in dem sich der Ursprung in der unteren linken Ecke befindet.
-   Ein DIB von oben nach unten, in dem sich der Ursprung in der oberen linken Ecke befindet.

Wenn die Höhe eines DIB, wie durch den **Height-Member** der Bitmapinformationsheaderstruktur angegeben, ein positiver Wert ist, handelt es sich um einen DIB von unten nach oben. Wenn die Höhe ein negativer Wert ist, handelt es sich um einen DIB von oben nach unten. DiBs von oben nach unten können nicht komprimiert werden.

Das Farbformat wird als Anzahl von Farbebenen und Farbbits angegeben. Die Anzahl der Farbebenen ist immer 1. Die Anzahl der Farbbits beträgt 1 für monofarbige Bitmaps, 4 für VGA-Bitmaps und 8, 16, 24 oder 32 für Bitmaps auf anderen Farbgeräten. Eine Anwendung ruft die Anzahl der Farbbits ab, die von einer bestimmten Anzeige (oder einem Drucker) verwendet werden, indem die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) aufgerufen und BITSPIXEL als zweites Argument angegeben wird.

Die Auflösung eines Anzeigegeräts wird in Pixel pro Meter angegeben. Eine Anwendung kann die horizontale Auflösung für eine Videoanzeige oder einen Drucker mit diesem dreistufigen Prozess abrufen.

1.  Rufen Sie [**die GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) auf, und geben Sie HORZRES als zweites Argument an.
2.  Rufen [**Sie GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) ein zweites Mal auf, und geben Sie HORZSIZE als zweites Argument an.
3.  Dividieren Sie den ersten Rückgabewert durch den zweiten Rückgabewert.

Die Anwendung kann die vertikale Auflösung abrufen, indem sie den gleichen dreistufigen Prozess mit verschiedenen Parametern verwendet: VERTRES statt HORZRES und VERTSIZE statt HORZSIZE.

Die Palette wird durch ein Array von [**RGBQUAD-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) dargestellt, die die Komponenten mit roter, grüner und blauer Intensität für jede Farbe in der Farbpalette eines Anzeigegeräts angeben. Jeder Farbindex im Palettenarray wird einem bestimmten Pixel im rechteckigen Bereich zugeordnet, der der Bitmap zugeordnet ist. Die Größe dieses Arrays in Bits entspricht der Breite des Rechtecks in Pixel, multipliziert mit der Höhe des Rechtecks in Pixel, multipliziert mit der Anzahl der Farbbits für das Gerät. Eine Anwendung kann die Größe der Gerätepalette abrufen, indem sie die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) aufruft, und NUMCOLORS als zweites Argument angeben.

Windows unterstützt die Komprimierung des Palettenarrays für 8-bpp- und 4-bpp-DIBs von unten nach oben. Diese Arrays können mithilfe des RLE-Schemas (Run-Length Encoding) komprimiert werden. Das RLE-Schema verwendet 2-Byte-Werte, das erste Byte, das die Anzahl der aufeinander folgenden Pixel an gibt, die einen Farbindex verwenden, und das zweite Byte, das den Index an gibt. Weitere Informationen zur Bitmapkomprimierung finden Sie in der Beschreibung der [**BitmapINFOHEADER-,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPFILEHEADER-,**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) [**BITMAPV4HEADER-**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)und [**BITMAPV5HEADER-Strukturen.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Eine Anwendung kann einen DIB aus einer DDB erstellen, indem sie die erforderlichen Strukturen initialisiert und die [**GetDIBits-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) aufruft. Um zu bestimmen, ob ein Gerät diese Funktion unterstützt, rufen Sie die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) auf, und geben Sie RC \_ DI BITMAP als \_ RASTERCAPS-Flag an.

Eine Anwendung, die eine Bitmap kopieren muss, kann [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) verwenden, um alle Pixel in einer Quellbitmap in eine Zielbitmap mit Ausnahme der Pixel zu kopieren, die der transparenten Farbe entsprechen.

Eine Anwendung kann mithilfe eines DIB Pixel auf dem Anzeigegerät festlegen, indem sie [**setDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) oder [**die StretchDIBits-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) aufruft. Um zu bestimmen, ob ein Gerät die **SetDIBitsToDevice-Funktion** unterstützt, rufen Sie die [**GetDeviceCaps-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) auf, und geben Sie RC \_ DIBTODEV als RASTERCAPS-Flag an. Geben Sie RC STRETCHDIB als RASTERCAPS-Flag an, um zu bestimmen, ob das Gerät \_ **StretchDIBits unterstützt.**

Eine Anwendung, die lediglich ein bereits vorhandenes DIB anzeigen muss, kann die [**Funktion SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) verwenden. Beispielsweise kann eine Tabellenkalkulationsanwendung vorhandene Diagramme öffnen und mithilfe der **Funktion SetDIBitsToDevice** in einem Fenster anzeigen. Um eine Bitmap in einem Fenster wiederholt neu zu erstellen, sollte die Anwendung jedoch die [**BitBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) verwenden. Beispielsweise würde eine Multimediaanwendung, die animierte Grafiken mit Sound kombiniert, vom Aufrufen der **BitBlt-Funktion** profitieren, da sie schneller als **SetDIBitsToDevice ausgeführt wird.**

 

 
