---
description: Festlegen von Medientypen in einem DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Festlegen von Medientypen in einem DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353631"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="a2e10-103">Festlegen von Medientypen in einem DMO</span><span class="sxs-lookup"><span data-stu-id="a2e10-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="a2e10-104">Bevor ein DMO Daten verarbeiten kann, muss der Client den Medientyp für jeden Stream festlegen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="a2e10-105">(Es gibt eine Ausnahme von dieser Regel, siehe [optionale Streams](optional-streams.md).) Um die Anzahl der Streams zu ermitteln, müssen Sie die [**imediaobject:: getstreamcount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="a2e10-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="a2e10-106">Diese Methode gibt zwei Werte zurück, die Anzahl der Eingaben und die Anzahl der Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="a2e10-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="a2e10-107">Diese Werte sind für die Lebensdauer des DMO fest.</span><span class="sxs-lookup"><span data-stu-id="a2e10-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="a2e10-108">**Bevorzugte Typen**</span><span class="sxs-lookup"><span data-stu-id="a2e10-108">**Preferred Types**</span></span>

<span data-ttu-id="a2e10-109">Der DMO weist für jeden Stream eine Liste möglicher Medientypen in der angegebenen Reihenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="a2e10-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="a2e10-110">Die bevorzugten Typen können z. b. 32-RGB, 24-Bit-RGB und 16-Bit-RGB in dieser Reihenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="a2e10-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="a2e10-111">Wenn die Medientypen vom Client festgelegt werden, können diese Listen als Hinweis verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2e10-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="a2e10-112">Um einen bevorzugten Typ für einen Stream abzurufen, rufen Sie die [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) -Methode oder die [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a2e10-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="a2e10-113">Geben Sie die Datenstrom Nummer und einen Indexwert für den Typ an (beginnend bei null).</span><span class="sxs-lookup"><span data-stu-id="a2e10-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="a2e10-114">Der folgende Code ruft beispielsweise den ersten bevorzugten Typ aus dem ersten Eingabedaten Strom ab:</span><span class="sxs-lookup"><span data-stu-id="a2e10-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="a2e10-115">Um alle bevorzugten Medientypen für einen bestimmten Stream aufzulisten, verwenden Sie eine-Schleife, die den Typindex Inkremente erhöht, bis die-Methode DMO \_ E \_ ohne \_ Weitere Elemente zurückgibt \_ , wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="a2e10-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="a2e10-116">Beachten Sie die folgenden Punkte zu bevorzugten Typen:</span><span class="sxs-lookup"><span data-stu-id="a2e10-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="a2e10-117">Der DMO gibt möglicherweise einen Typ zurück, der über keinen Format Block verfügt.</span><span class="sxs-lookup"><span data-stu-id="a2e10-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="a2e10-118">Ein DMO könnte z. b. einen Videotyp, z. b. 24-Bit-RGB, angeben, ohne die Breite und Höhe des Bilds bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="a2e10-119">Wenn Sie den Typ festlegen, müssen Sie jedoch einen kompletten Format Block bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="a2e10-120">(Einige Medientypen, z. b. "MIDI", benötigen nie einen Format Block. in diesem Fall gilt diese Anmerkung nicht.)</span><span class="sxs-lookup"><span data-stu-id="a2e10-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="a2e10-121">Der DMO muss nicht jede Kombination von bevorzugten Typen unterstützen, die er zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a2e10-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="a2e10-122">Wenn ein DMO z. b. über zwei Streams verfügt und jeder Stream vier bevorzugte Typen aufweist, gibt es 16 mögliche Kombinationen, aber nicht alle davon sind gültig.</span><span class="sxs-lookup"><span data-stu-id="a2e10-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="a2e10-123">Wenn der Client den Medientyp für einen Stream festlegt, kann der DMO die bevorzugten Typen für andere Streams aktualisieren, um den neuen Zustand widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="a2e10-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="a2e10-124">Dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2e10-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="a2e10-125">Für einige Streams bietet der DMO möglicherweise keine bevorzugten Typen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="a2e10-126">In der Regel sollte ein DMO in einigen Streams zumindest einige bevorzugte Typen anbieten.</span><span class="sxs-lookup"><span data-stu-id="a2e10-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="a2e10-127">Der DMO ist nicht erforderlich, um eine komplette Liste der Medientypen, die akzeptiert werden können, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="a2e10-128">Möglicherweise gibt es "nicht angekündigte" Typen, die der DMO unterstützt, aber nicht als bevorzugte Typen anbietet.</span><span class="sxs-lookup"><span data-stu-id="a2e10-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="a2e10-129">Kurz gesagt, der Client sollte die bevorzugten Typen nur als Richtlinien behandeln.</span><span class="sxs-lookup"><span data-stu-id="a2e10-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="a2e10-130">Die einzige Möglichkeit, herauszufinden, welche Typen unterstützt werden, besteht darin, Sie zu testen, wie im nächsten Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2e10-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="a2e10-131">**Festlegen des Medientyps in einem Stream**</span><span class="sxs-lookup"><span data-stu-id="a2e10-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="a2e10-132">Verwenden Sie die Methoden [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) und [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) , um den Typ für jeden Stream festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="a2e10-133">Sie müssen eine **DMO- \_ \_ Medientyp** Struktur bereitstellen, die eine umfassende Beschreibung des Medientyps enthält.</span><span class="sxs-lookup"><span data-stu-id="a2e10-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="a2e10-134">Im folgenden Beispiel 44,1 wird der Medientyp für den Eingabedaten Strom 0 festgelegt</span><span class="sxs-lookup"><span data-stu-id="a2e10-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="a2e10-135">Um einen Medientyp zu testen, ohne ihn festzulegen, müssen Sie **setinputtype** oder **setoutputtype** mit dem Flag DMO \_ Set \_ typef \_ Test \_ only aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="a2e10-136">Die Methode gibt "s OK" zurück \_ , wenn der Typ akzeptabel ist, \_ andernfalls "false":</span><span class="sxs-lookup"><span data-stu-id="a2e10-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="a2e10-137">Da sich die Einstellungen in einem Datenstrom auf einen anderen Stream auswirken können, müssen Sie möglicherweise den Medientyp eines Streams löschen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="a2e10-138">Aufrufen Sie hierzu **setinputtype** oder **setoutputtype** mit dem Flag DMO \_ Set \_ typef \_ Clear.</span><span class="sxs-lookup"><span data-stu-id="a2e10-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="a2e10-139">Bei einem decoderdmo würde der Client in der Regel zuerst den Eingabetyp festlegen und dann einen Ausgabetyp auswählen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="a2e10-140">Bei einem Encoder-DMO würde der Client zuerst den Ausgabetyp und dann den Eingabetyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="a2e10-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2e10-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2e10-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2e10-142">Direktes Hosting eines DMO</span><span class="sxs-lookup"><span data-stu-id="a2e10-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



