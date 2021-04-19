---
description: Gibt das Quell Rechteck für den Videomixer des erweiterten Videorenderer (EVR) an. Das Quell Rechteck ist der Teil des Video Rahmens, der vom Mixer an die Ziel Oberfläche blitet.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT-Attribut (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356573"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="037a4-104">Video \_ Zoom- \_ Rect-Attribut</span><span class="sxs-lookup"><span data-stu-id="037a4-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="037a4-105">Gibt das Quell Rechteck für den Videomixer des [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) an.</span><span class="sxs-lookup"><span data-stu-id="037a4-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="037a4-106">Das Quell Rechteck ist der Teil des Video Rahmens, der vom Mixer an die Ziel Oberfläche blitet.</span><span class="sxs-lookup"><span data-stu-id="037a4-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="037a4-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="037a4-107">Data type</span></span>

<span data-ttu-id="037a4-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="037a4-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="037a4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="037a4-109">Remarks</span></span>

<span data-ttu-id="037a4-110">Der Wert dieses Attributs ist eine [**MF videonormalizedrect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="037a4-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="037a4-111">Das Quell Rechteck wird relativ zu einem normalisierten Koordinatensystem definiert, in dem der gesamte Videorahmen ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt.</span><span class="sxs-lookup"><span data-stu-id="037a4-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="037a4-112">Das Quell Rechteck muss in den Videoframe passen. die Koordinaten des Quell Rechtecks haben einen Bereich von (0... 1).</span><span class="sxs-lookup"><span data-stu-id="037a4-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="037a4-113">Der Standard-EVR Presenter legt dieses Attribut auf dem Mixer fest.</span><span class="sxs-lookup"><span data-stu-id="037a4-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="037a4-114">Gehen Sie folgendermaßen vor, um das-Attribut festzulegen:</span><span class="sxs-lookup"><span data-stu-id="037a4-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="037a4-115">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf dem Mixer, um den Attribut Speicher des Mischers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="037a4-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="037a4-116">Aufrufen von [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) , um das **Video Zoom- \_ \_ Rect** -Attribut auf dem Mixer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="037a4-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="037a4-117">Der Wert ist eine [**MF videonormalizedrect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="037a4-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="037a4-118">In einem benutzerdefinierten EVR Presenter können Sie dieses Attribut verwenden, um die [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) -Methode zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="037a4-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="037a4-119">Weitere Informationen finden Sie unter [Quell-und Ziel Rechtecke](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="037a4-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="037a4-120">Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="037a4-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="037a4-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="037a4-121">Examples</span></span>

<span data-ttu-id="037a4-122">Im folgenden Beispiel wird das Quell Rechteck auf dem Mixer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037a4-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="037a4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037a4-123">Requirements</span></span>



| <span data-ttu-id="037a4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037a4-124">Requirement</span></span> | <span data-ttu-id="037a4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="037a4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="037a4-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="037a4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="037a4-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="037a4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="037a4-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="037a4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="037a4-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="037a4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="037a4-130">Header</span><span class="sxs-lookup"><span data-stu-id="037a4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="037a4-131"><dt>EVR. h</dt></span><span class="sxs-lookup"><span data-stu-id="037a4-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="037a4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037a4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037a4-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="037a4-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="037a4-134">Erweiterte Videorenderer-Attribute</span><span class="sxs-lookup"><span data-stu-id="037a4-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="037a4-135">Schreiben von EVR Presenter</span><span class="sxs-lookup"><span data-stu-id="037a4-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="037a4-136">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="037a4-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="037a4-137">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="037a4-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




