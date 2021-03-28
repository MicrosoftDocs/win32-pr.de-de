---
description: Bitmaps sollten in einer Datei gespeichert werden, die das festgelegte Bitmapdateiformat verwendet, und mit der Erweiterung "drei Zeichen. bmp" einen Namen zugewiesen.
ms.assetid: 44f19d14-4e0e-4512-8c86-6bd34ca4e87b
title: Bitmapspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28046f6d78f5137d0dfc5b1396bbf76be318daa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130845"
---
# <a name="bitmap-storage"></a>Bitmapspeicher

Bitmaps sollten in einer Datei gespeichert werden, die das festgelegte Bitmapdateiformat verwendet, und mit der Erweiterung "drei Zeichen. bmp" einen Namen zugewiesen. Das festgelegte Bitmapdateiformat besteht aus einer [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) -Struktur, gefolgt von einer [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-oder [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur. Ein Array aus [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen (auch als Farbtabelle bezeichnet) folgt der Struktur der bitmapinformationsheader. Auf die Farbtabelle folgt ein zweites Array von Indizes in die Farbtabelle (die eigentlichen Bitmapdaten).

Das Bitmapdateiformat ist in der folgenden Abbildung dargestellt.

![Diagramm des bitmapdateiformats, das BITMAPFILEHEADER, BITMAPINFOHEADER, rgbquad Array und Farb Index Array anzeigt](images/csbmp-02.png)

Die Elemente der [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) -Struktur identifizieren die Datei. Geben Sie die Größe der Datei in Bytes an. und geben den Offset vom ersten Byte in der Kopfzeile bis zum ersten Byte der Bitmapdaten an. Die Elemente der [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)-oder [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Struktur geben die Breite und Höhe der Bitmap in Pixel an. das Farb Format (Anzahl von Farbebenen und Farbbits pro Pixel) des Anzeige Geräts, auf dem die Bitmap erstellt wurde. Gibt an, ob die Bitmapdaten vor dem Speicher und dem verwendeten Komprimierungstyp komprimiert wurden. die Anzahl der Bytes von Bitmapdaten. die Auflösung des Anzeige Geräts, auf dem die Bitmap erstellt wurde. und die Anzahl der in den Daten dargestellten Farben. Die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Strukturen geben die RGB-Intensitätswerte für die einzelnen Farben in der Palette des Geräts an.

Das Farb Index Array ordnet eine Farbe in Form eines Indexes einer [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur zu, wobei jedes Pixel in einer Bitmap angezeigt wird. Daher entspricht die Anzahl der Bits im Farb Index Array der Anzahl der Pixel, die für die Indizierung der **rgbquad** -Strukturen benötigt wird. Beispielsweise verfügt eine "8x8 Black-and-White"-Bitmap über ein Farb Index Array von 8 \* 8 \* 1 = 64 Bits, da ein Bit erforderlich ist, um zwei Farben zu indizieren. Der in [Informationen zu Bitmaps](about-bitmaps.md)erwähnte Redbrick.bmp ist eine 32 x 32-Bitmap mit 16 Farben. das Farb Index Array ist 32 \* 32 \* 4 = 4096 Bits, da vier Bits den Wert 16 Farben haben.

Zum Erstellen eines Farb Index Arrays für eine Top-Down-Bitmap beginnen Sie in der obersten Zeile in der Bitmap. Der Index von [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) für die Farbe des äußersten linken Pixels ist die erste *n* Bits im Farb Index Array (wobei *n* die Anzahl der Bits ist, die zum Angeben aller **rgbquad** -Strukturen benötigt werden). Die Farbe des nächsten Pixels auf der rechten Seite entspricht den nächsten *n* Bits im Array usw. Nachdem Sie das ganz rechts Pixel in der Linie erreicht haben, fahren Sie mit dem äußersten linken Pixel in der folgenden Zeile fort. Fahren Sie fort, bis die gesamte Bitmap abgeschlossen ist. Wenn es sich um eine untere Bitmap handelt, starten Sie in der unteren Zeile der Bitmap statt in der oberen Zeile, und fahren Sie von links nach rechts fort, und fahren Sie mit der obersten Zeile der Bitmap fort.

In der folgenden hexadezimalen Ausgabe wird der Inhalt der Datei Redbrick.bmp angezeigt.


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



In der folgenden Tabelle werden die Daten Bytes angezeigt, die den Strukturen in einer Bitmapdatei zugeordnet sind.



| Struktur                                    | Entsprechende bytes |
|----------------------------------------------|---------------------|
| [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader) | 0x00 0x0D           |
| [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) | 0x0E 0x35           |
| [**Rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Array             | 0x36 0x75           |
| Farb Index Array                            | 0x76 0x275          |



 

 

 
