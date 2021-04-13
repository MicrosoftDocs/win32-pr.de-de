---
description: Legt die Video-Temporale Ebenenanzahl für einen Video Encoder fest.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484115"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="a2831-103">Codecapi \_ avencvideotemporallayercount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a2831-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="a2831-104">Legt die Video-Temporale Ebenenanzahl für einen Video Encoder fest.</span><span class="sxs-lookup"><span data-stu-id="a2831-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2831-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2831-105">Data type</span></span>

<span data-ttu-id="a2831-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="a2831-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="a2831-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="a2831-107">Property GUID</span></span>

<span data-ttu-id="a2831-108">**Codecapi \_ avencvideotemporallayercount**</span><span class="sxs-lookup"><span data-stu-id="a2831-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2831-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2831-109">Remarks</span></span>

<span data-ttu-id="a2831-110">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2831-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="a2831-111">Codecapi \_ avencvideotemporallayercount, [codecapi \_ avencvideousage](codecapi-avencvideousage.md)und [codecapi \_ avenccommonratecontrolmode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sind statische Codierungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2831-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="a2831-112">Nachdem Sie festgelegt wurden, werden diese nur wirksam, nachdem ein Set Media Type auf der Kamera-s-Ausgabe-PIN aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a2831-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2831-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2831-113">Requirements</span></span>



| <span data-ttu-id="a2831-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2831-114">Requirement</span></span> | <span data-ttu-id="a2831-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a2831-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2831-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2831-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2831-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2831-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a2831-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2831-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2831-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2831-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a2831-120">Header</span><span class="sxs-lookup"><span data-stu-id="a2831-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2831-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2831-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2831-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2831-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2831-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2831-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

