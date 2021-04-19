---
description: Gibt bei einem Video Medientyp an, wie 3D-Videorahmen im Arbeitsspeicher gespeichert werden.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359453"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="4caf0-103">\_Format Attribut für MF MT \_ \_ -Video 3D \_</span><span class="sxs-lookup"><span data-stu-id="4caf0-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="4caf0-104">Gibt bei einem Video Medientyp an, wie 3D-Videorahmen im Arbeitsspeicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4caf0-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="4caf0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4caf0-105">Data type</span></span>

<span data-ttu-id="4caf0-106">**MFVideo3DFormat** als **UInt32** gespeichert</span><span class="sxs-lookup"><span data-stu-id="4caf0-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4caf0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4caf0-107">Remarks</span></span>

<span data-ttu-id="4caf0-108">Der Wert dieses Attributs ist ein Member der [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="4caf0-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="4caf0-109">Das-Attribut wird nur angewendet, wenn das [MF \_ MT \_ \_ -Video 3D-](mf-mt-video-3d.md) Attribut den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="4caf0-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="4caf0-110">Dieses Attribut ist für unkomprimierte 3D-Videoformate erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4caf0-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="4caf0-111">Es ist optional für komprimierte 3D-Videos.</span><span class="sxs-lookup"><span data-stu-id="4caf0-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="4caf0-112">Eine Medienquelle, die codierte Frames bereitstellt, kann das-Attribut möglicherweise basierend auf Informationen im Datei Container festlegen.</span><span class="sxs-lookup"><span data-stu-id="4caf0-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="4caf0-113">Andernfalls sollte das Attribut vom Decoder im Ausgabe Medientyp des Decoders festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4caf0-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4caf0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4caf0-114">Requirements</span></span>



| <span data-ttu-id="4caf0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4caf0-115">Requirement</span></span> | <span data-ttu-id="4caf0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4caf0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4caf0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4caf0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4caf0-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4caf0-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4caf0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4caf0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4caf0-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4caf0-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4caf0-121">Header</span><span class="sxs-lookup"><span data-stu-id="4caf0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4caf0-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4caf0-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4caf0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4caf0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4caf0-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4caf0-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




