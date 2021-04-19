---
description: Gibt den maximalen QP an, der vom Encoder unterstützt wird.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346051"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="80162-103">Codecapi \_ avencvideomaxqp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80162-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="80162-104">Gibt den maximalen QP an, der vom Encoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="80162-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="80162-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80162-105">Data type</span></span>

<span data-ttu-id="80162-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="80162-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="80162-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="80162-107">Property GUID</span></span>

<span data-ttu-id="80162-108">**Codecapi \_ avencvideomaxqp**</span><span class="sxs-lookup"><span data-stu-id="80162-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="80162-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80162-109">Remarks</span></span>

<span data-ttu-id="80162-110">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="80162-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="80162-111">Der Encoder muss "[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.</span><span class="sxs-lookup"><span data-stu-id="80162-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="80162-112">Dies ist eine statische Eigenschaft, die bedeutet, dass Sie nur festgelegt werden kann, bevor die Codierungs Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="80162-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="80162-113">Der Standardwert muss dem maximalen QP entsprechen, der vom entsprechenden Codierungsstandard zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="80162-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="80162-114">Beispielsweise müssen H. 264-Encoder den Standardwert 51 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="80162-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="80162-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80162-115">Requirements</span></span>



| <span data-ttu-id="80162-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80162-116">Requirement</span></span> | <span data-ttu-id="80162-117">Wert</span><span class="sxs-lookup"><span data-stu-id="80162-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80162-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80162-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80162-119">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="80162-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="80162-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80162-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80162-121">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="80162-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="80162-122">Header</span><span class="sxs-lookup"><span data-stu-id="80162-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80162-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80162-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80162-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80162-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80162-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80162-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="80162-126">Codecapi \_ avencvideominqp</span><span class="sxs-lookup"><span data-stu-id="80162-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

