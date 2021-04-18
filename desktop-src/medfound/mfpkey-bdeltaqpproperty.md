---
description: Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: MFPKEY_BDELTAQP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358423"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="b409a-103">Mfpkey \_ bdelta taqp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b409a-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="b409a-104">Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.</span><span class="sxs-lookup"><span data-stu-id="b409a-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b409a-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b409a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b409a-106">g \_ wszwmvcbdelta taqp</span><span class="sxs-lookup"><span data-stu-id="b409a-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="b409a-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b409a-107">Data Type</span></span>

<span data-ttu-id="b409a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b409a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b409a-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b409a-109">Default Value</span></span>

<span data-ttu-id="b409a-110">0</span><span class="sxs-lookup"><span data-stu-id="b409a-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b409a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b409a-111">Remarks</span></span>

<span data-ttu-id="b409a-112">Der Bild quantifiziererer (QP) ist ein Maß für die Komprimierung eines Frames.</span><span class="sxs-lookup"><span data-stu-id="b409a-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="b409a-113">Höhere Werte stellen höhere Komprimierungs Verhältnisse dar.</span><span class="sxs-lookup"><span data-stu-id="b409a-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="b409a-114">Der QP kann in Schritten von halb Punkten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b409a-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="b409a-115">Ein B-Frame wird in der Regel mit einem QP identisch mit dem Wert oder 0,5, der höher ist als der QP des Anker Rahmens.</span><span class="sxs-lookup"><span data-stu-id="b409a-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="b409a-116">Durch die Angabe eines b-Frame-QP-Deltas oberhalb von 0 ist es möglich, B-Frames mit einem noch höheren Komprimierungs Verhältnis zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="b409a-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="b409a-117">Der B-Frame-Delta-QP kann nur in ganz punktinkrementen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b409a-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="b409a-118">Diese Eigenschaft muss auf einen ganzzahligen Wert zwischen 0 und 31 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b409a-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="b409a-119">Der empfohlene Wert ist 1.</span><span class="sxs-lookup"><span data-stu-id="b409a-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="b409a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b409a-120">Requirements</span></span>



| <span data-ttu-id="b409a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b409a-121">Requirement</span></span> | <span data-ttu-id="b409a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b409a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b409a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b409a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b409a-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b409a-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b409a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b409a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b409a-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b409a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b409a-127">Header</span><span class="sxs-lookup"><span data-stu-id="b409a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b409a-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b409a-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b409a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b409a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b409a-130">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b409a-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




