---
description: Gibt den Raten Steuerungs Modus für einen H. 264-Videostream an.
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: MF_MT_H264_RATE_CONTROL_MODES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3fc19070cd3b45aa25a1307a216f611dce1fd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353101"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a><span data-ttu-id="984a2-103">MF \_ MT \_ H264 \_ Rate- \_ Steuerelement Modi- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="984a2-103">MF\_MT\_H264\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="984a2-104">Gibt den Raten Steuerungs Modus für einen H. 264-Videostream an.</span><span class="sxs-lookup"><span data-stu-id="984a2-104">Specifies the rate-control mode for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="984a2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="984a2-105">Data type</span></span>

<span data-ttu-id="984a2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="984a2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="984a2-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="984a2-107">Get/set</span></span>

<span data-ttu-id="984a2-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="984a2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="984a2-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="984a2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="984a2-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="984a2-110">Applies to</span></span>

[<span data-ttu-id="984a2-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="984a2-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="984a2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="984a2-112">Remarks</span></span>

<span data-ttu-id="984a2-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="984a2-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="984a2-114">Der Wert entspricht dem Feld **bmratecontrolmodes** im UVC 1,2 H. 264 Probe/Commit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="984a2-114">The value corresponds to the **bmRateControlModes** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="984a2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="984a2-115">Requirements</span></span>



| <span data-ttu-id="984a2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="984a2-116">Requirement</span></span> | <span data-ttu-id="984a2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="984a2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="984a2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="984a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="984a2-119">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="984a2-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="984a2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="984a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="984a2-121">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="984a2-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="984a2-122">Header</span><span class="sxs-lookup"><span data-stu-id="984a2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="984a2-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="984a2-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="984a2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="984a2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984a2-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="984a2-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="984a2-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="984a2-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




