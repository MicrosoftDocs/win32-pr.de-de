---
description: Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine AM \_ QueryRate-Struktur.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910278"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="eaea6-104">AM \_ RATE \_ QueryFullFrameRate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eaea6-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="eaea6-105">Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eaea6-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="eaea6-106">Der Datentyp für diese Eigenschaft ist eine **AM \_ QueryRate-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="eaea6-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="eaea6-107">Diese Eigenschaft ist für Version 1.1 dieses Eigenschaftensatzes definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="eaea6-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="eaea6-108">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="eaea6-108">Label</span></span> | <span data-ttu-id="eaea6-109">Wert</span><span class="sxs-lookup"><span data-stu-id="eaea6-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="eaea6-110">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="eaea6-110">Property Set GUID</span></span> | <span data-ttu-id="eaea6-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="eaea6-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="eaea6-112">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="eaea6-112">Property ID</span></span>       | <span data-ttu-id="eaea6-113">AM \_ RATE \_ QueryFullFrameRate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eaea6-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="eaea6-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="eaea6-114">Data Type</span></span>         | [<span data-ttu-id="eaea6-115">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="eaea6-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="eaea6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaea6-116">Remarks</span></span>

<span data-ttu-id="eaea6-117">Wenn die Wiedergaberate die maximale Rate des Decoders überschreitet, sendet der Quellfilter Gruppen kontinuierlicher Stichproben, die durch Diskontinuitäten getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="eaea6-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="eaea6-118">Die Zeitstempel springen über die Diskontinuitäten.</span><span class="sxs-lookup"><span data-stu-id="eaea6-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="eaea6-119">Der Quellfilter kann dies auch dann tun, wenn die Wiedergaberate innerhalb der maximalen Rate des Decoders liegt, da es möglicherweise andere Faktoren gibt, z. B. Datenträger-E/A, die die vollständige Wiedergaberate einschränken.</span><span class="sxs-lookup"><span data-stu-id="eaea6-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaea6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaea6-120">Requirements</span></span>



| <span data-ttu-id="eaea6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaea6-121">Requirement</span></span> | <span data-ttu-id="eaea6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="eaea6-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaea6-123">Header</span><span class="sxs-lookup"><span data-stu-id="eaea6-123">Header</span></span><br/> | <dl> <span data-ttu-id="eaea6-124"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="eaea6-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaea6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaea6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaea6-126">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="eaea6-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




