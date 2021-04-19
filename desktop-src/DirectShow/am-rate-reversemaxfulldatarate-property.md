---
description: Gilt für Windows Vista und höher.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369153"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="209e4-103">In \_ Rate \_ reverl maxfulldatarate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="209e4-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="209e4-104">Gilt für Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="209e4-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="209e4-105">Gibt die maximale umgekehrte Wiedergabe Rate des Decoders zurück.</span><span class="sxs-lookup"><span data-stu-id="209e4-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="209e4-106">Der Wert der-Eigenschaft ist der absolute Wert der maximalen umgekehrten Geschwindigkeit x 10000.</span><span class="sxs-lookup"><span data-stu-id="209e4-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="209e4-107">Wenn die maximale umgekehrte Geschwindigkeit beispielsweise-2,0 beträgt, ist der Wert dieser Eigenschaft 20000.</span><span class="sxs-lookup"><span data-stu-id="209e4-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="209e4-108">Der Datentyp für diese Eigenschaft ist " **am \_ maxfulldatarate**", der `typedef` für " **Long**" ist.</span><span class="sxs-lookup"><span data-stu-id="209e4-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="209e4-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="209e4-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="209e4-110">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="209e4-110">Property Set GUID</span></span> | <span data-ttu-id="209e4-111">AM \_ kspropltid \_</span><span class="sxs-lookup"><span data-stu-id="209e4-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="209e4-112">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="209e4-112">Property ID</span></span>       | <span data-ttu-id="209e4-113">Die \_ Rate \_ reverl maxfulldatarate</span><span class="sxs-lookup"><span data-stu-id="209e4-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="209e4-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="209e4-114">Data Type</span></span>         | <span data-ttu-id="209e4-115">**AM \_ maxfulldatarate**</span><span class="sxs-lookup"><span data-stu-id="209e4-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="209e4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="209e4-116">Remarks</span></span>

<span data-ttu-id="209e4-117">Decoderer, die Smooth Reverse-Wiedergabe unterstützen, sollten diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="209e4-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="209e4-118">Weitere Informationen finden Sie unter [Verbesserungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="209e4-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="209e4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="209e4-119">Requirements</span></span>



| <span data-ttu-id="209e4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="209e4-120">Requirement</span></span> | <span data-ttu-id="209e4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="209e4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="209e4-122">Header</span><span class="sxs-lookup"><span data-stu-id="209e4-122">Header</span></span><br/> | <dl> <span data-ttu-id="209e4-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="209e4-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209e4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="209e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209e4-125">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="209e4-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




