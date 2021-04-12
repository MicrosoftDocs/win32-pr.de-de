---
description: Video fourccs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Video fourccs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344849"
---
# <a name="video-fourccs"></a>Video fourccs

Vielen Videoformaten werden FOURCC-Codes zugewiesen. Bei einem FourCC-Code handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird. Der FourCC-Code für im YUY2 Video lautet beispielsweise "im YUY2".

Zum Deklarieren von FourCC-Werten im Quellcode sind verschiedene C/C++-Makros definiert. Das **makefourcc** -Makro ist in "MMSYSTEM. h" definiert, und das " **FCC** "-Makro wird in "aviriff. h" und verschiedenen anderen Header Dateien definiert. Sie können einen FourCC-Code auch direkt als Zeichenfolgenliterale deklarieren, indem Sie einfach die Reihenfolge der Zeichen umkehren. Daher sind die folgenden Anweisungen äquivalent:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

(Im letzten Beispiel ist das Umkehren der Byte Reihenfolge erforderlich, da Windows eine Little-Endian-Architektur verwendet. ' Y ' = 0x59, ' U ' = 0x55 und ' 2 ' = 0x32, also ' 2yuy ' ist 0x32595559.)

Einige der [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md) -APIs verwenden einen **D3DFORMAT** -Wert, um ein Video Format zu beschreiben. Ein FourCC-Code kann auch in diesem Kontext verwendet werden:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>FourCC-Konstanten

In der folgenden Tabelle sind einige gängige FOURCC-Codes aufgeführt.



| FourCC-Wert | BESCHREIBUNG                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| H264       | H. 264-Video.                                                                                                          |
| 'I420'       | YUV-Video, das im planare 4:2:0-Format gespeichert ist.                                                                              |
| "IYUV"       | YUV-Video, das im planare 4:2:0-Format gespeichert ist.                                                                              |
| X 4s2 '       | MPEG-4 Part 2-Video.                                                                                                  |
| MP4 Bitrate       | Microsoft MPEG 4 Codec Version 3. Dieser Codec wird nicht mehr unterstützt.                                                  |
| MP4V       | MPEG-4 Part 2-Video.                                                                                                  |
| 'MPG1'       | MPEG-1-Video.                                                                                                         |
| 'MSS1'       | Inhalt, der mit dem Windows Media Video 7-Bildschirm Codec codiert ist.                                                          |
| 'MSS2'       | Inhalt, der mit dem Windows Media Video 9-Bildschirm Codec codiert ist.                                                          |
| UYVY       | YUV-Video im gepackten 4:2:2-Format gespeichert. Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.                         |
| 'WMV1'       | Mit dem Windows Media Video 7-Codec codierter Inhalt.                                                                 |
| 'WMV2'       | Mit dem Windows Media Video 8-Codec codierter Inhalt.                                                                 |
| 'WMV3'       | Mit dem Windows Media Video 9-Codec codierter Inhalt.                                                                 |
| "Wmva"       | Inhalt, der mit der älteren, veralteten Version von Windows Media Video 9 Advanced Profile Codec codiert ist.                 |
| "Wmvp"       | Inhalt, der mit Windows Media Video dem 9,1-Bildcodec codiert wurde.                                                         |
| 'WVC1'       | SMPTE 421m ("VC-1"). Inhalt, der mit Windows Media Video 9 Advanced Profile codiert ist.                                     |
| 'WVP2'       | Inhalt, der mit dem Windows Media Video 9,1 Image V2-Codec codiert ist.                                                      |
| Im YUY2       | YUV-Video im gepackten 4:2:2-Format gespeichert.                                                                              |
| 'YV12'       | YUV-Video, das im planare 4:2:0-oder 4:1:1-Format gespeichert ist. Identisch mit I420/IYUV, mit dem Unterschied, dass die Ebenen you und V gewechselt werden. |
| YVU9       | YUV-Video, das im planare 16:1:1-Format gespeichert ist.                                                                             |
| Im yvyu       | YUV-Video im gepackten 4:2:2-Format gespeichert. Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[Video Untertyp-GUIDs](video-subtype-guids.md)
</dt> </dl>

 

 



