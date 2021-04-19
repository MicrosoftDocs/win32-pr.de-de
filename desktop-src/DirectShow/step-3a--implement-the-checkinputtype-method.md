---
description: Schritt 3a.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Schritt 3a. Implementieren der checkinputtype-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350035"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="2ad7e-104">Schritt 3a.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-104">Step 3A.</span></span> <span data-ttu-id="2ad7e-105">Implementieren der checkinputtype-Methode</span><span class="sxs-lookup"><span data-stu-id="2ad7e-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="2ad7e-106">Dies ist Schritt 3a des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2ad7e-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="2ad7e-107">Die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode wird aufgerufen, wenn der upstreamfilter einen Medientyp für den Transformations Filter vorschlägt.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="2ad7e-108">Diese Methode nimmt einen Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt an, bei dem es sich um einen dünnen Wrapper für die [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur von am handelt.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="2ad7e-109">In dieser Methode sollten Sie alle relevanten Felder der **am- \_ \_ Medientyp** Struktur untersuchen, einschließlich der Felder im Format Block.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="2ad7e-110">Sie können die in **cmediatype** definierten Accessor-Methoden verwenden oder direkt auf die Strukturmember verweisen.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="2ad7e-111">Wenn ein Feld ungültig ist, wird der Vfw \_ E- \_ Typ \_ nicht \_ akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="2ad7e-112">Wenn der gesamte Medientyp gültig ist, geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="2ad7e-113">Beispielsweise muss im Filter des RLE-Encoders der Eingabetyp ein 8-Bit-oder ein 4-Bit-nicht komprimiertes RGB-Video sein.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="2ad7e-114">Es gibt keinen Grund, andere Eingabeformate (z. b. 16-oder 24-Bit-RGB) zu unterstützen, da der Filter Sie in eine niedrigere bidirektiontiefe konvertieren muss und DirectShow bereits einen [Farb Raum Konverter](color-space-converter-filter.md) -Filter für diesen Zweck bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="2ad7e-115">Im folgenden Beispiel wird davon ausgegangen, dass der Encoder ein 8-Bit-Video, aber kein 4-Bit-Video unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2ad7e-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="2ad7e-116">In diesem Beispiel überprüft die-Methode zuerst den Haupttyp und den Untertyp.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="2ad7e-117">Anschließend wird der Formattyp überprüft, um sicherzustellen, dass der Format Block eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="2ad7e-118">Der Filter kann auch [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)unterstützen, aber in diesem Fall würde es keinen echten Vorteil haben.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="2ad7e-119">Die **VIDEOINFOHEADER2** -Struktur fügt Unterstützung für das durchlaufen und nicht eckige Pixel hinzu, die in 8-Bit-Videos wahrscheinlich nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="2ad7e-120">Wenn der Formattyp richtig ist, überprüft das Beispiel die Member **biBitCount** und **bicompression** der **videoinfoheader** -Struktur, um zu überprüfen, ob das Format 8-Bit-nicht komprimiertes RGB ist.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="2ad7e-121">Wie in diesem Beispiel gezeigt, müssen Sie das</span><span class="sxs-lookup"><span data-stu-id="2ad7e-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="2ad7e-122">Zeiger auf die richtige-Struktur, basierend auf dem Formattyp.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="2ad7e-123">Überprüfen Sie vor dem Umwandeln des Zeigers immer den Formattyp GUID (**Format Type**) und die Größe des Format Blocks (**cbformat**).</span><span class="sxs-lookup"><span data-stu-id="2ad7e-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="2ad7e-124">Im Beispiel wird außerdem überprüft, ob die Anzahl der Paletteneinträge mit der Bittiefe kompatibel ist und der Format Block groß genug ist, um die Paletteneinträge aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="2ad7e-125">Wenn alle diese Informationen korrekt sind, gibt die Methode "S \_ OK" zurück.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="2ad7e-126">Als nächstes: [Schritt 3B. implementieren Sie die getmediatype-Methode](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="2ad7e-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ad7e-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ad7e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ad7e-128">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="2ad7e-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



