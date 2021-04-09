---
description: Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869555"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="76ad8-103">Mfpkey \_ forcemediansetting (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76ad8-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="76ad8-104">Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="76ad8-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="76ad8-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="76ad8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="76ad8-106">g \_ wszwmvcforcemediansetting</span><span class="sxs-lookup"><span data-stu-id="76ad8-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="76ad8-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="76ad8-107">Data Type</span></span>

<span data-ttu-id="76ad8-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="76ad8-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="76ad8-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="76ad8-109">Default Value</span></span>

<span data-ttu-id="76ad8-110">false</span><span class="sxs-lookup"><span data-stu-id="76ad8-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="76ad8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76ad8-111">Remarks</span></span>

<span data-ttu-id="76ad8-112">Die Median Filterung weist den Codec an, Rauschen und Körner beim Berechnen der Bewegung zwischen Frames zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="76ad8-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="76ad8-113">Dies kann die Qualität des Videos mit sehr lauter Qualität verbessern, kann jedoch zu Bewegungs Pfaden (auch als nachfolgende Artefakte bezeichnet) führen, wenn diese auf das saubere Quellvideo angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="76ad8-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="76ad8-114">Standardmäßig verwendet der Codec interne Logik, um zu bestimmen, ob die Median Filterung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76ad8-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="76ad8-115">Wenn Sie diese Eigenschaft festlegen, wird diese Logik überschrieben.</span><span class="sxs-lookup"><span data-stu-id="76ad8-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="76ad8-116">Dieser Filter ist nicht mit den in vielen Video Bearbeitungs-und nachträglich verarbeiteten Anwendungen gefundenen Median weich Filtern identisch.</span><span class="sxs-lookup"><span data-stu-id="76ad8-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76ad8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76ad8-117">Requirements</span></span>



| <span data-ttu-id="76ad8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76ad8-118">Requirement</span></span> | <span data-ttu-id="76ad8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="76ad8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76ad8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76ad8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76ad8-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76ad8-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="76ad8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76ad8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76ad8-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76ad8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76ad8-124">Header</span><span class="sxs-lookup"><span data-stu-id="76ad8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ad8-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ad8-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ad8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ad8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ad8-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76ad8-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




