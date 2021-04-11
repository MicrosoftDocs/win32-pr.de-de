---
description: Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215504"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="9b863-103">Mfpkey- \_ Eigenschaft ' peraloptlevel '</span><span class="sxs-lookup"><span data-stu-id="9b863-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="9b863-104">Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="9b863-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9b863-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9b863-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9b863-106">g \_ wszwmvcperperaloptlevel</span><span class="sxs-lookup"><span data-stu-id="9b863-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="9b863-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b863-107">Data Type</span></span>

<span data-ttu-id="9b863-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9b863-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9b863-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9b863-109">Default Value</span></span>

<span data-ttu-id="9b863-110">0</span><span class="sxs-lookup"><span data-stu-id="9b863-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="9b863-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b863-111">Remarks</span></span>

<span data-ttu-id="9b863-112">Die konservative perzeptive Optimierung ist ein Prozess, bei dem der Codec versucht, "wichtige" und "unbedeutende" Bereiche im Videoframe zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9b863-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="9b863-113">Nachdem Sie diese Bereiche des Frames identifiziert haben, erhält der Codec die Qualität wichtiger Regionen auf Kosten der Qualität wichtiger Regionen.</span><span class="sxs-lookup"><span data-stu-id="9b863-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="9b863-114">Die perzeptive Optimierung hebt hervor, dass das Bild für das menschliche Auge richtig angezeigt wird, anstatt auf eine strikte mathematische Genauigkeit zu beharren.</span><span class="sxs-lookup"><span data-stu-id="9b863-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="9b863-115">Die Ergebnisse der Optimierung variieren in Abhängigkeit vom Typ des codierten Videos erheblich.</span><span class="sxs-lookup"><span data-stu-id="9b863-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="9b863-116">Diese Funktion eignet sich gut für die Codierung mit geringem Bitrate und niedriger Auflösung (z. b. Webstreaming), sollte aber wahrscheinlich vermieden werden, wenn Sie auf die Archivierung von Videoqualität abzielen.</span><span class="sxs-lookup"><span data-stu-id="9b863-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b863-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b863-117">Requirements</span></span>



| <span data-ttu-id="9b863-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b863-118">Requirement</span></span> | <span data-ttu-id="9b863-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9b863-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b863-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b863-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b863-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b863-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b863-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b863-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b863-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b863-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b863-124">Header</span><span class="sxs-lookup"><span data-stu-id="9b863-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b863-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b863-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b863-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b863-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b863-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b863-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




