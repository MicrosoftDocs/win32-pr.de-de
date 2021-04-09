---
description: Arbeiten mit Medien Puffern
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Arbeiten mit Medien Puffern (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869544"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="92ded-103">Arbeiten mit Medien Puffern (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="92ded-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="92ded-104">In diesem Thema wird beschrieben, wie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle für den Zugriff auf die Daten in einem Medien Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92ded-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="92ded-105">Alle Medien Puffer machen **imfmediabuffer** verfügbar, das für beliebige Datentypen konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="92ded-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="92ded-106">Nicht komprimierte Video Frames sind ein Sonderfall, der im Thema [unkomprimierte Video Puffer](uncompressed-video-buffers.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="92ded-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="92ded-107">Puffergröße</span><span class="sxs-lookup"><span data-stu-id="92ded-107">Buffer Size</span></span>

<span data-ttu-id="92ded-108">Einem Medien Puffer sind zwei Größen zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="92ded-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="92ded-109">Die *Maximale Länge* ist die physische Größe des Arbeitsspeichers, der dem Puffer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="92ded-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="92ded-110">Dieser Wert wird festgelegt, wenn der Puffer erstellt wird, und wird während der Lebensdauer des Puffers nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="92ded-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="92ded-111">Die maximale Länge gibt an, wie viele Daten im Puffer gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="92ded-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="92ded-112">Um die maximale Größe zu ermitteln, nennen Sie [**imfmediabuffer:: getmaxlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="92ded-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="92ded-113">Die *aktuelle Länge* ist die Menge gültiger Daten, die sich derzeit im Puffer befinden.</span><span class="sxs-lookup"><span data-stu-id="92ded-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="92ded-114">Beim ersten zuordnen des Puffers ist die aktuelle Länge 0 (null), da keine gültigen Daten im Puffer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="92ded-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="92ded-115">Wenn Sie Daten in den Puffer schreiben, müssen Sie die aktuelle Länge durch Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength)aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="92ded-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="92ded-116">Wenn Sie z. b. 100 Bytes an Daten in den Puffer schreiben, nennen Sie **setcurrentlength** mit dem Wert 100.</span><span class="sxs-lookup"><span data-stu-id="92ded-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="92ded-117">Wenn Sie Daten aus einem Medien Puffer lesen, können Sie [**imfmediabuffer:: getcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) aufrufen, um herauszufinden, wie viele Daten aktuell im Puffer sind.</span><span class="sxs-lookup"><span data-stu-id="92ded-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="92ded-118">Liest die aktuelle Länge nicht.</span><span class="sxs-lookup"><span data-stu-id="92ded-118">Do not read past the current length.</span></span> <span data-ttu-id="92ded-119">Die aktuelle Länge kann die maximale Länge des Puffers nie überschreiten.</span><span class="sxs-lookup"><span data-stu-id="92ded-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="92ded-120">Zugreifen auf den Pufferspeicher</span><span class="sxs-lookup"><span data-stu-id="92ded-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="92ded-121">Um auf den Speicher im Puffer zuzugreifen, nennen Sie [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="92ded-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="92ded-122">Diese Methode gibt einen Zeiger auf den Anfang des Speicherblocks zurück.</span><span class="sxs-lookup"><span data-stu-id="92ded-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="92ded-123">Außerdem werden die maximale Länge und die aktuelle Länge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92ded-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="92ded-124">Wenn Sie die Verwendung des Zeigers abgeschlossen haben, nennen Sie [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="92ded-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="92ded-125">So schreiben Sie Daten in einen Medien Puffer:</span><span class="sxs-lookup"><span data-stu-id="92ded-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="92ded-126">Zum Abrufen eines Zeigers auf den Speicher muss [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92ded-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="92ded-127">Die-Methode gibt auch die maximale Länge des Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="92ded-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="92ded-128">Schreiben Sie die Daten in den Arbeitsspeicher, bis die maximale Länge des Puffers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="92ded-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="92ded-129">Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) zum Aktualisieren der aktuellen Länge.</span><span class="sxs-lookup"><span data-stu-id="92ded-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="92ded-130">Legen Sie die aktuelle Länge auf die Menge der Daten fest, die Sie in Schritt 2 geschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="92ded-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="92ded-131">Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92ded-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="92ded-132">So lesen Sie Daten aus einem Medien Puffer:</span><span class="sxs-lookup"><span data-stu-id="92ded-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="92ded-133">Zum Abrufen eines Zeigers auf den Speicher muss [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92ded-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="92ded-134">Die-Methode gibt auch die aktuelle Länge des Puffers (die Menge der gültigen Daten im Puffer) zurück.</span><span class="sxs-lookup"><span data-stu-id="92ded-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="92ded-135">Lesen Sie den Inhalt des Arbeitsspeichers bis zur aktuellen Länge.</span><span class="sxs-lookup"><span data-stu-id="92ded-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="92ded-136">Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92ded-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="92ded-137">Erstellen von System Speicher Puffern</span><span class="sxs-lookup"><span data-stu-id="92ded-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="92ded-138">Der Systemspeicher Puffer ist ein Medien Puffer, der einen Block des System Speichers verwaltet.</span><span class="sxs-lookup"><span data-stu-id="92ded-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="92ded-139">Um eine Instanz dieses Objekts zu erstellen, rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) oder [**mfkreatealignedmemorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) auf, und geben Sie eine Puffergröße an.</span><span class="sxs-lookup"><span data-stu-id="92ded-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="92ded-140">Beide Funktionen weisen einen Speicherblock zu und geben einen [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="92ded-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="92ded-141">Der Arbeitsspeicher wird automatisch freigegeben, wenn der Verweis Zähler des Medien Puffers Null erreicht und das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="92ded-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="92ded-142">Im folgenden Beispiel wird gezeigt, wie ein Systemspeicher Puffer erstellt und in den Puffer geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="92ded-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="92ded-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92ded-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ded-144">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="92ded-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="92ded-145">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="92ded-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



