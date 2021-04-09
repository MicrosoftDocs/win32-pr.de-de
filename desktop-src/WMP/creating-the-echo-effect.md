---
title: Erstellen des Echo Effekts
description: Erstellen des Echo Effekts
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Plug-in-Beispiel für ECHO DSP, Erstellen eines ECHO Effekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036400"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="b741f-109">Erstellen des Echo Effekts</span><span class="sxs-lookup"><span data-stu-id="b741f-109">Creating the Echo Effect</span></span>

<span data-ttu-id="b741f-110">Sie müssen zunächst den Code aus dem Assistenten Beispiel entfernen, der die Audiodatei skaliert.</span><span class="sxs-lookup"><span data-stu-id="b741f-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="b741f-111">Entfernen Sie den folgenden Code aus dem 8-Bit-Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="b741f-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="b741f-112">(Denken Sie daran, dass m "m" \_ durch m \_ dwdelta-Time ersetzt wurde.)</span><span class="sxs-lookup"><span data-stu-id="b741f-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="b741f-113">Entfernen Sie den folgenden Code aus dem 16-Bit-Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="b741f-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="b741f-114">Die im Beispielcode des Plug-in-Assistenten bereitgestellte Implementierung von " **DoProcess Output** " erstellt eine while-Schleife, die ein Mal für jedes Beispiel im von Windows Media Player bereitgestellten Eingabepuffer iteriert.</span><span class="sxs-lookup"><span data-stu-id="b741f-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="b741f-115">Diese Schleife funktioniert auf die gleiche Weise für 8-Bit-und 16-Bit-Audiodaten, obwohl jeweils eine separate Schleife erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b741f-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="b741f-116">In jedem Fall wird die Schleife mit folgendem Test initiiert:</span><span class="sxs-lookup"><span data-stu-id="b741f-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="b741f-117">In der Schleife sind die Verarbeitungs Routinen für 8-Bit-und 16-Bit-Audiodaten sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="b741f-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="b741f-118">Der Hauptunterschied besteht darin, dass der Code im 8-Bit-Abschnitt den Bereich der Datenwerte in-128 bis 127 ändert und dann den Bereich wieder zurück konvertiert, bevor die Daten in den Ausgabepuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b741f-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="b741f-119">Dies ist wichtig, um die Symmetrie des Audiowellen Formulars während der Verarbeitung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b741f-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="b741f-120">Nun können Sie beginnen, Code in der Verarbeitungs Schleife hinzuzufügen und zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b741f-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="b741f-121">Abrufen eines Beispiels aus dem Eingabepuffer</span><span class="sxs-lookup"><span data-stu-id="b741f-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="b741f-122">Während jeder Iterationen der Schleife wird eine einzelne Stichprobe aus dem Eingabepuffer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b741f-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="b741f-123">Für 8-Bit-Audiodaten wird das Beispiel in den neuen Bereich verschoben, und der Zeiger auf den Eingabepuffer wird auf das nächste Beispiel erweitert.</span><span class="sxs-lookup"><span data-stu-id="b741f-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="b741f-124">Der folgende Code wird vom Plug-in-Assistenten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b741f-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="b741f-125">Bei einem 16-Bit-audiovorgang ist der Prozess mit Ausnahme der Normalisierung identisch:</span><span class="sxs-lookup"><span data-stu-id="b741f-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="b741f-126">Beachten Sie, dass die Zeiger im 16-Bit-Code in den Typ **Short** konvertiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b741f-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="b741f-127">Abrufen eines Beispiels aus dem Verzögerungs Puffer</span><span class="sxs-lookup"><span data-stu-id="b741f-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="b741f-128">Rufen Sie als nächstes eine einzelne Stichprobe aus dem verzögerten Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="b741f-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="b741f-129">Für 8-Bit-Code werden die Verzögerungs Proben in ihrem nativen Bereich von 0 bis 255 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b741f-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="b741f-130">Der folgende Code, den Sie hinzufügen müssen, Ruft ein 8-Bit-Verzögerungs Beispiel ab:</span><span class="sxs-lookup"><span data-stu-id="b741f-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="b741f-131">Bei einem 16-Bit-audiovorgang ist der Prozess ähnlich:</span><span class="sxs-lookup"><span data-stu-id="b741f-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="b741f-132">Eingabe Beispiel in den Verzögerungs Puffer schreiben</span><span class="sxs-lookup"><span data-stu-id="b741f-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="b741f-133">Nun müssen Sie das Eingabe Beispiel im Verzögerungs Puffer an dem Speicherort speichern, von dem aus Sie das Verzögerungs Beispiel abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="b741f-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="b741f-134">Im folgenden finden Sie den Code, den Sie für 8-Bit-Audiodaten hinzufügen müssen:</span><span class="sxs-lookup"><span data-stu-id="b741f-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="b741f-135">Dies ist der Code, der für den 16-Bit-Abschnitt hinzugefügt werden soll:</span><span class="sxs-lookup"><span data-stu-id="b741f-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="b741f-136">Verschieben des Verzögerungs Puffer Zeigers</span><span class="sxs-lookup"><span data-stu-id="b741f-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="b741f-137">Nachdem die Arbeit im Verzögerungs Puffer für diese Iterationen abgeschlossen ist, können Sie den verschiebbaren Zeiger auf den Verzögerungs Puffer verschieben.</span><span class="sxs-lookup"><span data-stu-id="b741f-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="b741f-138">Wenn der Zeiger das Ende des Kreis Puffers erreicht, müssen Sie seinen Wert ändern, um auf den Anfang des Puffers zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="b741f-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="b741f-139">Um dies für 8-Bit-Audiodaten zu erreichen, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="b741f-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="b741f-140">Dies ist der Code für den 16-Bit-Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="b741f-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="b741f-141">Da der Zeiger im 16-Bit-Abschnitt wirklich eine Kopie der Element Variablen ist, müssen Sie daran denken, den Wert in der Element Variablen mit der neuen Adresse zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b741f-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="b741f-142">Wenn Sie dies nicht tun, zeigt der Verzögerungs Puffer Zeiger wiederholt auf den Anfang des Puffers, und Ihr Echo Effekt funktioniert nicht erwartungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b741f-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="b741f-143">Fügen Sie dem 16-Bit-Abschnitt den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="b741f-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="b741f-144">Mischen der Eingabe Stichprobe mit dem Delay-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b741f-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="b741f-145">Hier verwenden Sie die Werte für "nass Mischung" und "Dry Mix", um das abschließende Ausgabe Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b741f-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="b741f-146">Sie multiplizieren einfach jede Stichprobe mit dem Gleit Komma Wert, der den Prozentsatz des endgültigen Signals für das Beispiel darstellt.</span><span class="sxs-lookup"><span data-stu-id="b741f-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="b741f-147">Multiplizieren Sie die Eingabe Stichprobe mit dem Wert, der in m-Datei- \_ Mischungs Mischung gespeichert ist, Multiplizieren Sie das Verzögerungs Beispiel mit dem in m "m" \_ .</span><span class="sxs-lookup"><span data-stu-id="b741f-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="b741f-148">Fügen Sie dann die beiden Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="b741f-148">Then, add the two values.</span></span> <span data-ttu-id="b741f-149">Der Code, den Sie hinzufügen müssen, ist für die 8-Bit-und 16-Bit-Abschnitte identisch:</span><span class="sxs-lookup"><span data-stu-id="b741f-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="b741f-150">Schreiben der Daten in den Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="b741f-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="b741f-151">Kopieren Sie schließlich das gemischte Beispiel in den Ausgabepuffer, und fahren Sie dann mit dem Ausgabepuffer Zeiger fort.</span><span class="sxs-lookup"><span data-stu-id="b741f-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="b741f-152">Für 8-Bit-Audiodaten verwendet der Plug-in-Assistent den folgenden Code, um das Beispiel in seinen ursprünglichen Bereich zurückzusetzen:</span><span class="sxs-lookup"><span data-stu-id="b741f-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="b741f-153">Für 16-Bit-Audiodaten verwendet der Assistent den folgenden Code als letzten Schritt in der Verarbeitungs Schleife:</span><span class="sxs-lookup"><span data-stu-id="b741f-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="b741f-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b741f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b741f-155">**Implementieren von Cecho::D oprocess Output**</span><span class="sxs-lookup"><span data-stu-id="b741f-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




