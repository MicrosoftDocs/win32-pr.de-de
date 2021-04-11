---
description: Gibt den in Bewegungs suchen verwendeten Bereich an.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: MFPKEY_MOTIONSEARCHRANGE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215509"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="66b22-103">Mfpkey- \_ Eigenschaft "mutionsearchrange"</span><span class="sxs-lookup"><span data-stu-id="66b22-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="66b22-104">Gibt den in Bewegungs suchen verwendeten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="66b22-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="66b22-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="66b22-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="66b22-106">g \_ wszwmvcmutionsearchrange</span><span class="sxs-lookup"><span data-stu-id="66b22-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="66b22-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="66b22-107">Data Type</span></span>

<span data-ttu-id="66b22-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="66b22-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="66b22-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="66b22-109">Default Value</span></span>

<span data-ttu-id="66b22-110">0</span><span class="sxs-lookup"><span data-stu-id="66b22-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="66b22-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66b22-111">Remarks</span></span>

<span data-ttu-id="66b22-112">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="66b22-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="66b22-113">H bezeichnet den horizontalen Bereich und V den vertikalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="66b22-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="66b22-114">Alle Bereiche werden in Pixel angegeben.</span><span class="sxs-lookup"><span data-stu-id="66b22-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="66b22-115">Wert</span><span class="sxs-lookup"><span data-stu-id="66b22-115">Value</span></span> | <span data-ttu-id="66b22-116">Range</span><span class="sxs-lookup"><span data-stu-id="66b22-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="66b22-117">0</span><span class="sxs-lookup"><span data-stu-id="66b22-117">0</span></span>     | <span data-ttu-id="66b22-118">+ 63.75/-64,0 H, + 31.75/-32,0 V</span><span class="sxs-lookup"><span data-stu-id="66b22-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="66b22-119">1</span><span class="sxs-lookup"><span data-stu-id="66b22-119">1</span></span>     | <span data-ttu-id="66b22-120">+127,75/-128,0 H, +63,75/-64,0 V</span><span class="sxs-lookup"><span data-stu-id="66b22-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="66b22-121">2</span><span class="sxs-lookup"><span data-stu-id="66b22-121">2</span></span>     | <span data-ttu-id="66b22-122">+ 511.75/-512.0 H, + 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="66b22-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="66b22-123">3</span><span class="sxs-lookup"><span data-stu-id="66b22-123">3</span></span>     | <span data-ttu-id="66b22-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="66b22-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="66b22-125">-1</span><span class="sxs-lookup"><span data-stu-id="66b22-125">-1</span></span>    | <span data-ttu-id="66b22-126">Macroblock-Adaptive (automatisch)</span><span class="sxs-lookup"><span data-stu-id="66b22-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="66b22-127">Diese Eigenschaft steuert die Größe des Frame Bereichs, den der Codec nach einem Element sucht, das möglicherweise eine Bewegung zwischen Frames feststellt.</span><span class="sxs-lookup"><span data-stu-id="66b22-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="66b22-128">Ein größeres Suchfenster hilft, schnellere Bewegung zu finden, erfordert jedoch mehr CPU-Zeit.</span><span class="sxs-lookup"><span data-stu-id="66b22-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="66b22-129">Die CPU-Anforderungen werden auf jeder Ebene ungefähr verdoppelt.</span><span class="sxs-lookup"><span data-stu-id="66b22-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="66b22-130">Im automatischen Modus (-1) wird dynamisch der effizienteste Modus ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="66b22-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b22-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66b22-131">Requirements</span></span>



| <span data-ttu-id="66b22-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66b22-132">Requirement</span></span> | <span data-ttu-id="66b22-133">Wert</span><span class="sxs-lookup"><span data-stu-id="66b22-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66b22-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66b22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="66b22-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66b22-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66b22-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66b22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="66b22-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66b22-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66b22-138">Header</span><span class="sxs-lookup"><span data-stu-id="66b22-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b22-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b22-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b22-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66b22-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b22-141">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66b22-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




