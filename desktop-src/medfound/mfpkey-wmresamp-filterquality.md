---
description: Gibt die Qualität der Ausgabe an.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: MFPKEY_WMRESAMP_FILTERQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215041"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="8ec4d-103">Mfpkey \_ wmresamp \_ filterquality (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8ec4d-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="8ec4d-104">Gibt die Qualität der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8ec4d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8ec4d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8ec4d-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8ec4d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8ec4d-107">Data Type</span></span>

<span data-ttu-id="8ec4d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8ec4d-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="8ec4d-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="8ec4d-109">Applies To</span></span>

-   [<span data-ttu-id="8ec4d-110">Audioresampler-DSP</span><span class="sxs-lookup"><span data-stu-id="8ec4d-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="8ec4d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ec4d-111">Remarks</span></span>

<span data-ttu-id="8ec4d-112">Der gültige Bereich dieser Eigenschaft liegt zwischen 1 und 60 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="8ec4d-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="8ec4d-113">Höhere Werte führen zu einer Ausgabe höherer Qualität, führen jedoch zu einer höheren Latenz.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="8ec4d-114">Der Wert 1 ist im Wesentlichen identisch mit der linearen interpolung.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec4d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ec4d-115">Requirements</span></span>



| <span data-ttu-id="8ec4d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ec4d-116">Requirement</span></span> | <span data-ttu-id="8ec4d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8ec4d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec4d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ec4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec4d-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ec4d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8ec4d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ec4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec4d-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ec4d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ec4d-122">Header</span><span class="sxs-lookup"><span data-stu-id="8ec4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec4d-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4d-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec4d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ec4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec4d-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8ec4d-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
