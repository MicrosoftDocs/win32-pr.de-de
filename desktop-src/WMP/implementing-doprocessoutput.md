---
title: Implementieren von DoProcess Output
description: Implementieren von DoProcess Output
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, DoProcess Output
- DSP-Plug-ins, DoProcess Output
- audiodsp-Plug-ins, DoProcess Output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388418"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="7900b-108">Implementieren von DoProcess Output</span><span class="sxs-lookup"><span data-stu-id="7900b-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="7900b-109">Um Audiodaten zu verarbeiten, müssen Sie in " **DoProcess Output**" mehrere Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7900b-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="7900b-110">In den folgenden Schritten wird der Beispielcode des Plug-in-Assistenten als Beispiele verwendet.</span><span class="sxs-lookup"><span data-stu-id="7900b-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="7900b-111">Wenn Sie ein audiodsp-Plug-in erstellen möchten, das Medieninhalte desselben Typs verarbeitet, den der Plug-in-Assistent für den Beispielcode verwendet, müssen Sie nur den eigentlichen Verarbeitungs Code ändern, auf den in Schritt 6 verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7900b-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="7900b-112">Im folgenden werden alle in " **DoProcess Output**" implementierten Schritte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="7900b-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="7900b-113">Wenn das Plug-in derzeit nicht aktiviert ist, kopieren Sie die Daten einfach unverändert in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="7900b-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="7900b-114">Wenn das Plug-in die Daten in ein anderes Format konvertiert, müssen Sie die Konvertierungs Verarbeitung auch hier durchführen.</span><span class="sxs-lookup"><span data-stu-id="7900b-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="7900b-115">Rufen Sie einen Zeiger auf die Eingabe Formatstruktur ab.</span><span class="sxs-lookup"><span data-stu-id="7900b-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="7900b-116">Sie müssen Elementdaten aus dieser Struktur abrufen, also kopieren Sie den Zeiger von *m \_ mtinput*.**pbformat** in eine lokale Zeiger Variable eines Typs, der mit dem Format Strukturtyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7900b-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="7900b-117">Im folgenden Beispiel wird ein Zeiger auf eine **WaveFormatEx** -Eingabe Formatstruktur gespeichert:</span><span class="sxs-lookup"><span data-stu-id="7900b-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="7900b-118">Berechnen Sie die Anzahl der zu verarbeitenden Stichproben.</span><span class="sxs-lookup"><span data-stu-id="7900b-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="7900b-119">Der Beispielcode, den der Plug-in-Assistent generiert, führt diesen Schritt aus, indem die Anzahl der zu verarbeitenden Bytes durch das **nBlockAlign** -Element der Struktur des WaveFormatEx-Eingabe Formats dividiert und das Ergebnis dann mit der Anzahl der Kanäle multipliziert wird, die im **nchannels** -Member gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="7900b-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="7900b-120">Das folgende Beispiel zeigt den Beispielcode des Plug-in-Assistenten:</span><span class="sxs-lookup"><span data-stu-id="7900b-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="7900b-121">Legen Sie die Bittiefe der Audiodatei fest.</span><span class="sxs-lookup"><span data-stu-id="7900b-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="7900b-122">Der Beispielcode des Plug-in-Assistenten bestimmt eine 8-Bit-oder 16-Bit-Audiodatei, indem der **wbitspersample** -Member der **WaveFormatEx** -Struktur überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="7900b-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="7900b-123">Anschließend wird dieser Wert in einer Switch-Anweisung verwendet, um separate Verarbeitungs Routinen für jede Bittiefe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7900b-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="7900b-124">Möglicherweise müssen Sie eine andere Methode verwenden, wenn Sie mit anderen Format Typen und Bittiefen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7900b-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="7900b-125">Erstellen Sie eine-Schleife, um die Audiobeispiele im Eingabepuffer schrittweise zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="7900b-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="7900b-126">Rufen Sie ein Beispiel aus dem Eingabepuffer ab.</span><span class="sxs-lookup"><span data-stu-id="7900b-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="7900b-127">Dazu Dereferenzieren Sie den Eingabedaten Zeiger und speichern das Ergebnis in einer Variablen vom Typ "int". Für 16-Bit-Audiodaten müssen Sie den Byte Zeiger auf einen kurzen Zeiger umgestalten, um die höhere audiostichproben Genauigkeit zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7900b-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="7900b-128">Sobald Sie über den Wert verfügen, können Sie den *pbinputdata* -Zeiger sofort erhöhen, sodass er auf das nächste Beispiel zeigt.</span><span class="sxs-lookup"><span data-stu-id="7900b-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="7900b-129">Dies wird in den folgenden Beispielen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="7900b-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="7900b-130">Oder</span><span class="sxs-lookup"><span data-stu-id="7900b-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="7900b-131">Führen Sie die Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="7900b-131">Perform the processing.</span></span> <span data-ttu-id="7900b-132">An dieser Stelle wenden Sie die Algorithmen an, die das Beispiel irgendwie ändern.</span><span class="sxs-lookup"><span data-stu-id="7900b-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="7900b-133">Was Sie hier tun, ist Ihnen überlassen.</span><span class="sxs-lookup"><span data-stu-id="7900b-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="7900b-134">Schreiben Sie die verarbeiteten Daten in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="7900b-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="7900b-135">Erhöhen Sie den Zeiger direkt auf den Ausgabepuffer, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="7900b-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="7900b-136">Wiederholen Sie die Schleife, bis alle Beispiele verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="7900b-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="7900b-137">Gibt ein entsprechendes **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7900b-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7900b-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7900b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7900b-139">**Implementieren eines audiodsp-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="7900b-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




