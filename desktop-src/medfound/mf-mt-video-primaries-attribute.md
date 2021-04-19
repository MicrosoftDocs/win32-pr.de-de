---
description: Gibt die Farb Primärwerte für einen Video Medientyp an.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359529"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="45c94-103">MF \_ MT- \_ Video- \_ primär Attribut</span><span class="sxs-lookup"><span data-stu-id="45c94-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="45c94-104">Gibt die Farb Primärwerte für einen Video Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="45c94-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="45c94-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="45c94-105">Data type</span></span>

<span data-ttu-id="45c94-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="45c94-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="45c94-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45c94-107">Remarks</span></span>

<span data-ttu-id="45c94-108">Der Wert dieses Attributs ist ein Member der [**mfvideoprimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="45c94-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="45c94-109">Die [**MF videoprimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) -Enumeration identifiziert Farb Replikate, die bestimmten gängigen Videostandards zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="45c94-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="45c94-110">Wenn der Medientyp Farb Replikate verwendet, die nicht in der **MF videoprimaries** -Enumeration identifiziert werden, legen Sie anstelle dieses Attributs das [**benutzerdefinierte Attribut "MF \_ MT \_ Custom \_ Video \_ Primaries**](mf-mt-custom-video-primaries-attribute.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="45c94-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="45c94-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="45c94-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c94-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45c94-112">Requirements</span></span>



| <span data-ttu-id="45c94-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45c94-113">Requirement</span></span> | <span data-ttu-id="45c94-114">Wert</span><span class="sxs-lookup"><span data-stu-id="45c94-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45c94-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45c94-115">Minimum supported client</span></span><br/> | <span data-ttu-id="45c94-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="45c94-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="45c94-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45c94-117">Minimum supported server</span></span><br/> | <span data-ttu-id="45c94-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="45c94-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="45c94-119">Header</span><span class="sxs-lookup"><span data-stu-id="45c94-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c94-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c94-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c94-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45c94-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c94-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="45c94-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="45c94-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="45c94-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="45c94-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="45c94-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="45c94-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="45c94-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="45c94-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="45c94-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="45c94-127">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="45c94-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




