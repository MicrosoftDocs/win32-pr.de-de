---
description: Gibt das Flag für die audioproduktionsinformationen in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Avencddproductioninfoist-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344575"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="68bd6-104">Avencddproductioninfoist (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68bd6-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="68bd6-105">Gibt das Flag für die audioproduktionsinformationen in einem Dolby Digital-Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="68bd6-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="68bd6-106">Diese Eigenschaft gilt für Dolby Digital-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="68bd6-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="68bd6-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="68bd6-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="68bd6-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="68bd6-108">Data type</span></span>

<span data-ttu-id="68bd6-109">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="68bd6-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="68bd6-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="68bd6-110">Property GUID</span></span>

<span data-ttu-id="68bd6-111">**Codecapi \_ avencddproductioninfovorhanden**</span><span class="sxs-lookup"><span data-stu-id="68bd6-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="68bd6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68bd6-112">Remarks</span></span>

<span data-ttu-id="68bd6-113">Wenn der Wert **Variant \_ true** ist, sind die Einstellungen für die Mischungs Ebene und den Raum Typen gültig.</span><span class="sxs-lookup"><span data-stu-id="68bd6-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="68bd6-114">Geben Sie diese Einstellungen mit den Eigenschaften " [**avencddproductionroomtype**](avencddproductionroomtype-property.md) " und " [**avencddproductionmixlevel**](avencddproductionmixlevel-property.md) " an.</span><span class="sxs-lookup"><span data-stu-id="68bd6-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="68bd6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68bd6-115">Requirements</span></span>



| <span data-ttu-id="68bd6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68bd6-116">Requirement</span></span> | <span data-ttu-id="68bd6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="68bd6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68bd6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68bd6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="68bd6-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68bd6-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="68bd6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68bd6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="68bd6-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68bd6-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="68bd6-122">Header</span><span class="sxs-lookup"><span data-stu-id="68bd6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="68bd6-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68bd6-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bd6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68bd6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bd6-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="68bd6-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="68bd6-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68bd6-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




