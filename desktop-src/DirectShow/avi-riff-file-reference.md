---
description: Referenz zu AVI-Riff Dateien
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referenz zu AVI-Riff Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482547"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="cfabf-103">Referenz zu AVI-Riff Dateien</span><span class="sxs-lookup"><span data-stu-id="cfabf-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="cfabf-104">Das Microsoft AVI-Dateiformat ist eine bitdateispezifikation, die für Anwendungen verwendet wird, die audiovideosequenzen erfassen, bearbeiten und wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="cfabf-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="cfabf-105">Im Allgemeinen enthalten AVI-Dateien mehrere Streams mit unterschiedlichen Datentypen.</span><span class="sxs-lookup"><span data-stu-id="cfabf-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="cfabf-106">Die meisten AVI-Sequenzen verwenden sowohl Audiodaten als auch Videodaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="cfabf-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="cfabf-107">Eine einfache Variation für eine AVI-Sequenz verwendet Videodaten und erfordert keinen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="cfabf-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="cfabf-108">In diesem Abschnitt werden die Dateiformat Erweiterungen von OpenDML AVI nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cfabf-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="cfabf-109">Weitere Informationen zu diesen Erweiterungen finden Sie unter *OpenDML AVI-Dateiformat Erweiterungen*, die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="cfabf-110">Fourccs</span><span class="sxs-lookup"><span data-stu-id="cfabf-110">FOURCCs</span></span>

<span data-ttu-id="cfabf-111">Ein FourCC (aus vier Zeichen bestehende Code) ist 32 eine Ganzzahl ohne Vorzeichen, die durch die Verkettung von vier ASCII-Zeichen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cfabf-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="cfabf-112">Das FourCC "abcd" wird beispielsweise auf einem Little-Endian System als 0x64636261 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cfabf-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="cfabf-113">Fourccs kann Leerzeichen enthalten, sodass "ABC" ein gültiger FourCC ist.</span><span class="sxs-lookup"><span data-stu-id="cfabf-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="cfabf-114">Das Dateiformat AVI verwendet FOURCC-Codes, um Streamtypen, Datenblöcke, Indexeinträge und andere Informationen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cfabf-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="cfabf-115">Riff-Datei Format</span><span class="sxs-lookup"><span data-stu-id="cfabf-115">RIFF File Format</span></span>

<span data-ttu-id="cfabf-116">Das Format der AVI-Datei basiert auf dem Dokumentformat "Riff" (Ressourcenaustausch Dateiformat).</span><span class="sxs-lookup"><span data-stu-id="cfabf-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="cfabf-117">Eine Riff Datei besteht aus einem Riff-Header, gefolgt von NULL oder mehr *Listen* und *Blöcken*.</span><span class="sxs-lookup"><span data-stu-id="cfabf-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="cfabf-118">Der Riff-Header weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="cfabf-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="cfabf-119">Wenn ' Riff ' der Literale FourCC-Code ' Riff ' ist, `fileSize` ist ein 4-Byte-Wert, der die Größe der Daten in der Datei angibt, und `fileType` ein FourCC, der den spezifischen Dateityp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cfabf-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="cfabf-120">Der Wert von `fileSize` schließt die Größe des `fileType` FourCC plus die Größe der nachfolgenden Daten ein, aber nicht die Größe von ' Riff ' FourCC oder die Größe von `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="cfabf-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="cfabf-121">Die Datei Daten bestehen aus Blöcken und Listen in beliebiger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cfabf-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="cfabf-122">Ein Block weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="cfabf-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="cfabf-123">dabei `ckID` ist ein FourCC, der die im Block enthaltenen Daten identifiziert, `ckSize` ein 4-Byte-Wert, der die Größe der Daten in angibt `ckData` , und `ckData` 0 (null) oder mehr Daten bytes.</span><span class="sxs-lookup"><span data-stu-id="cfabf-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="cfabf-124">Die Daten werden immer bis zum nächsten **Wort** Rand aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="cfabf-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="cfabf-125">`ckSize` Gibt die Größe der gültigen Daten im Block an. die Auffüll Zeichen, die Größe von `ckID` oder die Größe von sind nicht enthalten `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="cfabf-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="cfabf-126">Eine Liste weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="cfabf-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="cfabf-127">wobei ' List ' der Literale FourCC-Code ' List ' ist, `listSize` ein 4-Byte-Wert, der die Größe der Liste angibt, `listType` ein FourCC-Code ist und `listData` aus Blöcken oder Listen in beliebiger Reihenfolge besteht.</span><span class="sxs-lookup"><span data-stu-id="cfabf-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="cfabf-128">Der Wert von `listSize` schließt die Größe von `listType` plus der Größe von ein `listData` ; er enthält nicht den "List"-FourCC oder die Größe von `listSize` .</span><span class="sxs-lookup"><span data-stu-id="cfabf-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="cfabf-129">Im restlichen Teil dieses Abschnitts werden die folgenden Notation zum Beschreiben von Riff Segmenten verwendet:</span><span class="sxs-lookup"><span data-stu-id="cfabf-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="cfabf-130">Gibt an, wo die Segmentgröße implizit ist.</span><span class="sxs-lookup"><span data-stu-id="cfabf-130">where the chunk size is implicit.</span></span> <span data-ttu-id="cfabf-131">Mit dieser Notation kann eine Liste wie folgt dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="cfabf-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="cfabf-132">Optionale Elemente werden in eckige Klammern gestellt: `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="cfabf-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="cfabf-133">AVI-Riff-Formular</span><span class="sxs-lookup"><span data-stu-id="cfabf-133">AVI RIFF Form</span></span>

<span data-ttu-id="cfabf-134">AVI-Dateien werden durch den FourCC "AVI" im Riff-Header identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cfabf-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="cfabf-135">Alle AVI-Dateien enthalten zwei verbindliche Listen Blöcke, die das Format der Streams bzw. der Streamdaten definieren.</span><span class="sxs-lookup"><span data-stu-id="cfabf-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="cfabf-136">Eine AVI-Datei kann auch einen Indexblock enthalten, der den Speicherort der Datenblöcke in der Datei liefert.</span><span class="sxs-lookup"><span data-stu-id="cfabf-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="cfabf-137">Eine AVI-Datei mit diesen Komponenten weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="cfabf-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="cfabf-138">Die Liste "HDRL" definiert das Format der Daten und ist das erste erforderliche Listen Segment.</span><span class="sxs-lookup"><span data-stu-id="cfabf-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="cfabf-139">Die "MOVI"-Liste enthält die Daten für die AVI-Sequenz und ist das zweite erforderliche Listen Segment.</span><span class="sxs-lookup"><span data-stu-id="cfabf-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="cfabf-140">Die "idx1"-Liste enthält den Index.</span><span class="sxs-lookup"><span data-stu-id="cfabf-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="cfabf-141">Bei AVI-Dateien müssen diese drei Komponenten in der richtigen Reihenfolge aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="cfabf-142">Die OpenDML-Erweiterungen definieren einen anderen Indextyp, der durch den FourCC "INDX" identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="cfabf-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="cfabf-143">Die Listen "HDRL" und "MOVI" verwenden unter Segmente für Ihre Daten.</span><span class="sxs-lookup"><span data-stu-id="cfabf-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="cfabf-144">Das folgende Beispiel zeigt das AVI-Riff-Formular, das mit den Blöcken erweitert wird, die zum Durchführen dieser Listen benötigt werden:</span><span class="sxs-lookup"><span data-stu-id="cfabf-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="cfabf-145">AVI-Haupt Header</span><span class="sxs-lookup"><span data-stu-id="cfabf-145">AVI Main Header</span></span>

<span data-ttu-id="cfabf-146">Die "HDRL"-Liste beginnt mit dem Haupt-AVI-Header, der in einem "avih"-Block enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cfabf-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="cfabf-147">Der Haupt Header enthält globale Informationen für die gesamte AVI-Datei, z. b. die Anzahl der Streams in der Datei und die Breite und Höhe der AVI-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="cfabf-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="cfabf-148">Der Haupt Header Block besteht aus einer [**avimainheader**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cfabf-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="cfabf-149">AVI-Streamheader</span><span class="sxs-lookup"><span data-stu-id="cfabf-149">AVI Stream Headers</span></span>

<span data-ttu-id="cfabf-150">Eine oder mehrere "String"-Listen folgen dem Haupt Header.</span><span class="sxs-lookup"><span data-stu-id="cfabf-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="cfabf-151">Für jeden Datenstrom ist eine "strinl"-Liste erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cfabf-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="cfabf-152">Jede "" "" "" "" "" "" "" Liste enthält Informationen zu einem Datenstrom in der Datei und muss einen Datenstrom-Header Block ("" "" "" "" "" "" "" ") und einen" "</span><span class="sxs-lookup"><span data-stu-id="cfabf-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="cfabf-153">Darüber hinaus kann eine "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "".</span><span class="sxs-lookup"><span data-stu-id="cfabf-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="cfabf-154">Der Datenstrom [**-Header Block**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) ("" "" "" "" "</span><span class="sxs-lookup"><span data-stu-id="cfabf-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="cfabf-155">Ein Datenstrom Format Block ("" "" "" "" "" "" "" "" "" "" "</span><span class="sxs-lookup"><span data-stu-id="cfabf-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="cfabf-156">Das Datenstrom Format Segment beschreibt das Format der Daten im Stream.</span><span class="sxs-lookup"><span data-stu-id="cfabf-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="cfabf-157">Die in diesem Segment enthaltenen Daten sind vom Streamtyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="cfabf-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="cfabf-158">Bei Videostreams handelt es sich bei den Informationen um eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die ggf. Paletteninformationen einschließt.</span><span class="sxs-lookup"><span data-stu-id="cfabf-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="cfabf-159">Für Audiostreams ist die Information eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cfabf-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="cfabf-160">Wenn das Datenstrom Header-Daten Segment ("Strind") vorhanden ist, folgt es dem Datenstrom Format Block.</span><span class="sxs-lookup"><span data-stu-id="cfabf-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="cfabf-161">Das Format und der Inhalt dieses Blocks werden vom Codec-Treiber definiert.</span><span class="sxs-lookup"><span data-stu-id="cfabf-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="cfabf-162">Diese Informationen werden in der Regel von Treibern für die Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfabf-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="cfabf-163">Anwendungen, die AVI-Dateien lesen und schreiben, müssen diese Informationen nicht interpretieren. Sie werden einfach als Speicherblock an den und vom Treiber übertragen.</span><span class="sxs-lookup"><span data-stu-id="cfabf-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="cfabf-164">Der optionale Abschnitt "stringenter" enthält eine auf NULL endenden Text Zeichenfolge, die den Datenstrom beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cfabf-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="cfabf-165">Die Streamheader in der HDRL-Liste sind den Datenstrom Daten in der Liste "MOVI" entsprechend der Reihenfolge der "stringenten" Blöcke zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cfabf-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="cfabf-166">Der erste "" Bereich "" "" "" "" "" "" "" "" "" ".</span><span class="sxs-lookup"><span data-stu-id="cfabf-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="cfabf-167">Streamdaten ("MOVI"-Liste)</span><span class="sxs-lookup"><span data-stu-id="cfabf-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="cfabf-168">Das Befolgen der Header Informationen ist eine "MOVI"-Liste, die die eigentlichen Daten in den Streams enthält – d. h. die Video Frames und Audiobeispiele.</span><span class="sxs-lookup"><span data-stu-id="cfabf-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="cfabf-169">Die Datenblöcke können sich direkt in der Liste "MOVI" befinden, oder Sie können in "Rec"-Listen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="cfabf-170">Die ' REC '-Gruppierung impliziert, dass die gruppierten Blöcke alle gleichzeitig vom Datenträger gelesen werden sollen, und ist für Dateien vorgesehen, die für die Wiedergabe von CD-ROM verschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="cfabf-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="cfabf-171">Der FourCC, der die einzelnen Daten Segmente identifiziert, besteht aus einer zweistelligen streamnummer, gefolgt von einem aus zwei Zeichen bestehenden Code, der den Typ der Informationen im Block definiert.</span><span class="sxs-lookup"><span data-stu-id="cfabf-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="cfabf-172">Code mit zwei Zeichen</span><span class="sxs-lookup"><span data-stu-id="cfabf-172">Two-character code</span></span> | <span data-ttu-id="cfabf-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfabf-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="cfabf-174">db</span><span class="sxs-lookup"><span data-stu-id="cfabf-174">db</span></span>                 | <span data-ttu-id="cfabf-175">Nicht komprimierter Videorahmen</span><span class="sxs-lookup"><span data-stu-id="cfabf-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="cfabf-176">dc</span><span class="sxs-lookup"><span data-stu-id="cfabf-176">dc</span></span>                 | <span data-ttu-id="cfabf-177">Komprimierter Videorahmen</span><span class="sxs-lookup"><span data-stu-id="cfabf-177">Compressed video frame</span></span>   |
| <span data-ttu-id="cfabf-178">pc</span><span class="sxs-lookup"><span data-stu-id="cfabf-178">pc</span></span>                 | <span data-ttu-id="cfabf-179">Palettenänderung</span><span class="sxs-lookup"><span data-stu-id="cfabf-179">Palette change</span></span>           |
| <span data-ttu-id="cfabf-180">WB</span><span class="sxs-lookup"><span data-stu-id="cfabf-180">wb</span></span>                 | <span data-ttu-id="cfabf-181">Audiodaten</span><span class="sxs-lookup"><span data-stu-id="cfabf-181">Audio data</span></span>               |



 

<span data-ttu-id="cfabf-182">Wenn Stream 0 z. b. Audiodaten enthält, haben die Datenblöcke für diesen Stream den FourCC "00wb".</span><span class="sxs-lookup"><span data-stu-id="cfabf-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="cfabf-183">Wenn Stream 1 Video enthält, haben die Datenblöcke für diesen Stream den FourCC "01dB" oder "01dc".</span><span class="sxs-lookup"><span data-stu-id="cfabf-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="cfabf-184">Mit Video Datenblöcken können auch neue Paletteneinträge definiert werden, um die Palette während einer AVI-Sequenz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfabf-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="cfabf-185">Jeder palettenänderungs Block (' xxpc ') enthält eine [**avipalchange**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cfabf-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="cfabf-186">Wenn ein Stream Palettenänderungen enthält, legen Sie das **avisf \_ Video \_ palchanges** -Flag im **dwFlags** -Member der [**avistreamheader**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) -Struktur für diesen Stream fest.</span><span class="sxs-lookup"><span data-stu-id="cfabf-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="cfabf-187">Textstreams können beliebige zwei Zeichen Codes verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="cfabf-188">AVI-Index Einträge</span><span class="sxs-lookup"><span data-stu-id="cfabf-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="cfabf-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1,0-Index</span><span class="sxs-lookup"><span data-stu-id="cfabf-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="cfabf-190">Ein optionaler Index (' idx1 ') kann der Liste ' MOVI ' folgen.</span><span class="sxs-lookup"><span data-stu-id="cfabf-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="cfabf-191">Der Index enthält eine Liste der Datenblöcke und deren Speicherort in der Datei.</span><span class="sxs-lookup"><span data-stu-id="cfabf-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="cfabf-192">Sie besteht aus einer [**avioldindex**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) -Struktur mit Einträgen für jeden Datenblock, einschließlich ' REC '-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="cfabf-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="cfabf-193">Wenn die Datei einen Index enthält, legen Sie das **avif \_ HasIndex** -Flag im **dwFlags** -Member der [**avimainheader**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="cfabf-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cfabf-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2,0-Index</span><span class="sxs-lookup"><span data-stu-id="cfabf-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="cfabf-195">Ein AVI 2,0-Index kann als einzelner Block angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="cfabf-196">Alternativ können Index Segmente innerhalb des Abschnitts "MOVI" verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="cfabf-197">Wenn die Index Segmente in den Block "MOVI" eingefügt werden, enthält ein Superindex einen Index der Index Segmente.</span><span class="sxs-lookup"><span data-stu-id="cfabf-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="cfabf-198">Die [**avimetaindex**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) -Struktur ist die Basis Struktur sowohl für die Index Segmente als auch für den Super Index.</span><span class="sxs-lookup"><span data-stu-id="cfabf-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="cfabf-199">Weitere Informationen finden Sie in den *OpenDML AVI-Dateiformat Erweiterungen*, die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="cfabf-200">(Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="cfabf-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="cfabf-201">Andere Datenblöcke</span><span class="sxs-lookup"><span data-stu-id="cfabf-201">Other Data Chunks</span></span>

<span data-ttu-id="cfabf-202">Daten können in einer AVI-Datei durch Einfügen von "Junk"-Blöcken nach Bedarf ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="cfabf-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="cfabf-203">Anwendungen sollten den Inhalt eines "Junk"-Blocks ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cfabf-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfabf-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cfabf-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfabf-205">AVI-Datei Format</span><span class="sxs-lookup"><span data-stu-id="cfabf-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
