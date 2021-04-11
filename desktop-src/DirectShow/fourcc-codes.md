---
description: FourCC-Codes
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: FourCC-Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123566"
---
# <a name="fourcc-codes"></a>FourCC-Codes

Vielen digitalen Medienformaten werden FOURCC-Codes zugewiesen. Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird. Der FourCC-Code für im YUY2 Video lautet beispielsweise "im YUY2". Für komprimierte Videoformate und nicht-RGB-Videoformate (z. b. YUV) sollte der **bicompression** -Member der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur auf den FourCC-Code festgelegt werden.

Es gibt verschiedene C/C++-Makros, die das Deklarieren von FourCC-Werten im Quellcode vereinfachen. Beispielsweise wird das **makefourcc** -Makro in MMSYSTEM. h deklariert, und das **FCC** -Makro wird in aviriff. h deklariert. Verwenden Sie diese wie folgt:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren. Beispiel:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



Das Umkehren der Reihenfolge ist erforderlich, da das Microsoft Windows-Betriebssystem eine Little-Endian-Architektur verwendet. ' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, daher ist ' 2yuy ' 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Umstellen von FOURCC-Codes in Untertyp-GUIDs

Ein Bereich von 2 \* 32 GUIDs ist für die Darstellung von fourccs reserviert. Diese GUIDs sind in der Form, `XXXXXXXX-0000-0010-8000-00AA00389B71` in der `XXXXXXXX` der FourCC-Code ist. Daher ist die Untertyp-GUID für im YUY2 `32595559-0000-0010-8000-00AA00389B71` .

Viele dieser GUIDs sind bereits in der Header Datei "UUIDs. h" definiert. Beispielsweise ist der im YUY2-Untertyp als mediasubtype \_ im YUY2 definiert. Die DirectShow-Basisklassen Bibliothek bietet auch eine Hilfsklasse, " [**fourccmap**](fourccmap.md)", die zum Konvertieren von FOURCC-Codes in GUID-Werte verwendet werden kann. Der **fourccmap** -Konstruktor nimmt einen FourCC-Code als Eingabeparameter an. Anschließend können Sie das **fourccmap** -Objekt in die entsprechende GUID umwandeln:


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Audiountertypen**](audio-subtypes.md)
</dt> <dt>

[Video Untertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Codecs](working-with-codecs.md)
</dt> </dl>

 

 



