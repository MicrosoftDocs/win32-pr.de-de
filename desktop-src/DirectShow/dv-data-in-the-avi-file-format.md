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
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="7a4ba-103">DV-Daten im AVI-Datei Format</span><span class="sxs-lookup"><span data-stu-id="7a4ba-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="7a4ba-104">Microsoft hat das Format für die Speicherung digitaler Videodaten (DV) in AVI-Dateien angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="7a4ba-105">Mit dieser Spezifikation wird sichergestellt, dass die in diesem Format erstellten AVI-Dateien mit zukünftigen Versionen der Architektur von DirectShow Digital Video für das windowsplatform kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="7a4ba-106">In diesem Artikel wird das Format von AVI-Dateien beschrieben, die DV-Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="7a4ba-107">Bestimmte fourccs (vier Zeichen Codes) für verschachtelte DV-Datenströme und DV-Kompressor/Dekompressor-streamhandler sind definiert.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="7a4ba-108">Die Stream-Format Struktur für DV-Daten ist definiert.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="7a4ba-109">Spezifikationen für zwei Methoden zum Speichern von DV-Daten im AVI-Dateiformat werden angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="7a4ba-110">Es wird davon ausgegangen, dass der Reader mit dem DV-Datenformat vertraut ist.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="7a4ba-111">(Dieses Format wird in der *Spezifikation von Digital VCRs*, das auch als blaues Buch bezeichnet wird, definiert.)</span><span class="sxs-lookup"><span data-stu-id="7a4ba-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="7a4ba-112">Es gibt zwei Arten von DV-AVI-Dateien: AVI-Dateien, die einen DV-Datenstrom enthalten, so genannte *Type-1-* Dateien. und AVI-Dateien, die das DV-Video als ' vids '-Stream und DV-Audiodaten als ' auds '-Datenströme ( *Type-2-* Dateien) enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="7a4ba-113">**AVI-Dateien mit einem DV-Datenstrom (Typ-1)**</span><span class="sxs-lookup"><span data-stu-id="7a4ba-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="7a4ba-114">Verschachtelte DV-Daten können im nativen Format als einzelner Stream innerhalb einer AVI-Riff Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="7a4ba-115">Dies hat den Vorteil, dass die minimale Menge an Datenspeicher für DV verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="7a4ba-116">Der Hauptnachteil besteht darin, dass dieses Dateiformat nicht mit dem Video für Windows abwärts kompatibel ist, da es weder ein Video-"vids" noch einen Audiodatei-"auds"-Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="7a4ba-117">Unterstützung für den überlappenden DV-Stream über die [DV-Muxer](dv-muxer-filter.md) -und [DV-Splitter](dv-splitter-filter.md) Filter, die mit DirectShow bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="7a4ba-118">DV-Daten können in einem einzelnen Stream innerhalb einer AVI-Riff Datei gespeichert werden, indem die iavs (verschachtelter Audiodaten-und Videostream) FourCC (vier-Zeichen-Code) im **fcctype** -Member und eine der "DVSD", "dvhd ' oder ' dvsl ' fourccs im **fccHandler** -Member des Stream-Header Blocks ' '</span><span class="sxs-lookup"><span data-stu-id="7a4ba-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="7a4ba-119">Die Frames pro Sekunde des Videodaten Stroms müssen in den Elementen " **dwrate** " und " **dwscale** " und der Gesamtzahl der Video Blöcke im "MOVI"-Segment im **dwLength** -Element angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="7a4ba-120">Der "DVSD"-streamhandler "FourCC" gibt an, dass die DV-Daten wie in Teil 2 der *Spezifikation von "Consumer-use Digital VCRs*" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="7a4ba-121">Das Video hat das Format 525 Zeilen bei 29,97 Hz (525-60) oder 625 Zeilen bei 25,00 Hz (625-50).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="7a4ba-122">Der ' dvhd '-streamhandler FourCC gibt an, dass die DV-Daten wie in Teil 3 der *Spezifikation für den verwendeten Consumer-use Digital VCRs* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="7a4ba-123">Das Video hat das Format 1125 Zeilen bei 30,00 Hz (1125-60) oder 1250 Zeilen bei 25,00 Hz (1250-50).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="7a4ba-124">Der "dvsl"-streamhandler "FourCC" gibt an, dass die DV-Daten wie in Teil 6 der *Spezifikation von "Consumer-use Digital VCRs*" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="7a4ba-125">Das Video hat das Format High-Compression SD (SDL).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="7a4ba-126">Der Rest dieses Artikels enthält Definitionen für "DVSD"-Streams.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="7a4ba-127">Auf den Datenstrom-Header Block muss ein [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -streamformatblock folgen.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="7a4ba-128">Die tatsächlichen DV-Daten werden als ' \# \# DC '-Blöcke im Block ' MOVI ' gespeichert (der \# \# im-Format stellt den Datenstrom Bezeichner dar).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="7a4ba-129">Jeder Block enthält einen Datenrahmen, entweder 10 oder 12 DV-DIF-Sequenzen für 525-60 bzw. 625-50 Systeme.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="7a4ba-130">Das DIF-Sequenz Format DV SD ("DVSD") wird in Teil 2 der *Spezifikation für die Verwendung digitaler VCRs* definiert.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="7a4ba-131">Das folgende Beispiel zeigt das AIFF-Riff Formular für eine AVI-Datei mit einem DV-Datenstrom, der mit abgeschlossenen Header Blöcken erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


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



<span data-ttu-id="7a4ba-132">**AVI-Dateien mit DV-Video-und DV-Audiostreams (Type-2)**</span><span class="sxs-lookup"><span data-stu-id="7a4ba-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="7a4ba-133">Verschachtelte DV-Daten können in einen Videostream und einen bis vier Audiodatenströme innerhalb einer AVI-Riff Datei aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="7a4ba-134">Dies hat den Vorteil, dass Sie mit Video für Windows abwärts kompatibel sind, da es einen standardmäßigen Video-"vids"-Stream und mindestens einen Standardaudiostream "auds" enthält. der Hauptnachteil besteht darin, dass das Dateiformat erfordert, dass die Audiodaten redundant als Audiostreams gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="7a4ba-135">Der "Video"-Stream ist tatsächlich der Native, überlappende DV-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="7a4ba-136">Als Standard-"vids"-Stream mit dem Handlertyp "DVSD" wird jedoch der [DV-Video Decoder](dv-video-decoder-filter.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="7a4ba-137">Dieses Format erfordert außerdem die Verwendung des [DV-Splitter](dv-splitter-filter.md) Filters, um die erfassten Dateien zu teilen, bevor Sie als AVI-Dateien geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="7a4ba-138">DV-Daten können als Videostream mit einer separaten Anzahl von Audiostreams in einer AVI-Riff Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="7a4ba-139">Der Videostream wird mit einem Standard-videostreamheader angegeben (der Wert des **fcctype** -Members ist ' vids ').</span><span class="sxs-lookup"><span data-stu-id="7a4ba-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="7a4ba-140">Der **fccHandler** -Member ist als "DVSD", "dvhd" oder "dvsl" angegeben.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="7a4ba-141">Die Frames pro Sekunde des Videodaten Stroms müssen in den Elementen " **dwrate** " und " **dwscale** " und der Gesamtzahl der Video Blöcke im "MOVI"-Segment im **dwLength** -Element angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="7a4ba-142">In dieser AVI-Datei mit DV-Video als ' vids '-Stream und DV-Audiodaten als ' auds '-Datenströme Form von DV ist das Format Block für den Videostream eine standardmäßige [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="7a4ba-143">Der Block für den Datenstrom Format kann optional so erweitert werden, dass er den [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Block einschließt, indem die Segmentgröße des Datenstroms von 40 Byte (Größe der **BITMAPINFOHEADER** -Struktur) auf 72 bytes (Größe der BITMAPINFOHEADER-Plus **dvinfo** -Strukturen) und unmittelbar nach der **BITMAPINFOHEADER** -Datenstruktur mit einer **dvinfo** </span><span class="sxs-lookup"><span data-stu-id="7a4ba-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="7a4ba-144">Der Audiostream (s) wird mit einem standardaudiostreamheader angegeben (der Wert des **fcctype** -Members ist ' auds ').</span><span class="sxs-lookup"><span data-stu-id="7a4ba-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="7a4ba-145">Der **fccHandler** -Member wird nicht für Audiostreams verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="7a4ba-146">Die DV-Videodaten werden als ' \# \# DC '-Blöcke gespeichert, wie in der vorherigen Beschreibung einer AVI-Datei mit einem DV-Daten definiert, und die Audiodaten werden als ' \# \# WB '-Blöcke im Block ' MOVI ' gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="7a4ba-147">Die *Angabe von "Consumer-use Digital VCRs* " ist möglicherweise in einigen Sprachen und Ländern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="7a4ba-148">Im folgenden Beispiel wird das AIFF-Riff Formular für eine AVI-Datei gezeigt, die das DV-Video als "vids"-Stream und DV-Audiodaten mit abgeschlossenen Header Blöcken erweitert hat (einschließlich Optionaler [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Daten, die auf die BitmapInfo im unter Abschnitt " [**strinmapinfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) " für den "vids"-Datenstrom folgen).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a4ba-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a4ba-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4ba-150">AVI-Datei Format</span><span class="sxs-lookup"><span data-stu-id="7a4ba-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
