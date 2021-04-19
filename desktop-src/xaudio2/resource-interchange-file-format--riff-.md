---
description: In dieser Übersicht wird das in WAV-Dateien verwendete Ressourcenaustausch Datei Format (-Riff) beschrieben. "Riff" ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Resource Interchange File Format (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363785"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="9e51c-104">Resource Interchange File Format (RIFF)</span><span class="sxs-lookup"><span data-stu-id="9e51c-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="9e51c-105">In dieser Übersicht wird das in WAV-Dateien verwendete Ressourcenaustausch Datei Format (-Riff) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9e51c-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="9e51c-106">"Riff" ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9e51c-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="9e51c-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="9e51c-107">RIFF</span></span>

<span data-ttu-id="9e51c-108">Eine Riff Datei besteht aus mehreren diskreten Abschnitten von Daten, die als *Blöcke bezeichnet werden*.</span><span class="sxs-lookup"><span data-stu-id="9e51c-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="9e51c-109">FourCC-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9e51c-109">FOURCC Identifiers</span></span>

<span data-ttu-id="9e51c-110">Der Typ der Daten in einem Block wird durch einen vierstelligen Code (FourCC) angegeben.</span><span class="sxs-lookup"><span data-stu-id="9e51c-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="9e51c-111">Ein FourCC ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen, die zum Identifizieren von Segmenttypen in einer Riff Datei verwendet werden, erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9e51c-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="9e51c-112">Beispielsweise wird das FourCC "abcd" in einem Little-in-System als 0x64636261 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="9e51c-113">Fourccs kann Leerzeichen enthalten, sodass "ABC" ein gültiges FourCC ist.</span><span class="sxs-lookup"><span data-stu-id="9e51c-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="9e51c-114">Audiodateien verwenden FOURCC-Codes, um audioformatblöcke, Audiodatenblöcke und andere Segmente zu identifizieren, die für das Audioformat spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="9e51c-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="9e51c-115">Die folgende Tabelle zeigt die FourCC-IDs, die in den von XAudio2 unterstützten Audioformaten erwartet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e51c-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="9e51c-116">Format</span><span class="sxs-lookup"><span data-stu-id="9e51c-116">Format</span></span> | <span data-ttu-id="9e51c-117">FourCC-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9e51c-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="9e51c-118">Zusätzliche Informationen</span><span class="sxs-lookup"><span data-stu-id="9e51c-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e51c-119">PCM</span><span class="sxs-lookup"><span data-stu-id="9e51c-119">PCM</span></span>    | <span data-ttu-id="9e51c-120">"Riff", "f", "Data"</span><span class="sxs-lookup"><span data-stu-id="9e51c-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="9e51c-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="9e51c-121">ADPCM</span></span>  | <span data-ttu-id="9e51c-122">"Riff", "f", "Data", "SMPL", "wsmpl"</span><span class="sxs-lookup"><span data-stu-id="9e51c-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="9e51c-123">Eine Beschreibung der ADPCM-spezifischen FourCC-IDs finden Sie unter [Übersicht über ADPCM](adpcm-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="9e51c-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="9e51c-124">Die FourCC-IDs "Riff", "fmt" und "Data" sind für alle unterstützten Formate üblich.</span><span class="sxs-lookup"><span data-stu-id="9e51c-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="9e51c-125">In der folgenden Tabelle werden die FourCC-IDs beschrieben, die in allen unterstützten Formaten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="9e51c-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="9e51c-126">FourCC-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9e51c-126">FOURCC identifier</span></span> | <span data-ttu-id="9e51c-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e51c-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e51c-128">„RIFF“</span><span class="sxs-lookup"><span data-stu-id="9e51c-128">"RIFF"</span></span>            | <span data-ttu-id="9e51c-129">Der Standard-Riff Block, der einen Dateityp mit dem Wert "Wave" oder "xwma" in den ersten vier Bytes des Daten Abschnitts und die anderen Blöcke in der Datei im Rest des Daten Abschnitts enthält.</span><span class="sxs-lookup"><span data-stu-id="9e51c-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="9e51c-130">„fmt“</span><span class="sxs-lookup"><span data-stu-id="9e51c-130">"fmt"</span></span>             | <span data-ttu-id="9e51c-131">Enthält den Format Header für die Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="9e51c-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="9e51c-132">Die Daten in diesem Block entsprechen einer der folgenden Strukturen: **WaveFormatEx**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span><span class="sxs-lookup"><span data-stu-id="9e51c-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="9e51c-133">„data“</span><span class="sxs-lookup"><span data-stu-id="9e51c-133">"data"</span></span>            | <span data-ttu-id="9e51c-134">Enthält Audiodaten für die Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="9e51c-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="9e51c-135">In XAudio2 wird der Inhalt des Datensegments in einen Puffer eingelesen und als **paudiodata** -Member einer [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur an eine Quell Stimme übergeben.</span><span class="sxs-lookup"><span data-stu-id="9e51c-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="9e51c-136">Chunks</span><span class="sxs-lookup"><span data-stu-id="9e51c-136">Chunks</span></span>

<span data-ttu-id="9e51c-137">Eine Riff Datei besteht aus einem Riff Block, der 0 (null) oder mehr andere Blöcke enthält.</span><span class="sxs-lookup"><span data-stu-id="9e51c-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="9e51c-138">Der Riff Block weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="9e51c-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="9e51c-139">"Riff", Filesize, filetype, Data</span><span class="sxs-lookup"><span data-stu-id="9e51c-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="9e51c-140">Wenn "Riff" der Literale FourCC-Code "Riff" ist, ist *FileSize* ein 4-Byte-Wert, der die Größe der Daten in der Datei angibt, und *filetype* ist ein FourCC, der den spezifischen Dateityp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9e51c-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="9e51c-141">Der Wert von *FileSize* umfasst die Größe von *filetype* FourCC plus die Größe der nachfolgenden Daten, jedoch nicht die Größe des "Riff"-FourCC oder die Größe der *Dateigröße*.</span><span class="sxs-lookup"><span data-stu-id="9e51c-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="9e51c-142">Die Daten bestehen aus Blöcken in beliebiger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e51c-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="9e51c-143">Andere Blöcke weisen die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="9e51c-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="9e51c-144">Wenn " *segkid* " ein FourCC ist, das die im Block enthaltenen Daten identifiziert, ist " *ChunkSize* " ein 4-Byte-Wert, der die Größe des Abschnitts "Data" des Blocks angibt, und die Daten sind 0 (null) oder mehr Bytes an Daten.</span><span class="sxs-lookup"><span data-stu-id="9e51c-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="9e51c-145">Die Daten werden immer bis zur nächsten Wort Grenze aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="9e51c-146">*ChunkSize* gibt die Größe der gültigen Daten im Block an.</span><span class="sxs-lookup"><span data-stu-id="9e51c-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="9e51c-147">Es enthält keine Auffüll Zeichen, die Größe von *segbrocken* oder die Größe von Block *Größe*.</span><span class="sxs-lookup"><span data-stu-id="9e51c-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e51c-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e51c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e51c-149">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="9e51c-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="9e51c-150">So wird's gemacht: Wiedergeben von Ton mit XAudio2</span><span class="sxs-lookup"><span data-stu-id="9e51c-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="9e51c-151">XAudio2-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="9e51c-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



