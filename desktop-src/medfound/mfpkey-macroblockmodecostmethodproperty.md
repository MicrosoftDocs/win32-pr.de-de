---
description: Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360197"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="87eb7-103">Mfpkey \_ makroblockmodecostmethod (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87eb7-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="87eb7-104">Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="87eb7-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="87eb7-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="87eb7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="87eb7-106">g \_ wszwmvcmacroblockmodecostmethod</span><span class="sxs-lookup"><span data-stu-id="87eb7-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="87eb7-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="87eb7-107">Data Type</span></span>

<span data-ttu-id="87eb7-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="87eb7-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="87eb7-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="87eb7-109">Default Value</span></span>

<span data-ttu-id="87eb7-110">0</span><span class="sxs-lookup"><span data-stu-id="87eb7-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="87eb7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87eb7-111">Remarks</span></span>

<span data-ttu-id="87eb7-112">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87eb7-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="87eb7-113">Wert</span><span class="sxs-lookup"><span data-stu-id="87eb7-113">Value</span></span> | <span data-ttu-id="87eb7-114">Verwendete Methode</span><span class="sxs-lookup"><span data-stu-id="87eb7-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb7-115">0</span><span class="sxs-lookup"><span data-stu-id="87eb7-115">0</span></span>     | <span data-ttu-id="87eb7-116">Traurig/Hadamard.</span><span class="sxs-lookup"><span data-stu-id="87eb7-116">SAD/Hadamard.</span></span> <span data-ttu-id="87eb7-117">Mit dieser Option wird der Codec so konfiguriert, dass nur die Verzerrung beim Berechnen der Kosten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87eb7-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="87eb7-118">1</span><span class="sxs-lookup"><span data-stu-id="87eb7-118">1</span></span>     | <span data-ttu-id="87eb7-119">RD-Kosten.</span><span class="sxs-lookup"><span data-stu-id="87eb7-119">RD cost.</span></span> <span data-ttu-id="87eb7-120">Mit dieser Option wird der Codec so konfiguriert, dass sowohl die Rate als auch die Verzerrung beim Berechnen der Kosten berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="87eb7-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="87eb7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87eb7-121">Requirements</span></span>



| <span data-ttu-id="87eb7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87eb7-122">Requirement</span></span> | <span data-ttu-id="87eb7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="87eb7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb7-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87eb7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="87eb7-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87eb7-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87eb7-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87eb7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="87eb7-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87eb7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87eb7-128">Header</span><span class="sxs-lookup"><span data-stu-id="87eb7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="87eb7-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87eb7-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87eb7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87eb7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87eb7-131">mfpkey- \_ Methode "mutionmatchmethod"</span><span class="sxs-lookup"><span data-stu-id="87eb7-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="87eb7-132">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87eb7-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




