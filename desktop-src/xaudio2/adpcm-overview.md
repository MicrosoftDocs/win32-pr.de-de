---
description: Bei Adaptive Differential Pulse Code Modulation (ADPCM) handelt es sich um ein Ersetztes Komprimierungs Format, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks bereitzustellen.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Übersicht über ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358574"
---
# <a name="adpcm-overview"></a><span data-ttu-id="91cab-103">Übersicht über ADPCM</span><span class="sxs-lookup"><span data-stu-id="91cab-103">ADPCM Overview</span></span>

<span data-ttu-id="91cab-104">Bei Adaptive Differential Pulse Code Modulation (ADPCM) handelt es sich um ein Ersetztes Komprimierungs Format, das für XAudio2 implementiert wird, um zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="91cab-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="91cab-105">Bei einem Verlust behafchten Komprimierungs Format werden einige Daten während der Komprimierung geändert und verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="91cab-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="91cab-106">Für ADPCM können Komprimierungs Verhältnisse von bis zu 4:1 erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="91cab-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="91cab-107">Die Implementierung von ADPCM für XAudio2 bietet zusätzliche Features zum Angeben der Größe des Komprimierungs Beispiel Blocks.</span><span class="sxs-lookup"><span data-stu-id="91cab-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="91cab-108">Mit ADPCM kann der audiodesigner eine Einstellung auswählen, die eine angemessene Gefährdung zwischen Größe, Qualität und Auflösung darstellt (zum Platzieren von Schleifen Punkten).</span><span class="sxs-lookup"><span data-stu-id="91cab-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="91cab-109">XAudio2 verwendet eine geänderte Version des Microsoft ADPCM-Codecs, die die erweiterte Datenformatierung unterstützt, die zum Bereitstellen von benutzerdefinierten Beispiel Blockgrößen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="91cab-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="91cab-110">Aus diesem Grund können XAudio2-Audiodaten nicht von Audiomodulen abgespielt werden, die diese Version des ADPCM-Codecs nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="91cab-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="91cab-111">Derzeit ist die ADPCM-Komprimierung nur für Windows verfügbar, einschließlich XNA Game Studio Express für Windows-bereit Stellungen.</span><span class="sxs-lookup"><span data-stu-id="91cab-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="91cab-112">ADPCM-Codierung</span><span class="sxs-lookup"><span data-stu-id="91cab-112">ADPCM Encoding</span></span>

<span data-ttu-id="91cab-113">Audiodaten werden mit dem Befehlszeilen Tool adpcmencode in ADPCM codiert.</span><span class="sxs-lookup"><span data-stu-id="91cab-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="91cab-114">Adpcmencode</span><span class="sxs-lookup"><span data-stu-id="91cab-114">AdpcmEncode</span></span>

    <span data-ttu-id="91cab-115">Verwenden Sie das Befehlszeilen Tool **adpcmencode** , um Audiodateien als ADPCM für die Verwendung mit XAudio2 zu codieren.</span><span class="sxs-lookup"><span data-stu-id="91cab-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="91cab-116">ADPCM-Decodierung</span><span class="sxs-lookup"><span data-stu-id="91cab-116">ADPCM Decoding</span></span>

<span data-ttu-id="91cab-117">Software Decodierung von ADPCM wird in XAudio2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91cab-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="91cab-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="91cab-118">XAudio2</span></span>

    <span data-ttu-id="91cab-119">Um ADPCM-codierte Daten in XAudio2 zu verwenden, müssen Sie eine **ADPCMWAVEFORMAT** -Struktur mit ADPCM-spezifischen Werten initialisieren und Sie als Argument an [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) übergeben, wenn Sie eine Quellsprache erstellen.</span><span class="sxs-lookup"><span data-stu-id="91cab-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="91cab-120">Ein Beispiel für das Laden und Wiedergeben eines Sounds in XAudio2 finden [Sie unter Gewusst wie: Wiedergabe eines Sounds mit XAudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="91cab-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="91cab-121">Samplesperblock</span><span class="sxs-lookup"><span data-stu-id="91cab-121">SamplesPerBlock</span></span>

<span data-ttu-id="91cab-122">Die ADPCM-Komprimierung funktioniert, indem Sie die Wellenform in Blöcke aufteilen und die Variation der Wellenform-Beispiele in jedem Block Vorhersagen.</span><span class="sxs-lookup"><span data-stu-id="91cab-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="91cab-123">Die Größe der Blöcke wird in den Beispielen gemessen.</span><span class="sxs-lookup"><span data-stu-id="91cab-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="91cab-124">Die kleinste Blockgröße ist 32 Samples, und die höchste ist 512 Stichproben.</span><span class="sxs-lookup"><span data-stu-id="91cab-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="91cab-125">Größere Blöcke ermöglichen eine bessere Komprimierung, was zu kleineren Dateigrößen führt, aber auf Kosten der Ton Qualität und-Auflösung für das Ausrichten von Schleifen Punkten.</span><span class="sxs-lookup"><span data-stu-id="91cab-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="91cab-126">Im Allgemeinen führt das Ändern des samplesperblock-Werts zu diesen vor-und Nachteile:</span><span class="sxs-lookup"><span data-stu-id="91cab-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="91cab-127">Wenn samplesperblock...</span><span class="sxs-lookup"><span data-stu-id="91cab-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="91cab-128">Dateikomprimierung</span><span class="sxs-lookup"><span data-stu-id="91cab-128">File Compression</span></span> | <span data-ttu-id="91cab-129">Sound Qualität</span><span class="sxs-lookup"><span data-stu-id="91cab-129">Sound Quality</span></span> | <span data-ttu-id="91cab-130">Schleifen Punkt Auflösung</span><span class="sxs-lookup"><span data-stu-id="91cab-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="91cab-131">Erhöht (max. 512)</span><span class="sxs-lookup"><span data-stu-id="91cab-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="91cab-132">Erhöht</span><span class="sxs-lookup"><span data-stu-id="91cab-132">Increases</span></span>        | <span data-ttu-id="91cab-133">Ticks</span><span class="sxs-lookup"><span data-stu-id="91cab-133">Decreases</span></span>     | <span data-ttu-id="91cab-134">Ticks</span><span class="sxs-lookup"><span data-stu-id="91cab-134">Decreases</span></span>             |
| <span data-ttu-id="91cab-135">Wird verringert (bis zu min. 32)</span><span class="sxs-lookup"><span data-stu-id="91cab-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="91cab-136">Ticks</span><span class="sxs-lookup"><span data-stu-id="91cab-136">Decreases</span></span>        | <span data-ttu-id="91cab-137">Erhöht</span><span class="sxs-lookup"><span data-stu-id="91cab-137">Increases</span></span>     | <span data-ttu-id="91cab-138">Erhöht</span><span class="sxs-lookup"><span data-stu-id="91cab-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="91cab-139">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="91cab-139">Restrictions</span></span>

<span data-ttu-id="91cab-140">Da ADPCM Beispiel Blöcke verwendet, die nacheinander ausgerichtet sind, kann eine mit ADPCM komprimierte Welle einen nicht abgeschlossenen, partiellen Block am Ende haben.</span><span class="sxs-lookup"><span data-stu-id="91cab-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="91cab-141">Der ADPCM-Decoder generiert Ruhe für den Rest dieses partiellen Blocks, wodurch die Wellen Schleife nahtlos verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="91cab-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="91cab-142">Der Wert des *samplesperblock* -Parameters wirkt sich auf die Auflösung aus, mit der Sie wellendaten und Schleifenpunkte ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="91cab-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="91cab-143">Wenn Sie versuchen, die Komprimierung auf eine nicht ausgerichtete Welle anzuwenden, erhalten Sie eine Fehlermeldung oder eine Warnung, je nachdem, ob die Welle in Schleifen Wiedergabe Ereignissen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91cab-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="91cab-144">Es ist nicht möglich, eine Welle zu komprimieren, die in Schleifen Wiedergabe Ereignissen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91cab-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="91cab-145">Entfernen Sie Sie aus den Schleifen Wiedergabe Ereignissen, und wenden Sie die Komprimierung erneut an.</span><span class="sxs-lookup"><span data-stu-id="91cab-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="91cab-146">Wenn Sie die-Welle ausschließlich im nicht-Schleifen Modus verwenden, gilt die Einschränkung der Beispiel Block Ausrichtung nicht.</span><span class="sxs-lookup"><span data-stu-id="91cab-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="91cab-147">ADPCM-Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="91cab-147">ADPCM File Structure</span></span>

<span data-ttu-id="91cab-148">Eine ADPCM-Datei ist eine Standard-Riff Datei mit den folgenden Blocktypen.</span><span class="sxs-lookup"><span data-stu-id="91cab-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="91cab-149">Block FCC</span><span class="sxs-lookup"><span data-stu-id="91cab-149">Chunk FCC</span></span>     | <span data-ttu-id="91cab-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91cab-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91cab-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="91cab-151">RIFF</span></span>          | <span data-ttu-id="91cab-152">Der Standard-Riff Block, der einen Dateityp mit dem Wert Wave in den ersten vier Bytes seines Daten Abschnitts und die anderen Blöcke in der Datei im Rest des Daten Abschnitts enthält.</span><span class="sxs-lookup"><span data-stu-id="91cab-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="91cab-153">fmt</span><span class="sxs-lookup"><span data-stu-id="91cab-153">fmt</span></span>           | <span data-ttu-id="91cab-154">Enthält den Format Header der ADPCM-Datei.</span><span class="sxs-lookup"><span data-stu-id="91cab-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="91cab-155">Die Daten in diesem Block entsprechen einer **ADPCMWAVEFORMAT** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="91cab-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="91cab-156">Daten</span><span class="sxs-lookup"><span data-stu-id="91cab-156">data</span></span>          | <span data-ttu-id="91cab-157">Enthält die codierten ADPCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="91cab-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="91cab-158">Wenn Sie ADPCM in XAudio2 verwenden, müssen Sie den Inhalt des Datensegments in einem Puffer lesen und als **paudiodata** -Member einer [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur an eine Quell Stimme übergeben.</span><span class="sxs-lookup"><span data-stu-id="91cab-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="91cab-159">Sie müssen den Inhalt des Datensegments nicht in Byte austauschen.</span><span class="sxs-lookup"><span data-stu-id="91cab-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="91cab-160">SMPL und wsmp</span><span class="sxs-lookup"><span data-stu-id="91cab-160">smpl and wsmp</span></span> | <span data-ttu-id="91cab-161">Optionale Blocktypen, die die Schleifen Informationen für die ADPCM-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="91cab-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="91cab-162">Wenn Sie ADPCM in XAudio2 verwenden, werden die in den SMPL-oder wsmp-Blöcken enthaltenen Werte verwendet, um die **loopbeginlooplength** -und **loopCount** -Elemente der [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="91cab-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="91cab-163">Auf der Xbox 360 müssen Sie die aus einem SMPL-Block geladenen Daten in Byte austauschen, um den Byte Reihenfolge-Unterschied zwischen Windows und Xbox 360 zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="91cab-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91cab-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91cab-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91cab-165">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="91cab-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
