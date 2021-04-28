---
description: 'AM_RATE_ReverseMaxFullDataRate-Eigenschaft: Gilt für Windows Vista und höher.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099968"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="e7093-103">AM \_ RATE \_ ReverseMaxFullDataRate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7093-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="e7093-104">Gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="e7093-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="e7093-105">Gibt die maximale umgekehrte Wiedergaberate des Decoders zurück.</span><span class="sxs-lookup"><span data-stu-id="e7093-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="e7093-106">Der Wert der -Eigenschaft ist der absolute Wert der maximalen Umgekehrtgeschwindigkeit x 10000.</span><span class="sxs-lookup"><span data-stu-id="e7093-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="e7093-107">Wenn die maximale Umgekehrtgeschwindigkeit beispielsweise -2,0 beträgt, ist der Wert dieser Eigenschaft 20000.</span><span class="sxs-lookup"><span data-stu-id="e7093-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="e7093-108">Der Datentyp für diese Eigenschaft ist **AM \_ MaxFullDataRate**, bei dem es sich um einen `typedef` für **LONG** handelt.</span><span class="sxs-lookup"><span data-stu-id="e7093-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="e7093-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7093-109">This property is read-only.</span></span>



| <span data-ttu-id="e7093-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="e7093-110">Label</span></span> | <span data-ttu-id="e7093-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e7093-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="e7093-112">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="e7093-112">Property Set GUID</span></span> | <span data-ttu-id="e7093-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e7093-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="e7093-114">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="e7093-114">Property ID</span></span>       | <span data-ttu-id="e7093-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="e7093-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="e7093-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e7093-116">Data Type</span></span>         | <span data-ttu-id="e7093-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="e7093-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="e7093-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7093-118">Remarks</span></span>

<span data-ttu-id="e7093-119">Decoder, die eine reibungslose umgekehrte Wiedergabe unterstützen, sollten diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e7093-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="e7093-120">Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="e7093-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7093-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7093-121">Requirements</span></span>



| <span data-ttu-id="e7093-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7093-122">Requirement</span></span> | <span data-ttu-id="e7093-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e7093-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7093-124">Header</span><span class="sxs-lookup"><span data-stu-id="e7093-124">Header</span></span><br/> | <dl> <span data-ttu-id="e7093-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="e7093-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7093-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7093-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7093-127">**Ratenänderungseigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="e7093-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




