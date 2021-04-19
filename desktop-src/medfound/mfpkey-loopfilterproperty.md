---
description: Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355649"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="aff88-103">Mfpkey \_ loopfilter (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aff88-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="aff88-104">Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="aff88-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="aff88-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="aff88-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="aff88-106">g \_ wszwmvcloopfilter</span><span class="sxs-lookup"><span data-stu-id="aff88-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="aff88-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aff88-107">Data Type</span></span>

<span data-ttu-id="aff88-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="aff88-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="aff88-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aff88-109">Remarks</span></span>

<span data-ttu-id="aff88-110">Der Schleifen Filter ist eine Blockierungs Methode, die während der Codierung und Decodierung angewendet wird, um blockierende Artefakte bei der Codierungs Zeit ("in der Schleife") zu reduzieren, sodass zukünftige P-Frames und B-Frames Sie nicht weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="aff88-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="aff88-111">Die Anwendung des Schleifen Filters wirkt sich darauf aus, dass die Ränder der Makroblöcke in den Ausgabevideo Frames weniger bemerkbar sind.</span><span class="sxs-lookup"><span data-stu-id="aff88-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="aff88-112">Gleichzeitig kann das Bild in der Darstellung weicher werden.</span><span class="sxs-lookup"><span data-stu-id="aff88-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="aff88-113">Obwohl der Schleifen Filter in einigen Frames zu reduzierten Bilddetails führen kann, wird die Qualität des gesamten Videos merklich beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="aff88-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="aff88-114">Der größte Nachteil bei der Verwendung der Schleifen Filterung ist die zusätzliche Decodierung der Leistung.</span><span class="sxs-lookup"><span data-stu-id="aff88-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff88-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff88-115">Requirements</span></span>



| <span data-ttu-id="aff88-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff88-116">Requirement</span></span> | <span data-ttu-id="aff88-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aff88-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff88-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aff88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aff88-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff88-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aff88-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aff88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aff88-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff88-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aff88-122">Header</span><span class="sxs-lookup"><span data-stu-id="aff88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff88-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff88-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff88-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff88-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff88-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aff88-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




