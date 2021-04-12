---
title: Implementieren von imediaobject-"depjeestreamingresources"
description: Implementieren von imediaobject-"depjeestreamingresources"
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
- Echo DSP-Plug-in-Beispiel, Verzögerungs Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388438"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="abc52-109">Implementieren von imediaobject:: Zuweisung</span><span class="sxs-lookup"><span data-stu-id="abc52-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="abc52-110">Im Echo-Beispiel erstellt die Methode " **depingestreamingresources** " den Verzögerungs Puffer.</span><span class="sxs-lookup"><span data-stu-id="abc52-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="abc52-111">Dies geschieht wie folgt:</span><span class="sxs-lookup"><span data-stu-id="abc52-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="abc52-112">Berechnen einer Größe für den Puffer, der der angegebenen Verzögerungszeit für den angegebenen Medientyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="abc52-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="abc52-113">Ordnen Sie entweder neuen Speicher zu, oder ordnen Sie die Puffergröße neu zu, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="abc52-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="abc52-114">Aufrufen einer Methode, die den Puffer mit Werten füllt, die die Stille darstellen.</span><span class="sxs-lookup"><span data-stu-id="abc52-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="abc52-115">Der Wert für "Stille" ist abhängig von der Bittiefe unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="abc52-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="abc52-116">Für 8-Bit-Audiodaten wird Stille durch den Hexadezimalwert 80 dargestellt. für 16-Bit-Audiodaten wird die Ruhe durch 0 (null) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="abc52-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="abc52-117">Berechnen der Verzögerungs Puffergröße</span><span class="sxs-lookup"><span data-stu-id="abc52-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="abc52-118">Um die für den Verzögerungs Puffer erforderliche Größe zu berechnen, müssen Sie zuerst eine **WaveFormatEx** -Struktur abrufen, die Informationen über die Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="abc52-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="abc52-119">Im folgenden Beispiel wird ein Zeiger auf diese-Struktur aus der Eingabe- **DMO- \_ \_ Medientyp** Struktur abgerufen:</span><span class="sxs-lookup"><span data-stu-id="abc52-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="abc52-120">Nachdem Sie einen Zeiger auf die richtige **WaveFormatEx** -Struktur gespeichert haben, können Sie seine Member überprüfen und verwenden, um die erforderliche Puffergröße zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="abc52-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="abc52-121">Dies wird im folgenden Codebeispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="abc52-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="abc52-122">Mit diesem Algorithmus wird die Puffergröße berechnet, indem die Verzögerungszeit (in Millisekunden) multipliziert mit der Anzahl von Samplings pro Millisekunde multipliziert wird. Anschließend wird das Ergebnis mit der Anzahl der Kanäle multipliziert und das Ergebnis dann mit der Anzahl der Bytes pro Stichprobe multipliziert.</span><span class="sxs-lookup"><span data-stu-id="abc52-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="abc52-123">Die Anzahl der Kanäle und die Anzahl der Bytes pro Stichprobe sind nicht offensichtlich. Sie werden im nBlockAlign-Member codiert.</span><span class="sxs-lookup"><span data-stu-id="abc52-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="abc52-124">Division durch 1000 reduziert den nsamplespersec-Wert auf Stichproben pro Millisekunde. die Millisekunde ist die gewünschte Einheit, da die Verzögerungszeit in Millisekunden angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abc52-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="abc52-125">Zuordnen des Verzögerungs Pufferspeichers</span><span class="sxs-lookup"><span data-stu-id="abc52-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="abc52-126">Nachdem Sie die Arbeitsspeicher Anforderungen berechnet haben, können Sie den Puffer zuordnen.</span><span class="sxs-lookup"><span data-stu-id="abc52-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="abc52-127">Der Puffer muss möglicherweise gelöscht werden, wenn er vorhanden ist, z. b. wenn der Benutzer die Eigenschaften Seite aufruft, um den Wert für die Verzögerungszeit zu ändern.</span><span class="sxs-lookup"><span data-stu-id="abc52-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="abc52-128">Der folgende Code veranschaulicht die Zuordnung des Verzögerungs Puffers:</span><span class="sxs-lookup"><span data-stu-id="abc52-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="abc52-129">Wenn der Puffer erfolgreich zugewiesen wurde, sollten Sie den verschiebbaren Zeiger auf den Anfang des Puffers verschieben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="abc52-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="abc52-130">Auffüllen des Verzögerungs Puffers mit Ruhe</span><span class="sxs-lookup"><span data-stu-id="abc52-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="abc52-131">Es ist praktisch, eine Methode zu schreiben, um den Verzögerungs Puffer mit Werten zu füllen, die die Stille darstellen.</span><span class="sxs-lookup"><span data-stu-id="abc52-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="abc52-132">Die Methode sollte den Zeiger auf die gültige WaveFormatEx-Struktur empfangen und dann den Member von wbitspersample überprüfen, um zu bestimmen, ob das Audioelement 8-Bit oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="abc52-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="abc52-133">Im folgenden Beispiel wird der Verzögerungs Puffer mit dem korrekten Wert für "Stille" gefüllt:</span><span class="sxs-lookup"><span data-stu-id="abc52-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="abc52-134">Denken Sie daran, die vorwärts Deklaration für die Funktion der Header Datei "Echo. h" im Abschnitt "private" hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="abc52-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="abc52-135">Sie sollten Code am Ende von "zufügerestreamingresources" hinzufügen, um diese Methode jedes Mal aufzurufen, wenn der Verzögerungs Puffer erstellt oder seine Größe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="abc52-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="abc52-136">Der folgende Beispielcode übergibt den WaveFormatEx-Zeiger mit dem Namen pwave an die neue Methode:</span><span class="sxs-lookup"><span data-stu-id="abc52-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="abc52-137">Neuzuordnen des Verzögerungs Pufferspeichers</span><span class="sxs-lookup"><span data-stu-id="abc52-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="abc52-138">Wenn der Benutzer die Verzögerungszeit mithilfe der Eigenschaften Seite ändert, muss auch die Größe des Verzögerungs Puffers geändert werden.</span><span class="sxs-lookup"><span data-stu-id="abc52-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="abc52-139">Sie haben den Code zu alloingestreamingresources bereits hinzugefügt, um die Größe des Puffers zu ändern. Sie müssen jedoch eine Codezeile zu Cecho::p UT Delay hinzufügen, \_ um die Ressourcen Zuordnungs Methode bei jeder Änderung des Eigenschafts Werts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="abc52-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="abc52-140">Hier folgt der Code:</span><span class="sxs-lookup"><span data-stu-id="abc52-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="abc52-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abc52-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abc52-142">**Arbeiten mit Streamingressourcen**</span><span class="sxs-lookup"><span data-stu-id="abc52-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




