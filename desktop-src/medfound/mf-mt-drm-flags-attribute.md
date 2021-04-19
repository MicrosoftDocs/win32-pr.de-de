---
description: Gibt an, ob für einen Video Medientyp die Erzwingung des Kopierschutzes erforderlich ist.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: MF_MT_DRM_FLAGS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364078"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="de225-103">MF \_ MT \_ DRM- \_ Flags-Attribut</span><span class="sxs-lookup"><span data-stu-id="de225-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="de225-104">Gibt an, ob für einen Video Medientyp die Erzwingung des Kopierschutzes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="de225-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="de225-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de225-105">Data type</span></span>

<span data-ttu-id="de225-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="de225-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="de225-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de225-107">Remarks</span></span>

<span data-ttu-id="de225-108">Der Wert dieses Attributs ist ein Member der [**mfvideodrmflags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="de225-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="de225-109">Dieses Attribut stellt einen Hinweis für die Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="de225-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="de225-110">Er wird nicht verwendet, um den Kopierschutz zu erzwingen oder den Kopierschutzmechanismus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="de225-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="de225-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="de225-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de225-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de225-112">Requirements</span></span>



| <span data-ttu-id="de225-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de225-113">Requirement</span></span> | <span data-ttu-id="de225-114">Wert</span><span class="sxs-lookup"><span data-stu-id="de225-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de225-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de225-115">Minimum supported client</span></span><br/> | <span data-ttu-id="de225-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="de225-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="de225-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de225-117">Minimum supported server</span></span><br/> | <span data-ttu-id="de225-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="de225-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="de225-119">Header</span><span class="sxs-lookup"><span data-stu-id="de225-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="de225-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="de225-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de225-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de225-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de225-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="de225-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de225-123">MF \_ SD- \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="de225-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="de225-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de225-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="de225-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="de225-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="de225-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="de225-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="de225-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="de225-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




