---
description: Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347927"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="36fe9-103">Mfpkey \_ denoiseoption (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="36fe9-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="36fe9-104">Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="36fe9-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="36fe9-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="36fe9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="36fe9-106">g \_ wszwmvcdenoise-Option</span><span class="sxs-lookup"><span data-stu-id="36fe9-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="36fe9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="36fe9-107">Data Type</span></span>

<span data-ttu-id="36fe9-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="36fe9-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="36fe9-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="36fe9-109">Default Value</span></span>

<span data-ttu-id="36fe9-110">false</span><span class="sxs-lookup"><span data-stu-id="36fe9-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="36fe9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36fe9-111">Remarks</span></span>

<span data-ttu-id="36fe9-112">Der Rauschfilter kann die Qualität von lärmenden Videoquellen verbessern, wie z. b. Film, der große Mengen an Granularität oder Videoaufnahmen enthält.</span><span class="sxs-lookup"><span data-stu-id="36fe9-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="36fe9-113">Dieser Filter kann in Live Codierungs Szenarios verwendet werden, in denen die externe Vorverarbeitung keine Option ist.</span><span class="sxs-lookup"><span data-stu-id="36fe9-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="36fe9-114">Dieser Filter sollte für saubere Videoquellen deaktiviert werden, da er die Bildqualität reduzieren kann, wenn die Qualität für den Einstieg geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="36fe9-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fe9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36fe9-115">Requirements</span></span>



| <span data-ttu-id="36fe9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36fe9-116">Requirement</span></span> | <span data-ttu-id="36fe9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="36fe9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36fe9-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36fe9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36fe9-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36fe9-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36fe9-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36fe9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36fe9-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36fe9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36fe9-122">Header</span><span class="sxs-lookup"><span data-stu-id="36fe9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36fe9-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="36fe9-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36fe9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36fe9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fe9-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36fe9-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




