---
description: DV-Daten im AVI-Dateiformat
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: DV-Daten im AVI-Dateiformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c048cb42fa3ba49457c115944075c064b9cfd4c31263519e9d5af3e5f0a268a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749110"
---
# <a name="dv-data-in-the-avi-file-format"></a>DV-Daten im AVI-Dateiformat

Microsoft hat das Format für die Speicherung digitaler Videodaten (DV) in AVI-Dateien angegeben. Durch Die Einhaltung dieser Spezifikation wird sichergestellt, dass die in diesem Format erstellten AVI-Dateien mit zukünftigen Versionen der digitalen Videoarchitektur directShow für windowsplatform kompatibel sind.

In diesem Artikel wird das Format von AVI-Dateien beschrieben, die DV-Daten enthalten. Spezifische FOURCCs (vierstellige Codes) für überlappende DV-Datenströme und DV-Entsprechungs-/Dekomprimierungsstreamhandler werden definiert. Die Streamformatstruktur für DV-Daten wird definiert. Es werden Spezifikationen für zwei Methoden zum Speichern von DV-Daten im AVI-Dateiformat angegeben.

Es wird davon ausgegangen, dass der Reader mit dem DV-Datenformat vertraut ist. (Dieses Format wird in der *Spezifikation von consumer-use Digital VCRs* definiert, die auch als Blue Book bezeichnet wird.)

Es gibt zwei Arten von DV AVI-Dateien: AVI-Dateien, die einen DV-Datenstrom enthalten, die als *Type-1-Dateien* bezeichnet werden; und AVI-Dateien, die DV-Videos als "vids"-Datenstrom und DV-Audiodatenströme als "auds"-Datenströme enthalten, die als *Typ-2-Dateien* bezeichnet werden.

**AVI-Dateien mit einem DV-Datenstrom (Typ-1)**

Verschachtelte DV-Daten können in ihrem nativen Format als einzelner Datenstrom in einer AVI DATEIFORMAT-Datei gespeichert werden. Dies hat den Vorteil, dass die Mindestmenge an Datenspeicherung für DV verwendet wird. Der Hauptnachteil besteht darin, dass dieses Dateiformat nicht abwärtskompatibel mit Video für Windows ist, da es weder einen Videostream "vids" noch einen Audiostream "auds" enthält. Unterstützung für den überlappenden DV-Stream wird über die [Filter DV Muxer](dv-muxer-filter.md) und [DV Splitter](dv-splitter-filter.md) bereitgestellt, die mit DirectShow bereitgestellt werden.

DV-Daten können in einem einzelnen Datenstrom innerhalb einer AVI DOSSIER-Datei gespeichert werden, indem im **fccType-Member** die FOURCC-Datei "iavs" (überlappender Audio- und Videodatenstrom) und entweder der "dvsd", "dvhd" oder "dvsl" FOURCCs im **fccHandler-Member** des Header-Chunks "strh" angegeben werden. Die Frames pro Sekunde des Videodatenstroms müssen in den **DwRate-** und **dwScale-Membern** und der Gesamtanzahl von Videoblöcken im Block "mlappen" im **dwLength-Element** angegeben werden.

Der DVSD-Streamhandler FOURCC gibt an, dass die DV-Daten in Teil 2 der *Spezifikation der Consumer-use Digital VCRs* definiert sind. Das Video hat das Format 525 Zeilen bei 29,97 Hz (525-60) oder 625 Zeilen bei 25,00 Hz (625-50).

Der "dvhd"-Streamhandler FOURCC gibt an, dass die DV-Daten gemäß Teil 3 der *Spezifikation der consumer-use Digital VCRs* definiert sind. Das Video hat das Format 1125 Zeilen bei 30,00 Hz (1125-60) oder 1250 Zeilen bei 25,00 Hz (1250-50).

Der "dvsl"-Streamhandler FOURCC gibt an, dass die DV-Daten wie in Teil 6 der *Spezifikation der consumer-use Digital VCRs* definiert sind. Das Video hat das Format von SD mit hoher Komprimierung (HIGH-Compression SD, SDL).

> [!Note]  
> Der Rest dieses Artikels enthält Definitionen für "dvsd"-Streams.

 

Auf den Datenstromheader-Block [](/windows/desktop/api/strmif/ns-strmif-dvinfo) muss ein DVINFO-Datenstromformatabschnitt folgen.

Die tatsächlichen DV-Daten werden als \# \# DC-Blöcke im Block "mung" gespeichert \# \# (das im Format stellt den Datenstrombezeichner dar). Jeder Block enthält einen Datenrahmen, entweder 10 oder 12 DV DIF-Sequenzen für 525-60- bzw. 625-50-Systeme. Das DV SD-DIF-Sequenzformat ('dvsd') ist in Teil 2 der *Spezifikation der Consumer-use Digital VCRs* definiert.

Das folgende Beispiel zeigt das Formular AIFF DATEIFORMAT für eine AVI-Datei mit einem DV-Datenstrom, erweitert mit abgeschlossenen Headerblöcken.


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



**AVI-Dateien mit DV-Video- und DV-Audio-Streams (Typ-2)**

Verschachtelte DV-Daten können in einen Videostream und ein bis vier Audiostreams innerhalb einer AVI-PROTOKOLLDATEI aufgeteilt werden. Dies hat den Vorteil, dass es abwärtskompatibel mit Video für Windows ist, da es einen Standardmäßig-Videostream "vids" und mindestens einen Standardaudiostream "auds" enthält. Der Hauptnachteil besteht darin, dass dieses Dateiformat erfordert, dass die Audiodaten redundant als Audiostreams gespeichert werden. Der Videodatenstrom ist eigentlich der native überlappende DV-Datenstrom. Als Standardstream vom Typ "vids" mit dem Handlertyp "dvsd" wird jedoch der [DV-Videodecoder](dv-video-decoder-filter.md) verwendet. Dieses Format erfordert auch die Verwendung des [DV-Splitterfilters,](dv-splitter-filter.md) um "erfasste" Dateien aufzuteilen, bevor sie als AVI-Dateien geschrieben werden.

DV-Daten können als Videodatenstrom mit einer separaten Anzahl von Audiostreams in einer AVI DATEIFORMAT-Datei gespeichert werden. Der Videostream wird mit einem Standard-Videostreamheader angegeben (der **fccType-Memberwert** ist "vids"). Der **fccHandler-Member** wird als "dvsd", "dvhd" oder "dvsl" angegeben. Die Frames pro Sekunde des Videodatenstroms müssen in den **DwRate-** und **dwScale-Membern** und der Gesamtanzahl von Videoblöcken im Block "mlappen" im **dwLength-Element** angegeben werden.

In dieser AVI-Datei mit DV-Video als "vids"-Stream und DV-Audio als DV-Datenstromform "auds" ist der Block für das Videostreamformat eine standardmäßige [**BITMAPINFOHEADER-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Der Datenstromformat-Block kann optional um den [**DVINFO-Block**](/windows/desktop/api/strmif/ns-strmif-dvinfo) erweitert werden, indem die Größe des Datenstromformatblöckes von 40 Byte (Größe der **BITMAPINFOHEADER-Struktur)** auf 72 Bytes (Größe von **BITMAPINFOHEADER** plus **DVINFO-Strukturen)** erhöht und direkt auf die **BITMAPINFOHEADER-Datenstruktur** mit einer **DVINFO-Datenstruktur** folgt.

Die Audiodatenströme werden mit einem Standard-Audiostreamheader angegeben (der **fccType-Memberwert** ist "auds"). Der **fccHandler-Member** wird nicht für Audiostreams verwendet.

Die DV-Videodaten werden als \# \# "dc"-Blöcke gespeichert, wie in der vorherigen Beschreibung einer AVI-Datei mit einer DV-Daten definiert, und die Audiodaten werden als \# \# wb-Blöcke im Block "m untereinander" gespeichert.

> [!Note]  
> Die *Spezifikation von consumer-use Digital VCRs* ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.

 

Das folgende Beispiel zeigt das AIFF-FORMULAR FÜR EINE AVI-Datei mit DV-Video als "vids"-Stream und DV-Audio als "auds"-Datenströme, die mit abgeschlossenen Headerblöcken erweitert wurden (einschließlich optionaler [**DVINFO-Daten**](/windows/desktop/api/strmif/ns-strmif-dvinfo) nach [**der BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) im Unterabschnitt "strf" für den Datenstrom "vids").


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

[AVI-Dateiformat](avi-file-format.md)
</dt> </dl>

 

 
