---
description: Arbeiten mit Medien Beispielen
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Arbeiten mit Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961104"
---
# <a name="working-with-media-samples"></a><span data-ttu-id="bda87-103">Arbeiten mit Medien Beispielen</span><span class="sxs-lookup"><span data-stu-id="bda87-103">Working with Media Samples</span></span>

<span data-ttu-id="bda87-104">In diesem Thema wird beschrieben, wie Sie die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle zum Bearbeiten von Medien Beispiel Objekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="bda87-104">This topic describes how to use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to manipulate media sample objects.</span></span> <span data-ttu-id="bda87-105">Eine allgemeine Übersicht über die Medien Beispiele finden Sie unter [Medien Beispiele](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="bda87-105">For a general overview of media samples, see [Media Samples](media-samples.md).</span></span>

<span data-ttu-id="bda87-106">Um ein neues Medien Beispiel zu erstellen, rufen Sie die [**mfkreatesample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="bda87-106">To create a new media sample, call the [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) function.</span></span> <span data-ttu-id="bda87-107">Anfänglich ist die Puffer Liste des Beispiels leer.</span><span class="sxs-lookup"><span data-stu-id="bda87-107">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="bda87-108">Um einen Puffer am Ende der Liste hinzuzufügen, nennen Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="bda87-108">To add a buffer to the end of the list, call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="bda87-109">Der folgende Code zeigt, wie Sie ein Beispiel erstellen und diesem einen Puffer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bda87-109">The following code shows how to create a sample and add a buffer to it.</span></span>


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="bda87-110">Die empfohlene Vorgehensweise zum Abrufen der Puffer aus dem Beispiel besteht darin, [**imfsample:: converttezusammenguousbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bda87-110">The recommended way to get the buffers from the sample is to call [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer).</span></span> <span data-ttu-id="bda87-111">Diese Methode gibt einen einzelnen kontinuierlichen Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="bda87-111">This method returns a single continguous buffer.</span></span>

<span data-ttu-id="bda87-112">Um die Puffer in der Liste zu durchlaufen, rufen Sie zunächst [**imfsample:: getbuffercount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount)auf.</span><span class="sxs-lookup"><span data-stu-id="bda87-112">To iterate through the buffers in the list, start by calling [**IMFSample::GetBufferCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount).</span></span> <span data-ttu-id="bda87-113">Diese Methode gibt die Anzahl von Puffern zurück.</span><span class="sxs-lookup"><span data-stu-id="bda87-113">This method returns the number of buffers.</span></span> <span data-ttu-id="bda87-114">Rufen Sie dann [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) auf, und geben Sie den Index des abzurufenden Puffers an.</span><span class="sxs-lookup"><span data-stu-id="bda87-114">Then call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) and specify the index of the buffer to retrieve.</span></span> <span data-ttu-id="bda87-115">Puffer werden von 0 (null) indiziert.</span><span class="sxs-lookup"><span data-stu-id="bda87-115">Buffers are indexed from zero.</span></span>

<span data-ttu-id="bda87-116">Der folgende Code zeigt, wie die Puffer in einem Beispiel durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="bda87-116">The following code shows how to iterate through the buffers in a sample.</span></span>


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



<span data-ttu-id="bda87-117">Beispiele haben einen Zeitstempel und eine Dauer.</span><span class="sxs-lookup"><span data-stu-id="bda87-117">Samples have a time stamp and a duration.</span></span> <span data-ttu-id="bda87-118">Der Zeitstempel gibt an, wann die Daten im Beispiel relativ zur Präsentationszeit gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bda87-118">The time stamp indicates when the data in the sample should be rendered, relative to the presentation clock.</span></span> <span data-ttu-id="bda87-119">Die Dauer ist die Zeitspanne, für die die Daten gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bda87-119">The duration is the length of time for which the data should be rendered.</span></span> <span data-ttu-id="bda87-120">In der Regel legt die Komponente, die die Daten generiert, den anfänglichen Zeitstempel und die Dauer fest.</span><span class="sxs-lookup"><span data-stu-id="bda87-120">Typically the component that generates the data sets the initial time stamp and duration.</span></span> <span data-ttu-id="bda87-121">Diese Werte werden möglicherweise von der Medien Sitzung geändert.</span><span class="sxs-lookup"><span data-stu-id="bda87-121">These values might get modified by the Media Session.</span></span> <span data-ttu-id="bda87-122">Um den Zeitstempel festzulegen, wenden Sie [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)an.</span><span class="sxs-lookup"><span data-stu-id="bda87-122">To set the time stamp, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="bda87-123">Um die Dauer festzulegen, müssen Sie [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bda87-123">To set the duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="bda87-124">Beispiele können auch über Attribute verfügen, die zusätzliche Informationen über das Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="bda87-124">Samples can also have attributes, which contain additional information about the sample.</span></span> <span data-ttu-id="bda87-125">Eine Liste der Beispiel Attribute finden Sie unter [Beispiel Attribute](sample-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bda87-125">For a list of sample attributes, see [Sample Attributes](sample-attributes.md).</span></span> <span data-ttu-id="bda87-126">Zum Festlegen und Abrufen von Attributen verwenden Sie die [**imfattributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) erbt.</span><span class="sxs-lookup"><span data-stu-id="bda87-126">To set and retrieve attributes, use the [**IMFAttributes Interface**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) inherits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bda87-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bda87-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda87-128">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="bda87-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="bda87-129">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="bda87-129">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



