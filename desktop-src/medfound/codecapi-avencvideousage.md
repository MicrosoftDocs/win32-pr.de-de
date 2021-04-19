---
description: Legt die Video Verwendung für einen Video Encoder fest.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342795"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="01476-103">Codecapi \_ avencvideousage (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="01476-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="01476-104">Legt die Video Verwendung für einen Video Encoder fest.</span><span class="sxs-lookup"><span data-stu-id="01476-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="01476-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="01476-105">Data type</span></span>

<span data-ttu-id="01476-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="01476-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="01476-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="01476-107">Property GUID</span></span>

<span data-ttu-id="01476-108">**Codecapi \_ avencvideousage**</span><span class="sxs-lookup"><span data-stu-id="01476-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="01476-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01476-109">Remarks</span></span>

<span data-ttu-id="01476-110">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="01476-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="01476-111">[Codecapi \_ Avencvideotemporallayercount](codecapi-avencvideotemporallayercount.md), codecapi \_ avencvideousage und [codecapi \_ avenccommonratecontrolmode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sind statische Codierungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01476-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="01476-112">Nachdem Sie festgelegt wurden, werden diese nur wirksam, nachdem ein Set Media Type auf der Kamera-s-Ausgabe-PIN aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="01476-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="01476-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01476-113">Requirements</span></span>



| <span data-ttu-id="01476-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01476-114">Requirement</span></span> | <span data-ttu-id="01476-115">Wert</span><span class="sxs-lookup"><span data-stu-id="01476-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01476-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01476-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01476-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="01476-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="01476-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01476-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01476-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="01476-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="01476-120">Header</span><span class="sxs-lookup"><span data-stu-id="01476-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01476-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01476-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01476-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01476-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01476-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01476-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

