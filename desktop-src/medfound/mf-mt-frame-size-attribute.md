---
description: Breite und Höhe eines Video Rahmens in Pixel.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: MF_MT_FRAME_SIZE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352345"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="c991d-103">MF- \_ MT- \_ Frame \_ Größen Attribut</span><span class="sxs-lookup"><span data-stu-id="c991d-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="c991d-104">Breite und Höhe eines Video Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c991d-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="c991d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c991d-105">Data type</span></span>

<span data-ttu-id="c991d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c991d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c991d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c991d-107">Remarks</span></span>

<span data-ttu-id="c991d-108">Die oberen 32 Bits enthalten die Breite, und die unteren 32 Bits enthalten die Höhe.</span><span class="sxs-lookup"><span data-stu-id="c991d-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="c991d-109">Um dieses Attribut festzulegen, verwenden Sie die [**mfsetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c991d-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="c991d-110">Um dieses Attribut zu erhalten, verwenden Sie die [**mfgetattributesize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c991d-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="c991d-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c991d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="c991d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c991d-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="c991d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c991d-113">Requirements</span></span>



| <span data-ttu-id="c991d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c991d-114">Requirement</span></span> | <span data-ttu-id="c991d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c991d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c991d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c991d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c991d-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c991d-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c991d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c991d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c991d-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c991d-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c991d-120">Header</span><span class="sxs-lookup"><span data-stu-id="c991d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c991d-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c991d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c991d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c991d-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c991d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c991d-124">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="c991d-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c991d-125">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="c991d-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




