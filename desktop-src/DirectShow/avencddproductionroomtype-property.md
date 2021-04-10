---
description: Gibt den Raumtyp für einen Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Avencddproductionroomtype-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125198"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="a88da-104">Avencddproductionroomtype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a88da-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="a88da-105">Gibt den Raumtyp für einen Dolby Digital-Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="a88da-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="a88da-106">Diese Eigenschaft gilt für Dolby Digital-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="a88da-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="a88da-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a88da-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a88da-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a88da-108">Data type</span></span>

<span data-ttu-id="a88da-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a88da-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a88da-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="a88da-110">Property GUID</span></span>

<span data-ttu-id="a88da-111">**Codecapi \_ avencddproductionroomtype**</span><span class="sxs-lookup"><span data-stu-id="a88da-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="a88da-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a88da-112">Property value</span></span>

<span data-ttu-id="a88da-113">Der Wert dieser Eigenschaft ist ein Member der [**eavencddproductionroomtype**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="a88da-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88da-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a88da-114">Remarks</span></span>

<span data-ttu-id="a88da-115">Der *Raumtyp* bezieht sich auf die Größe des Raums, der während der Produktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a88da-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="a88da-116">Wenn Sie diese Eigenschaft festlegen, legen Sie die Eigenschaft " [**avencddproductioninfoist**](avencddproductioninfoexists-property.md) " auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="a88da-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88da-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a88da-117">Requirements</span></span>



| <span data-ttu-id="a88da-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a88da-118">Requirement</span></span> | <span data-ttu-id="a88da-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a88da-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a88da-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a88da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a88da-121">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a88da-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a88da-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a88da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a88da-123">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a88da-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a88da-124">Header</span><span class="sxs-lookup"><span data-stu-id="a88da-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88da-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88da-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88da-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a88da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88da-127">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="a88da-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a88da-128">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a88da-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

