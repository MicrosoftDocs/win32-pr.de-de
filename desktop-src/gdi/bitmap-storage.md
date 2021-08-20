---
description: Bitmaps sollten in einer Datei gespeichert werden, die das eingerichtete Bitmapdateiformat verwendet und einen Namen mit der aus drei Zeichen .bmp hat.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Bitmap-Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83688f240899ded49227264b716d8c5d1fb609aa747fc358184a78ad18c8d17f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038208"
---
# <a name="bitmap-storage"></a>Bitmap-Storage

Bitmaps sollten in einer Datei gespeichert werden, die das eingerichtete Bitmapdateiformat verwendet und einen Namen mit der aus drei Zeichen .bmp hat. Das eingerichtete Bitmapdateiformat besteht aus einer [**BITMAPFILEHEADER-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) gefolgt von einer [**BITMAPINFOHEADER-,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER-**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)oder [**BITMAPV5HEADER-Struktur.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) Ein Array von [**RGBQUAD-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) (auch als Farbtabelle bezeichnet) folgt der Bitmapinformationsheaderstruktur. Auf die Farbtabelle folgt ein zweites Array von Indizes in der Farbtabelle (die tatsächlichen Bitmapdaten).

Das Bitmapdateiformat wird in der folgenden Abbildung dargestellt.

![Diagramm des Bitmapdateiformats mit bitmapfileheader, bitmapinfoheader, rgbquad array und color-index array](images/csbmp-02.png)

Die Member der [**BITMAPFILEHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) identifizieren die Datei. geben Sie die Größe der Datei in Bytes an. und geben den Offset vom ersten Byte im Header bis zum ersten Byte der Bitmapdaten an. Die Member der [**BITMAPINFOHEADER-,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER-**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)oder [**BITMAPV5HEADER-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) geben die Breite und Höhe der Bitmap in Pixel an. das Farbformat (Anzahl der Farbebenen und Farbbits pro Pixel) des Anzeigegeräts, auf dem die Bitmap erstellt wurde; gibt an, ob die Bitmapdaten vor dem Speichern komprimiert wurden und welche Art von Komprimierung verwendet wurde; die Anzahl der Bytes von Bitmapdaten; die Auflösung des Anzeigegeräts, auf dem die Bitmap erstellt wurde; und die Anzahl der in den Daten dargestellten Farben. Die [**RGBQUAD-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) geben die RGB-Intensitätswerte für jede der Farben in der Gerätepalette an.

Das Farbindexarray ordnet eine Farbe in Form eines Indexes einer [**RGBQUAD-Struktur**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) mit jedem Pixel in einer Bitmap zu. Daher entspricht die Anzahl der Bits im Farbindexarray der Anzahl von Pixeln, die der Anzahl der Bits entspricht, die zum Indizieren der **RGBQUAD-Strukturen erforderlich** sind. Beispielsweise verfügt eine 8x8-Bitmap aus Schwarz und Weiß über ein Farbindexarray von 8 \* 8 \* 1 = 64 Bit, da ein Bit zum Indizieren von zwei Farben benötigt wird. Die Redbrick.bmp, die unter About Bitmaps (Informationen zu [Bitmaps)](about-bitmaps.md)erwähnt wird, ist eine 32x32-Bitmap mit 16 Farben. Sein Farbindexarray ist 32 \* 32 \* 4 = 4.096 Bits, da vier Bits 16 Farben indizieren.

Um ein Farbindexarray für eine Bitmap von oben nach unten zu erstellen, beginnen Sie mit der oberen Zeile in der Bitmap. Der Index des [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) für die Farbe des linkssten Pixels ist die ersten *n* Bits im Farbindexarray (wobei *n* die Anzahl der Bits ist, die zum Angeben aller **RGBQUAD-Strukturen** erforderlich sind). Die Farbe des nächsten Pixels rechts ist die nächsten *n* Bits im Array usw. Nachdem Sie das Pixel ganz rechts in der Zeile erreicht haben, fahren Sie mit dem ganz links stehenden Pixel in der folgenden Zeile fort. Fahren Sie fort, bis Sie mit der gesamten Bitmap fertig sind. Wenn es sich um eine Bitmap von unten nach oben handelt, beginnen Sie in der unteren Zeile der Bitmap und nicht in der oberen Zeile, gehen sie immer noch von links nach rechts, und fahren Sie mit der oberen Zeile der Bitmap fort.

Die folgende hexadezimale Ausgabe zeigt den Inhalt der Datei Redbrick.bmp.


```C++
0000    42 4d 76 02 00 00 00 00  00 00 76 00 00 00 28 00 
0010    00 00 20 00 00 00 20 00  00 00 01 00 04 00 00 00 
0020    00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00 
0030    00 00 00 00 00 00 00 00  00 00 00 00 80 00 00 80 
0040    00 00 00 80 80 00 80 00  00 00 80 00 80 00 80 80 
0050    00 00 80 80 80 00 c0 c0  c0 00 00 00 ff 00 00 ff 
0060    00 00 00 ff ff 00 ff 00  00 00 ff 00 ff 00 ff ff 
0070    00 00 ff ff ff 00 00 00  00 00 00 00 00 00 00 00 
0080    00 00 00 00 00 00 00 00  00 00 00 00 00 00 09 00 
0090    00 00 00 00 00 00 11 11  01 19 11 01 10 10 09 09 
00a0    01 09 11 11 01 90 11 01  19 09 09 91 11 10 09 11 
00b0    09 11 19 10 90 11 19 01  19 19 10 10 11 10 09 01 
00c0    91 10 91 09 10 10 90 99  11 11 11 11 19 00 09 01 
00d0    91 01 01 19 00 99 11 10  11 91 99 11 09 90 09 91 
00e0    01 11 11 11 91 10 09 19  01 00 11 90 91 10 09 01 
00f0    11 99 10 01 11 11 91 11  11 19 10 11 99 10 09 10 
0100    01 11 11 11 19 10 11 09  09 10 19 10 10 10 09 01 
0110    11 19 00 01 10 19 10 11  11 01 99 01 11 90 09 19 
0120    11 91 11 91 01 11 19 10  99 00 01 19 09 10 09 19 
0130    10 91 11 01 11 11 91 01  91 19 11 00 99 90 09 01 
0140    01 99 19 01 91 10 19 91  91 09 11 99 11 10 09 91 
0150    11 10 11 91 99 10 90 11  01 11 11 19 11 90 09 11 
0160    00 19 10 11 01 11 99 99  99 99 99 99 99 99 09 99 
0170    99 99 99 99 99 99 00 00  00 00 00 00 00 00 00 00 
0180    00 00 00 00 00 00 90 00  00 00 00 00 00 00 00 00 
0190    00 00 00 00 00 00 99 11  11 11 19 10 19 19 11 09 
01a0    10 90 91 90 91 00 91 19  19 09 01 10 09 01 11 11 
01b0    91 11 11 11 10 00 91 11  01 19 10 11 10 01 01 11 
01c0    90 11 11 11 91 00 99 09  19 10 11 90 09 90 91 01 
01d0    19 09 91 11 01 00 90 10  19 11 00 11 11 00 10 11 
01e0    01 10 11 19 11 00 90 19  10 91 01 90 19 99 00 11 
01f0    91 01 11 01 91 00 99 09  09 01 10 11 91 01 10 91 
0200    99 11 10 90 91 00 91 11  00 10 11 01 10 19 19 09 
0210    10 00 99 01 01 00 91 01  19 91 19 91 11 09 10 11 
0220    00 91 00 10 90 00 99 01  11 10 09 10 10 19 09 01 
0230    91 90 11 09 11 00 90 99  11 11 11 90 19 01 19 01 
0240    91 01 01 19 09 00 91 10  11 91 99 09 09 90 11 91 
0250    01 19 11 11 91 00 91 19  01 00 11 00 91 10 11 01 
0260    11 11 10 01 11 00 99 99  99 99 99 99 99 99 99 99 
0270    99 99 99 99 99 90 
```



Die folgende Tabelle zeigt die Datenbytes, die den Strukturen in einer Bitmapdatei zugeordnet sind.



| Struktur                                    | Entsprechende Bytes |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x0E 0x35           |
| [**RGBQUAD-Array**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)             | 0x36 0x75           |
| Farbindexarray                            | 0x76 0x275          |



 

 

 
