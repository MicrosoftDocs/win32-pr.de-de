---
description: Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959416"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="0a444-103">Mfpkey- \_ Eigenschaft "mutionmatchmethod"</span><span class="sxs-lookup"><span data-stu-id="0a444-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="0a444-104">Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a444-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0a444-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0a444-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0a444-106">g \_ wszwmvcmutionmatchmethod</span><span class="sxs-lookup"><span data-stu-id="0a444-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="0a444-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0a444-107">Data Type</span></span>

<span data-ttu-id="0a444-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0a444-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0a444-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="0a444-109">Default Value</span></span>

<span data-ttu-id="0a444-110">0</span><span class="sxs-lookup"><span data-stu-id="0a444-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0a444-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a444-111">Remarks</span></span>

<span data-ttu-id="0a444-112">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0a444-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="0a444-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0a444-113">Value</span></span> | <span data-ttu-id="0a444-114">Verwendete Methode</span><span class="sxs-lookup"><span data-stu-id="0a444-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="0a444-115">0</span><span class="sxs-lookup"><span data-stu-id="0a444-115">0</span></span>     | <span data-ttu-id="0a444-116">Summe der absoluten Unterschiede (traurig)</span><span class="sxs-lookup"><span data-stu-id="0a444-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="0a444-117">1</span><span class="sxs-lookup"><span data-stu-id="0a444-117">1</span></span>     | <span data-ttu-id="0a444-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="0a444-118">Hadamard</span></span>                          |
| <span data-ttu-id="0a444-119">-1</span><span class="sxs-lookup"><span data-stu-id="0a444-119">-1</span></span>    | <span data-ttu-id="0a444-120">Makroblock-Adaptive.</span><span class="sxs-lookup"><span data-stu-id="0a444-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="0a444-121">Die Summe der absoluten Unterschiede (Sad) ist eine schnellere, aber weniger genaue Methode als die Hadamard-Transformation.</span><span class="sxs-lookup"><span data-stu-id="0a444-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="0a444-122">Die Hadamard-Transformation ist präziser, aber Rechen intensiv.</span><span class="sxs-lookup"><span data-stu-id="0a444-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="0a444-123">Der Makroblock-Adaptive Modus stellt einen angemessenen Kompromiss zwischen den beiden Methoden dar, indem zwischen den beiden Transformationen dynamisch ausgewählt wird, wobei die Hadamard-Transformation nur bei Bedarf ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0a444-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a444-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a444-124">Requirements</span></span>



| <span data-ttu-id="0a444-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a444-125">Requirement</span></span> | <span data-ttu-id="0a444-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0a444-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a444-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a444-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0a444-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a444-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0a444-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a444-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0a444-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a444-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a444-131">Header</span><span class="sxs-lookup"><span data-stu-id="0a444-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a444-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a444-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a444-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a444-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a444-134">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a444-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




