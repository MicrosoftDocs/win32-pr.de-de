---
description: Gilt für Windows Vista und höher.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910238"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="51229-103">AM \_ RATE \_ ReverseMaxFullDataRate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51229-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="51229-104">Gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="51229-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="51229-105">Gibt die maximale umgekehrte Wiedergaberate des Decoders zurück.</span><span class="sxs-lookup"><span data-stu-id="51229-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="51229-106">Der Wert der -Eigenschaft ist der absolute Wert der maximalen Umgekehrtgeschwindigkeit x 10000.</span><span class="sxs-lookup"><span data-stu-id="51229-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="51229-107">Wenn die maximale umgekehrte Geschwindigkeit beispielsweise -2,0 beträgt, ist der Wert dieser Eigenschaft 20000.</span><span class="sxs-lookup"><span data-stu-id="51229-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="51229-108">Der Datentyp für diese Eigenschaft ist **AM \_ MaxFullDataRate**, bei dem es sich um einen `typedef` für **LONG** handelt.</span><span class="sxs-lookup"><span data-stu-id="51229-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="51229-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="51229-109">This property is read-only.</span></span>



| <span data-ttu-id="51229-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="51229-110">Label</span></span> | <span data-ttu-id="51229-111">Wert</span><span class="sxs-lookup"><span data-stu-id="51229-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="51229-112">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="51229-112">Property Set GUID</span></span> | <span data-ttu-id="51229-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="51229-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="51229-114">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="51229-114">Property ID</span></span>       | <span data-ttu-id="51229-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="51229-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="51229-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="51229-116">Data Type</span></span>         | <span data-ttu-id="51229-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="51229-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="51229-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51229-118">Remarks</span></span>

<span data-ttu-id="51229-119">Decoder, die eine reibungslose umgekehrte Wiedergabe unterstützen, sollten diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="51229-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="51229-120">Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="51229-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51229-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51229-121">Requirements</span></span>



| <span data-ttu-id="51229-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51229-122">Requirement</span></span> | <span data-ttu-id="51229-123">Wert</span><span class="sxs-lookup"><span data-stu-id="51229-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51229-124">Header</span><span class="sxs-lookup"><span data-stu-id="51229-124">Header</span></span><br/> | <dl> <span data-ttu-id="51229-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="51229-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51229-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51229-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51229-127">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="51229-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




