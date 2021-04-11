---
title: Funktionsweise des Audiokomprimierungs-Managers
description: Funktionsweise des Audiokomprimierungs-Managers
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- Multimedia-Audiodatei, Audiokomprimierungs-Manager (ACM)
- Audiokomprimierung, Audiokomprimierungs-Manager (ACM)
- Audiokomprimierungs-Manager (ACM), Informationen zu
- ACM (Audiokomprimierungs-Manager), Informationen zu
- Audiokomprimierungs-Manager (ACM), Codec-Treiber
- ACM (Audiokomprimierungs-Manager), Codec-Treiber
- Audiokomprimierungs-Manager (ACM), Format Konverter-Treiber
- ACM (Audiokomprimierungs-Manager), Format Konverter-Treiber
- Audiokomprimierungs-Manager (ACM), Filtertreiber
- ACM (Audiokomprimierungs-Manager), Filtertreiber
- Audiokomprimierungs-Manager (ACM), Kompressor-Treiber
- ACM (Audiokomprimierungs-Manager), Kompressor-Treiber
- Audiokomprimierungs-Manager (ACM), Debug-Treiber
- ACM (Audiokomprimierungs-Manager), Debug-Treiber
- Codec-Treiber
- Konvertieren von konvertertreibern
- Filtertreiber
- Kompressor-Treiber
- Debug-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310340"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="ef543-122">Funktionsweise des Audiokomprimierungs-Managers</span><span class="sxs-lookup"><span data-stu-id="ef543-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="ef543-123">Der ACM verwendet vorhandene Treiber Schnittstellen Hooks, um den standardmäßigen Mapping-Algorithmus für Waveform-Audiogeräte zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ef543-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="ef543-124">Dadurch kann das ACM Geräte offene Aufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="ef543-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="ef543-125">Nachdem ein-Rückruf abgefangen wurde, kann das ACM eine Reihe von Aufgaben zum Verarbeiten der Audiodaten ausführen, z. b. das Einfügen eines externen Kompressors oder dekompressors in die Sequenz.</span><span class="sxs-lookup"><span data-stu-id="ef543-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="ef543-126">Das ACM verwaltet die folgenden Treiber Typen:</span><span class="sxs-lookup"><span data-stu-id="ef543-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="ef543-127">Kompressor-und Debug-Treiber (Codec)</span><span class="sxs-lookup"><span data-stu-id="ef543-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="ef543-128">Konvertieren von konvertertreibern</span><span class="sxs-lookup"><span data-stu-id="ef543-128">Format converter drivers</span></span>
-   <span data-ttu-id="ef543-129">Filter Treiber</span><span class="sxs-lookup"><span data-stu-id="ef543-129">Filter drivers</span></span>

<span data-ttu-id="ef543-130">-Kompressoren und-Dekompressoren ändern einen Formattyp in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="ef543-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="ef543-131">Beispielsweise kann ein Kompressor oder Dekompressor eine PCM-Datei (Pulse Code-Modulation) in eine ADPCM-Datei (Adaptive Differential Pulse Code Modulation) ändern.</span><span class="sxs-lookup"><span data-stu-id="ef543-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="ef543-132">Format Konverter ändern das Format, jedoch nicht den Datentyp.</span><span class="sxs-lookup"><span data-stu-id="ef543-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="ef543-133">Ein Konverter kann z. b. 44-kHz-16-Bit-Daten in 44-kHz-, 8-Bit-Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="ef543-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="ef543-134">Filter ändern das Datenformat überhaupt nicht, aber Sie ändern die Wellenform-Audiodaten auf irgendeine Weise.</span><span class="sxs-lookup"><span data-stu-id="ef543-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="ef543-135">Beispielsweise könnte ein Filter einen Datenstrom und ein Echo von sich selbst kombinieren.</span><span class="sxs-lookup"><span data-stu-id="ef543-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="ef543-136">Ein einzelner ACM-Treiber oder ein Filtertag oder ein Formattag innerhalb eines Treibers unterstützt möglicherweise auch Kombinationen der vorangehenden Typen.</span><span class="sxs-lookup"><span data-stu-id="ef543-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="ef543-137">Bei der Waveform-Audioausgabe übergibt das ACM jeden Puffer von Daten an den Konverter, sobald er eintrifft.</span><span class="sxs-lookup"><span data-stu-id="ef543-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="ef543-138">Der Konverter zerlegt die Daten und gibt die entkomprimierten Daten an das ACM in einem "Shadow"-Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="ef543-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="ef543-139">Das ACM übergibt dann den entkomprimierten Schatten Puffer an den Waveform-Audiotreiber.</span><span class="sxs-lookup"><span data-stu-id="ef543-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="ef543-140">Das ACM ordnet die Schatten Puffer an, wenn eine Vorbereitungs Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ef543-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="ef543-141">Bei der Waveform-Audioeingabe übergibt das ACM leere Schatten Puffer an den Treiber.</span><span class="sxs-lookup"><span data-stu-id="ef543-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="ef543-142">Er verwendet einen Hintergrund Task, um eine Benachrichtigung zu erhalten, nachdem der Treiber den Schatten Puffer ausgefüllt hat.</span><span class="sxs-lookup"><span data-stu-id="ef543-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="ef543-143">Der ACM übergibt die Puffer dann zur Komprimierung an den Treiber.</span><span class="sxs-lookup"><span data-stu-id="ef543-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="ef543-144">Nachdem die Komprimierung abgeschlossen ist, übergibt der Treiber die Daten an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ef543-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




