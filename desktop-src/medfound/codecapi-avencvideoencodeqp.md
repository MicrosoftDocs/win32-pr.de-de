---
description: Gibt den Quantisierungsparameter (QP) für die Videocodierung an.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339723"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="adfe2-103">Codecapi \_ avencvideoencodeqp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="adfe2-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="adfe2-104">Gibt den Quantisierungsparameter (QP) für die Videocodierung an.</span><span class="sxs-lookup"><span data-stu-id="adfe2-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="adfe2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="adfe2-105">Data type</span></span>

<span data-ttu-id="adfe2-106">**ULONGLONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="adfe2-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="adfe2-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="adfe2-107">Property GUID</span></span>

<span data-ttu-id="adfe2-108">**Codecapi \_ avencvideoencodeqp**</span><span class="sxs-lookup"><span data-stu-id="adfe2-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="adfe2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="adfe2-109">Property value</span></span>

<span data-ttu-id="adfe2-110">Ein Satz von 4 16-Bit-Feldern, die verwendet werden, um die Frame-QPS in der Fixed-QP-Codierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="adfe2-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="adfe2-111">Die Felder lauten:</span><span class="sxs-lookup"><span data-stu-id="adfe2-111">The fields are:</span></span>

-   <span data-ttu-id="adfe2-112">Bits 0-15: Standard-QP</span><span class="sxs-lookup"><span data-stu-id="adfe2-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="adfe2-113">Bits 16-31: für I-Frames verwendetes QP</span><span class="sxs-lookup"><span data-stu-id="adfe2-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="adfe2-114">Bits 32-47: für P-Frames verwendetes QP</span><span class="sxs-lookup"><span data-stu-id="adfe2-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="adfe2-115">Bits 48-63: für B-Frames verwendetes QP</span><span class="sxs-lookup"><span data-stu-id="adfe2-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="adfe2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adfe2-116">Remarks</span></span>

<span data-ttu-id="adfe2-117">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="adfe2-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="adfe2-118">Um eine konsistente Verwendung für verschiedene Encoder sicherzustellen, sollten Sie davon ausgehen, dass Encoder nur das Standard-QP betrachten und QP-Werte für e/a/B-Bilder ignorieren können.</span><span class="sxs-lookup"><span data-stu-id="adfe2-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="adfe2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adfe2-119">Requirements</span></span>



| <span data-ttu-id="adfe2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adfe2-120">Requirement</span></span> | <span data-ttu-id="adfe2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="adfe2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adfe2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adfe2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adfe2-123">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="adfe2-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="adfe2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adfe2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adfe2-125">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="adfe2-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="adfe2-126">Header</span><span class="sxs-lookup"><span data-stu-id="adfe2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="adfe2-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="adfe2-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adfe2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adfe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfe2-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="adfe2-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="adfe2-130">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="adfe2-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

