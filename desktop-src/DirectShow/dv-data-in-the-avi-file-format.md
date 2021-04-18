---
description: DV-Daten im AVI-Datei Format
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: DV-Daten im AVI-Datei Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482390"
---
# <a name="dv-data-in-the-avi-file-format"></a>DV-Daten im AVI-Datei Format

Microsoft hat das Format für die Speicherung digitaler Videodaten (DV) in AVI-Dateien angegeben. Mit dieser Spezifikation wird sichergestellt, dass die in diesem Format erstellten AVI-Dateien mit zukünftigen Versionen der Architektur von DirectShow Digital Video für das windowsplatform kompatibel sind.

In diesem Artikel wird das Format von AVI-Dateien beschrieben, die DV-Daten enthalten. Bestimmte fourccs (vier Zeichen Codes) für verschachtelte DV-Datenströme und DV-Kompressor/Dekompressor-streamhandler sind definiert. Die Stream-Format Struktur für DV-Daten ist definiert. Spezifikationen für zwei Methoden zum Speichern von DV-Daten im AVI-Dateiformat werden angegeben.

Es wird davon ausgegangen, dass der Reader mit dem DV-Datenformat vertraut ist. (Dieses Format wird in der *Spezifikation von Digital VCRs*, das auch als blaues Buch bezeichnet wird, definiert.)

Es gibt zwei Arten von DV-AVI-Dateien: AVI-Dateien, die einen DV-Datenstrom enthalten, so genannte *Type-1-* Dateien. und AVI-Dateien, die das DV-Video als ' vids '-Stream und DV-Audiodaten als ' auds '-Datenströme ( *Type-2-* Dateien) enthalten.

**AVI-Dateien mit einem DV-Datenstrom (Typ-1)**

Verschachtelte DV-Daten können im nativen Format als einzelner Stream innerhalb einer AVI-Riff Datei gespeichert werden. Dies hat den Vorteil, dass die minimale Menge an Datenspeicher für DV verwendet werden muss. Der Hauptnachteil besteht darin, dass dieses Dateiformat nicht mit dem Video für Windows abwärts kompatibel ist, da es weder ein Video-"vids" noch einen Audiodatei-"auds"-Stream enthält. Unterstützung für den überlappenden DV-Stream über die [DV-Muxer](dv-muxer-filter.md) -und [DV-Splitter](dv-splitter-filter.md) Filter, die mit DirectShow bereitgestellt werden.

DV-Daten können in einem einzelnen Stream innerhalb einer AVI-Riff Datei gespeichert werden, indem die iavs (verschachtelter Audiodaten-und Videostream) FourCC (vier-Zeichen-Code) im **fcctype** -Member und eine der "DVSD", "dvhd ' oder ' dvsl ' fourccs im **fccHandler** -Member des Stream-Header Blocks ' ' Die Frames pro Sekunde des Videodaten Stroms müssen in den Elementen " **dwrate** " und " **dwscale** " und der Gesamtzahl der Video Blöcke im "MOVI"-Segment im **dwLength** -Element angegeben werden.

Der "DVSD"-streamhandler "FourCC" gibt an, dass die DV-Daten wie in Teil 2 der *Spezifikation von "Consumer-use Digital VCRs*" definiert sind. Das Video hat das Format 525 Zeilen bei 29,97 Hz (525-60) oder 625 Zeilen bei 25,00 Hz (625-50).

Der ' dvhd '-streamhandler FourCC gibt an, dass die DV-Daten wie in Teil 3 der *Spezifikation für den verwendeten Consumer-use Digital VCRs* definiert sind. Das Video hat das Format 1125 Zeilen bei 30,00 Hz (1125-60) oder 1250 Zeilen bei 25,00 Hz (1250-50).

Der "dvsl"-streamhandler "FourCC" gibt an, dass die DV-Daten wie in Teil 6 der *Spezifikation von "Consumer-use Digital VCRs*" definiert sind. Das Video hat das Format High-Compression SD (SDL).

> [!Note]  
> Der Rest dieses Artikels enthält Definitionen für "DVSD"-Streams.

 

Auf den Datenstrom-Header Block muss ein [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -streamformatblock folgen.

Die tatsächlichen DV-Daten werden als ' \# \# DC '-Blöcke im Block ' MOVI ' gespeichert (der \# \# im-Format stellt den Datenstrom Bezeichner dar). Jeder Block enthält einen Datenrahmen, entweder 10 oder 12 DV-DIF-Sequenzen für 525-60 bzw. 625-50 Systeme. Das DIF-Sequenz Format DV SD ("DVSD") wird in Teil 2 der *Spezifikation für die Verwendung digitaler VCRs* definiert.

Das folgende Beispiel zeigt das AIFF-Riff Formular für eine AVI-Datei mit einem DV-Datenstrom, der mit abgeschlossenen Header Blöcken erweitert wurde.


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



**AVI-Dateien mit DV-Video-und DV-Audiostreams (Type-2)**

Verschachtelte DV-Daten können in einen Videostream und einen bis vier Audiodatenströme innerhalb einer AVI-Riff Datei aufgeteilt werden. Dies hat den Vorteil, dass Sie mit Video für Windows abwärts kompatibel sind, da es einen standardmäßigen Video-"vids"-Stream und mindestens einen Standardaudiostream "auds" enthält. der Hauptnachteil besteht darin, dass das Dateiformat erfordert, dass die Audiodaten redundant als Audiostreams gespeichert werden. Der "Video"-Stream ist tatsächlich der Native, überlappende DV-Datenstrom. Als Standard-"vids"-Stream mit dem Handlertyp "DVSD" wird jedoch der [DV-Video Decoder](dv-video-decoder-filter.md) verwendet. Dieses Format erfordert außerdem die Verwendung des [DV-Splitter](dv-splitter-filter.md) Filters, um die erfassten Dateien zu teilen, bevor Sie als AVI-Dateien geschrieben werden.

DV-Daten können als Videostream mit einer separaten Anzahl von Audiostreams in einer AVI-Riff Datei gespeichert werden. Der Videostream wird mit einem Standard-videostreamheader angegeben (der Wert des **fcctype** -Members ist ' vids '). Der **fccHandler** -Member ist als "DVSD", "dvhd" oder "dvsl" angegeben. Die Frames pro Sekunde des Videodaten Stroms müssen in den Elementen " **dwrate** " und " **dwscale** " und der Gesamtzahl der Video Blöcke im "MOVI"-Segment im **dwLength** -Element angegeben werden.

In dieser AVI-Datei mit DV-Video als ' vids '-Stream und DV-Audiodaten als ' auds '-Datenströme Form von DV ist das Format Block für den Videostream eine standardmäßige [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur. Der Block für den Datenstrom Format kann optional so erweitert werden, dass er den [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Block einschließt, indem die Segmentgröße des Datenstroms von 40 Byte (Größe der **BITMAPINFOHEADER** -Struktur) auf 72 bytes (Größe der BITMAPINFOHEADER-Plus **dvinfo** -Strukturen) und unmittelbar nach der **BITMAPINFOHEADER** -Datenstruktur mit einer **dvinfo** 

Der Audiostream (s) wird mit einem standardaudiostreamheader angegeben (der Wert des **fcctype** -Members ist ' auds '). Der **fccHandler** -Member wird nicht für Audiostreams verwendet.

Die DV-Videodaten werden als ' \# \# DC '-Blöcke gespeichert, wie in der vorherigen Beschreibung einer AVI-Datei mit einem DV-Daten definiert, und die Audiodaten werden als ' \# \# WB '-Blöcke im Block ' MOVI ' gespeichert.

> [!Note]  
> Die *Angabe von "Consumer-use Digital VCRs* " ist möglicherweise in einigen Sprachen und Ländern nicht verfügbar.

 

Im folgenden Beispiel wird das AIFF-Riff Formular für eine AVI-Datei gezeigt, die das DV-Video als "vids"-Stream und DV-Audiodaten mit abgeschlossenen Header Blöcken erweitert hat (einschließlich Optionaler [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Daten, die auf die BitmapInfo im unter Abschnitt " [**strinmapinfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) " für den "vids"-Datenstrom folgen).


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AVI-Datei Format](avi-file-format.md)
</dt> </dl>

 

 
