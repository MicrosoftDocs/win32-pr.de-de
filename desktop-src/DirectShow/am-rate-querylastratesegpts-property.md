---
description: Diese Eigenschaft fragt den Decoder nach der Startzeit der Änderungs Rate ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von der Position in der Warteschlange für Raten Änderungen.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372617"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="5ad92-103">\_Bitrate \_ querylastratesegpts (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5ad92-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="5ad92-104">Diese Eigenschaft fragt den Decoder nach der Startzeit der Änderungs Rate ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von der Position in der Warteschlange für Raten Änderungen.</span><span class="sxs-lookup"><span data-stu-id="5ad92-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="5ad92-105">Diese Eigenschaft ist für die Version 1,1 dieser Eigenschaften Gruppe definiert. Weitere Informationen finden Sie unter [**\_ Rate \_ userateversion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="5ad92-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="5ad92-106">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="5ad92-106">Property Set GUID</span></span> | <span data-ttu-id="5ad92-107">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="5ad92-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="5ad92-108">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="5ad92-108">Property ID</span></span>       | <span data-ttu-id="5ad92-109">\_Rate der \_ querylastratesegpts</span><span class="sxs-lookup"><span data-stu-id="5ad92-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="5ad92-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5ad92-110">Data Type</span></span>         | <span data-ttu-id="5ad92-111">**Verweis \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="5ad92-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="5ad92-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ad92-112">Remarks</span></span>

<span data-ttu-id="5ad92-113">Der Quell Filter kann diese Eigenschaft verwenden, um Raten Änderungen über mehrere Audiodaten Ströme hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5ad92-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad92-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ad92-114">Requirements</span></span>



| <span data-ttu-id="5ad92-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ad92-115">Requirement</span></span> | <span data-ttu-id="5ad92-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad92-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad92-117">Header</span><span class="sxs-lookup"><span data-stu-id="5ad92-117">Header</span></span><br/> | <dl> <span data-ttu-id="5ad92-118"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad92-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad92-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ad92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad92-120">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="5ad92-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




