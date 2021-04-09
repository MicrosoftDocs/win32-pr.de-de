---
description: Gibt den Verwendungs Modus für einen UVC H. 264-Encoder an.
ms.assetid: 05158F47-CE01-4C99-8FFA-6BBD4F829B59
title: MF_MT_H264_USAGE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad5239c81e490f5069b8a6f95d4a91c1f150f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129552"
---
# <a name="mf_mt_h264_usage-attribute"></a><span data-ttu-id="8304e-103">MF \_ MT \_ H264 \_ Usage-Attribut</span><span class="sxs-lookup"><span data-stu-id="8304e-103">MF\_MT\_H264\_USAGE attribute</span></span>

<span data-ttu-id="8304e-104">Gibt den Verwendungs Modus für einen UVC H. 264-Encoder an.</span><span class="sxs-lookup"><span data-stu-id="8304e-104">Specifies the usage mode for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="8304e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8304e-105">Data type</span></span>

<span data-ttu-id="8304e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8304e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="8304e-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="8304e-107">Get/set</span></span>

<span data-ttu-id="8304e-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8304e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8304e-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="8304e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8304e-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="8304e-110">Applies to</span></span>

[<span data-ttu-id="8304e-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="8304e-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="8304e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8304e-112">Remarks</span></span>

<span data-ttu-id="8304e-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8304e-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="8304e-114">Der Wert entspricht dem Feld **busage** im UVC 1,2 H. 264 Probe/Commit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8304e-114">The value corresponds to the **bUsage** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8304e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8304e-115">Requirements</span></span>



| <span data-ttu-id="8304e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8304e-116">Requirement</span></span> | <span data-ttu-id="8304e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8304e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8304e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8304e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8304e-119">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8304e-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8304e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8304e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8304e-121">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8304e-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8304e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8304e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8304e-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8304e-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8304e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8304e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8304e-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8304e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8304e-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="8304e-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




