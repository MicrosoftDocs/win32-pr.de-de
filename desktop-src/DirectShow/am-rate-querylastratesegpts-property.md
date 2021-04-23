---
description: Diese Eigenschaft fragt den Decoder nach der Startzeit der Rateänderung ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von ihrer Position in der Ratenänderungswarteschlange.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910268"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="9ab41-103">AM \_ RATE \_ QueryLastRateSegPTS-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ab41-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="9ab41-104">Diese Eigenschaft fragt den Decoder nach der Startzeit der Rateänderung ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von ihrer Position in der Ratenänderungswarteschlange.</span><span class="sxs-lookup"><span data-stu-id="9ab41-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="9ab41-105">Diese Eigenschaft ist für Version 1.1 dieses Eigenschaftensatzes definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="9ab41-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="9ab41-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="9ab41-106">Label</span></span> | <span data-ttu-id="9ab41-107">Wert</span><span class="sxs-lookup"><span data-stu-id="9ab41-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="9ab41-108">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="9ab41-108">Property Set GUID</span></span> | <span data-ttu-id="9ab41-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="9ab41-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="9ab41-110">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="9ab41-110">Property ID</span></span>       | <span data-ttu-id="9ab41-111">AM \_ RATE \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="9ab41-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="9ab41-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9ab41-112">Data Type</span></span>         | <span data-ttu-id="9ab41-113">**\_REFERENZZEIT**</span><span class="sxs-lookup"><span data-stu-id="9ab41-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="9ab41-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ab41-114">Remarks</span></span>

<span data-ttu-id="9ab41-115">Der Quellfilter kann diese Eigenschaft verwenden, um Rateänderungen über mehrere Audio- und Videostreams hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9ab41-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab41-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ab41-116">Requirements</span></span>



| <span data-ttu-id="9ab41-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ab41-117">Requirement</span></span> | <span data-ttu-id="9ab41-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9ab41-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab41-119">Header</span><span class="sxs-lookup"><span data-stu-id="9ab41-119">Header</span></span><br/> | <dl> <span data-ttu-id="9ab41-120"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab41-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab41-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ab41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab41-122">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="9ab41-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




