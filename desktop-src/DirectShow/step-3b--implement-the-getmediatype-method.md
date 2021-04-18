---
description: Schritt 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Schritt 3B. Implementieren der getmediatype-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530500"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="9edc9-104">Schritt 3B.</span><span class="sxs-lookup"><span data-stu-id="9edc9-104">Step 3B.</span></span> <span data-ttu-id="9edc9-105">Implementieren der getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="9edc9-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="9edc9-106">Dies ist Schritt 3B des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9edc9-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="9edc9-107">Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9edc9-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="9edc9-108">Die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode gibt einen der bevorzugten Ausgabetypen des Filters zurück, auf den von der Indexnummer verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9edc9-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="9edc9-109">Diese Methode wird nie aufgerufen, es sei denn, die Eingabe-PIN des Filters ist bereits verbunden.</span><span class="sxs-lookup"><span data-stu-id="9edc9-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="9edc9-110">Daher können Sie den Medientyp aus der Upstream-Verbindung verwenden, um die bevorzugten Ausgabetypen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9edc9-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="9edc9-111">Ein Encoder bietet in der Regel einen einzelnen bevorzugten Typ, der das Zielformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="9edc9-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="9edc9-112">Decoderer unterstützen in der Regel einen Bereich von Ausgabeformaten und bieten Sie in der Reihenfolge absteigender Qualität oder Effizienz an.</span><span class="sxs-lookup"><span data-stu-id="9edc9-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="9edc9-113">Die Liste kann beispielsweise "UYVY", "Y211", "RGB-24", "RGB-565", "RGB-555" und "RGB-8" in dieser Reihenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="9edc9-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="9edc9-114">Effektfilter erfordern möglicherweise eine genaue Entsprechung zwischen dem Ausgabeformat und dem Eingabeformat.</span><span class="sxs-lookup"><span data-stu-id="9edc9-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="9edc9-115">Im folgenden Beispiel wird ein einzelner Ausgabetyp zurückgegeben, der durch Ändern des Eingabe Typs zum Angeben der RLE8-Komprimierung erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="9edc9-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="9edc9-116">In diesem Beispiel ruft die-Methode [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) auf, um den Eingabetyp aus der Eingabe-PIN zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9edc9-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="9edc9-117">Anschließend werden einige der Felder wie folgt geändert, um das Komprimierungs Format anzugeben:</span><span class="sxs-lookup"><span data-stu-id="9edc9-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="9edc9-118">Er weist eine neue Untertyp-GUID zu, die aus dem FourCC-Code ' mrle ' mithilfe der [**fourccmap**](fourccmap.md) -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9edc9-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="9edc9-119">Er ruft die [**cmediatype:: setvariablesize**](cmediatype-setvariablesize.md) -Methode auf, die das **bfixedsizesamples** -Flag auf **false** und das **lsamplesize** -Element auf 0 (null) festlegt. Dies deutet auf Stichproben variabler Größe hin.</span><span class="sxs-lookup"><span data-stu-id="9edc9-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="9edc9-120">Sie ruft die [**cmediatype:: settemporalcompression**](cmediatype-settemporalcompression.md) -Methode mit dem Wert **false** auf, der angibt, dass jeder Frame ein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="9edc9-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="9edc9-121">(Dieses Feld dient nur zu Informationszwecken, sodass Sie es problemlos ignorieren können.)</span><span class="sxs-lookup"><span data-stu-id="9edc9-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="9edc9-122">Das Feld **bicompression** wird auf BI RLE8 festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="9edc9-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="9edc9-123">Dadurch wird das **bisizeimage** -Feld auf die Bildgröße festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9edc9-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="9edc9-124">Als nächstes: [Schritt 3C. implementieren Sie die checktransform-Methode](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="9edc9-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9edc9-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9edc9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9edc9-126">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="9edc9-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



