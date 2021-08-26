---
description: FOURCC-Codes
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: FOURCC-Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25820d21fb8e8386fb11816c373debf427fa783b8a2f2d4723a46e689e6aea0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043320"
---
# <a name="fourcc-codes"></a>FOURCC-Codes

Vielen digitalen Medienformaten sind FOURCC-Codes zugewiesen. Ein FOURCC-Code ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird. Der FOURCC-Code für das YUY2-Video ist beispielsweise "YUY2". Bei komprimierten Videoformaten und Nicht-RGB-Videoformaten (z. B. YUV) sollte das **biCompression-Element** der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) auf den FOURCC-Code festgelegt werden.

Es gibt verschiedene C/C++-Makros, die das Deklarieren von FOURCC-Werten im Quellcode vereinfachen. Beispielsweise wird das **MAKEFOURCC-Makro** in Mmsystem.h deklariert, und das **FCC-Makro** wird in Aviriff.h deklariert. Verwenden Sie sie wie folgt:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



Sie können einen FOURCC-Code auch direkt als Zeichenfolgenliteral deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren. Beispiel:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



Das Umkehren der Reihenfolge ist erforderlich, da das Microsoft Windows-Betriebssystem eine Little-Endian-Architektur verwendet. "Y" = 0x59, "U" = 0x55 und "2" = 0x32, sodass "2 TOKENY" 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Konvertieren von FOURCC-Codes in Untertyp-GUIDs

Ein Bereich von 2 \* 32 GUIDs ist für die Darstellung von FOURCCs reserviert. Diese GUIDs haben alle das Formular, `XXXXXXXX-0000-0010-8000-00AA00389B71` wobei `XXXXXXXX` der FOURCC-Code ist. Daher ist die Untertyp-GUID für YUY2 `32595559-0000-0010-8000-00AA00389B71` .

Viele dieser GUIDs sind bereits in der Headerdatei Uuids.h definiert. Der YUY2-Untertyp ist beispielsweise als MEDIASUBTYPE \_ YUY2 definiert. Die DirectShow-Basisklassenbibliothek stellt auch die Hilfsklasse [**FOURCCMap**](fourccmap.md)zur Verfügung, die zum Konvertieren von FOURCC-Codes in GUID-Werte verwendet werden kann. Der **FOURCCMap-Konstruktor** akzeptiert einen FOURCC-Code als Eingabeparameter. Anschließend können Sie das **FOURCCMap-Objekt** in die entsprechende GUID umwanden:


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

[Videountertypen](video-subtypes.md)
</dt> <dt>

[Arbeiten mit Codecs](working-with-codecs.md)
</dt> </dl>

 

 



