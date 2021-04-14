---
description: Die Framerate eines Video Medientyps in Frames pro Sekunde.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: MF_MT_FRAME_RATE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393722"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="2c6d7-103">MF- \_ MT- \_ Frame \_ Raten Attribut</span><span class="sxs-lookup"><span data-stu-id="2c6d7-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="2c6d7-104">Die Framerate eines Video Medientyps in Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c6d7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2c6d7-105">Data type</span></span>

<span data-ttu-id="2c6d7-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2c6d7-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c6d7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c6d7-107">Remarks</span></span>

<span data-ttu-id="2c6d7-108">Die Framerate wird als Verhältnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="2c6d7-109">Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="2c6d7-110">Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="2c6d7-111">Wenn die Framerate 29,97 fps beträgt, ist das Verhältnis 30.000/1001.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="2c6d7-112">Verwenden Sie die [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) -Funktion, um den Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="2c6d7-113">Um den Wert zu erhalten, verwenden Sie die [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="2c6d7-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="2c6d7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c6d7-115">Examples</span></span>

<span data-ttu-id="2c6d7-116">Im folgenden Beispiel wird die Framerate für einen Video Medientyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="2c6d7-117">Im folgenden Beispiel wird die Frame Rate aus einem Video Medientyp abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2c6d7-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="2c6d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c6d7-118">Requirements</span></span>



| <span data-ttu-id="2c6d7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c6d7-119">Requirement</span></span> | <span data-ttu-id="2c6d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2c6d7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6d7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c6d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6d7-122">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2c6d7-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2c6d7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c6d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6d7-124">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2c6d7-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2c6d7-125">Header</span><span class="sxs-lookup"><span data-stu-id="2c6d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6d7-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c6d7-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6d7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c6d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6d7-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2c6d7-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c6d7-129">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="2c6d7-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2c6d7-130">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="2c6d7-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c6d7-131">**Mfaveragetimeperframeumframerate**</span><span class="sxs-lookup"><span data-stu-id="2c6d7-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="2c6d7-132">**Mfframerateesaveragetimeperframe**</span><span class="sxs-lookup"><span data-stu-id="2c6d7-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




