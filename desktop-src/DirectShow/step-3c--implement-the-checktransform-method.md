---
description: 'Schritt 3C:'
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: 'Schritt 3C: Implementieren der checktransform-Methode'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218019"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="bd669-104">Schritt 3C:</span><span class="sxs-lookup"><span data-stu-id="bd669-104">Step 3C.</span></span> <span data-ttu-id="bd669-105">Implementieren der checktransform-Methode</span><span class="sxs-lookup"><span data-stu-id="bd669-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="bd669-106">Dies ist Schritt 3C des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bd669-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="bd669-107">Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd669-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="bd669-108">Die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode überprüft, ob ein vorgeschlagene Ausgabetyp mit dem aktuellen Eingabetyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="bd669-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="bd669-109">Die-Methode wird auch aufgerufen, wenn die Eingabe-PIN erneut eine Verbindung herstellt, nachdem die PIN-Ausgabe Verbindung hergestellt</span><span class="sxs-lookup"><span data-stu-id="bd669-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="bd669-110">Im folgenden Beispiel wird überprüft, ob das Format RLE8 Video ist. die Bild Dimensionen entsprechen dem Eingabeformat. und die Paletteneinträge sind identisch.</span><span class="sxs-lookup"><span data-stu-id="bd669-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="bd669-111">Sie lehnt auch Quell-und Ziel Rechtecke ab, die nicht mit der Bildgröße identisch sind.</span><span class="sxs-lookup"><span data-stu-id="bd669-111">It also rejects source and target rectangles that do not match the image size.</span></span>


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="bd669-112">**PIN-erneute Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="bd669-112">**Pin Reconnections**</span></span>

<span data-ttu-id="bd669-113">Anwendungen können die PIN trennen und die Verbindung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="bd669-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="bd669-114">Angenommen, eine Anwendung verbindet beide Pins, trennt die eingabepin und verbindet die Eingabe-PIN dann erneut mit einer neuen Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="bd669-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="bd669-115">In diesem Fall schlägt **checktransform** fehl, da die Abmessungen des Bilds nicht mehr identisch sind.</span><span class="sxs-lookup"><span data-stu-id="bd669-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="bd669-116">Dieses Verhalten ist sinnvoll, obwohl der Filter auch versuchen könnte, die Ausgabepin erneut mit einem neuen Medientyp zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="bd669-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="bd669-117">Weiter: [Schritt 4. Legen Sie zuordnereigenschaften fest](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bd669-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd669-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd669-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd669-119">PIN wird wieder hergestellt</span><span class="sxs-lookup"><span data-stu-id="bd669-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="bd669-120">Quell-und Ziel Rechtecke in Videorenderer</span><span class="sxs-lookup"><span data-stu-id="bd669-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="bd669-121">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="bd669-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



