---
description: Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349151"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="762c5-103">Mfpkey \_ rangeredux (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="762c5-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="762c5-104">Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.</span><span class="sxs-lookup"><span data-stu-id="762c5-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="762c5-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="762c5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="762c5-106">g \_ wszwmvcrangeredux</span><span class="sxs-lookup"><span data-stu-id="762c5-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="762c5-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="762c5-107">Data Type</span></span>

<span data-ttu-id="762c5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="762c5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="762c5-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="762c5-109">Default Value</span></span>

<span data-ttu-id="762c5-110">0</span><span class="sxs-lookup"><span data-stu-id="762c5-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="762c5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="762c5-111">Remarks</span></span>

<span data-ttu-id="762c5-112">Bereichs Reduzierung gibt den Grad an, in dem der Codec den Bereich von Luma und Chroma des Videos verringern soll.</span><span class="sxs-lookup"><span data-stu-id="762c5-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="762c5-113">Durch Verringern des Bereichs wird die Größe codierter Video Frames reduziert, aber auch die Farbdetails des Videos reduziert.</span><span class="sxs-lookup"><span data-stu-id="762c5-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="762c5-114">Die Bereichs Reduzierung besteht aus der Verringerung der Codierung und der Erweiterung während der Decodierung.</span><span class="sxs-lookup"><span data-stu-id="762c5-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="762c5-115">Die Erweiterungs Faktoren können sich von den Reduzierungs Faktoren unterscheiden, aber dies wird in den meisten Szenarien nicht empfohlen, in denen das Neuzuordnen von Bereichen nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="762c5-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="762c5-116">Die Bereichs Reduzierung und-Erweiterung erfolgt separat in den Kanälen von Luma und Chroma.</span><span class="sxs-lookup"><span data-stu-id="762c5-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="762c5-117">Das Verringern des Bereichs kann eine effiziente Möglichkeit zum Reduzieren der Komplexität von Videos mit niedriger Bitrate sein, ohne dass die Bilddetails beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="762c5-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="762c5-118">Wenn Sie alle vier Werte auf 8 festlegen, wird die Menge der Informationen zu "Luma" und "Chroma" um die Hälfte reduziert, sodass mehr Bits zum Beibehalten der Bilddetails umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="762c5-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="762c5-119">Beim Codieren von Videos mit sehr niedrigen Bitraten kann der Codec die Bereichs Reduzierung automatisch verwenden.</span><span class="sxs-lookup"><span data-stu-id="762c5-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="762c5-120">Wenn Sie alle vier Werte auf 0 festlegen, wird die Bereichs Reduzierung auch in Szenarios mit geringem Bitrate vollständig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="762c5-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="762c5-121">Wenn Sie den Farbbereich verringern, wird die codierte Größe von Video Frames reduziert, aber es kann zu einer Unhöflichkeit in den decodierten Frames führen.</span><span class="sxs-lookup"><span data-stu-id="762c5-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="762c5-122">Wenn diese Eigenschaft nicht festgelegt ist, bestimmt der Codec, ob die Bereichs Reduzierung zur Codierungs Zeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="762c5-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="762c5-123">Diese Option wird normalerweise nur bei niedrigen Bitraten durch den Codec ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="762c5-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="762c5-124">Der Wert dieser Eigenschaft ist eine Kombination aus vier Komponenten, die durch Nullen getrennt sind und als 0x0m0m0n0n formatiert sind, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="762c5-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="762c5-125">M ist der Codierungs Bereich-Reduzierungs Faktor für die Y-Komponente.</span><span class="sxs-lookup"><span data-stu-id="762c5-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="762c5-126">m ist der Erweiterungs Faktor für den Decodierungs Bereich für die Y-Komponente (normalerweise identisch mit m).</span><span class="sxs-lookup"><span data-stu-id="762c5-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="762c5-127">N ist der Codierungs Bereich-Reduzierungs Faktor für die UV-Komponente.</span><span class="sxs-lookup"><span data-stu-id="762c5-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="762c5-128">n ist der Erweiterungs Faktor für den Decodierungs Bereich für die UV-Komponente (normalerweise identisch mit n).</span><span class="sxs-lookup"><span data-stu-id="762c5-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="762c5-129">Jeder Faktor ist eine Ziffer zwischen 0 und 8, wobei 0 keine Verringerung oder Erweiterung und 8 die maximale Reduzierung oder Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="762c5-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="762c5-130">Wenn Sie den Wert auf 0x00000000 festlegen, wird die Bereichs Verkleinerung vollständig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="762c5-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="762c5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="762c5-131">Requirements</span></span>



| <span data-ttu-id="762c5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="762c5-132">Requirement</span></span> | <span data-ttu-id="762c5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="762c5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="762c5-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="762c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="762c5-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762c5-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="762c5-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="762c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="762c5-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="762c5-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="762c5-138">Header</span><span class="sxs-lookup"><span data-stu-id="762c5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="762c5-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="762c5-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762c5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="762c5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762c5-141">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="762c5-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




