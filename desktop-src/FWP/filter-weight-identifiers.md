---
title: Filtern von Gewichtungs bezeichlern ("f")
description: Filtern von Gewichtungs Bezeichner, die von der Basis Filter-Engine (BFE) verwendet werden, um automatisch generierte Filter Gewichtungen zu berechnen.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346327"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="d495d-103">Filtern von Gewichtungs bezeichlern</span><span class="sxs-lookup"><span data-stu-id="d495d-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="d495d-104">Die Filter Gewichtungs-IDs, die von der Basis Filter-Engine (BFE) verwendet werden, um automatisch generierte Filter Gewichtungen zu berechnen, sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d495d-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="d495d-105">Weitere Informationen zur Filter Gewichtungs Generierung finden Sie unter [Filtern der Gewichtungs Zuweisung](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="d495d-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="d495d-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**Bits für automatische f- \_ \_ Gewichtung \_**</span><span class="sxs-lookup"><span data-stu-id="d495d-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d495d-107">(60)</span><span class="sxs-lookup"><span data-stu-id="d495d-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="d495d-108">Anzahl von Bits, die für automatisch generierte Filter Gewichtungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d495d-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d495d-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**maximale Größe für \_ Automatisches f- \_ Gewicht \_**</span><span class="sxs-lookup"><span data-stu-id="d495d-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d495d-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="d495d-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="d495d-111">Maximale automatisch generierte Filter Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="d495d-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d495d-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d495d-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d495d-113">0xc</span><span class="sxs-lookup"><span data-stu-id="d495d-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="d495d-114">BFE weist einem IKE-und AuthIP-Filter eine Gewichtung mit diesem Bereichs Wert zu.</span><span class="sxs-lookup"><span data-stu-id="d495d-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="d495d-115">Weitere Informationen zu IKE/AuthIP-Filtern finden Sie unter [IKE/AuthIP-Ausnahmen](ike-exemptions.md) .</span><span class="sxs-lookup"><span data-stu-id="d495d-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d495d-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**swpm- \_ Gewichtungs \_ Bereich- \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="d495d-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d495d-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="d495d-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="d495d-118">BFE weist den IPSec-Richtlinien Filtern eine Gewichtung mit diesem Bereichs Wert zu.</span><span class="sxs-lookup"><span data-stu-id="d495d-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d495d-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**maximale Größe des gültigen f- \_ \_ Bereichs \_**</span><span class="sxs-lookup"><span data-stu-id="d495d-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d495d-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="d495d-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="d495d-121">Maximal zulässiger Wert für Filter Gewichtungs Bereich.</span><span class="sxs-lookup"><span data-stu-id="d495d-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="d495d-122">**MAXUINT64** stellt den größtmöglichen Wert von **UINT64** dar.</span><span class="sxs-lookup"><span data-stu-id="d495d-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="d495d-123">Der Wert dieser Konstante ist 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d495d-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d495d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d495d-124">Requirements</span></span>



| <span data-ttu-id="d495d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d495d-125">Requirement</span></span> | <span data-ttu-id="d495d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d495d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d495d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d495d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d495d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d495d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d495d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d495d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d495d-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d495d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d495d-131">Header</span><span class="sxs-lookup"><span data-stu-id="d495d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d495d-132"><dt>"F"</dt></span><span class="sxs-lookup"><span data-stu-id="d495d-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





