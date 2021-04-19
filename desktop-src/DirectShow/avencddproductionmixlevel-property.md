---
description: Gibt die Mischungs Ebene in Dezibel (DB) in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Avencddproductionmixlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346003"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="4a2eb-104">Avencddproductionmixlevel (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a2eb-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="4a2eb-105">Gibt die Mischungs Ebene in Dezibel (DB) in einem Dolby Digital-Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="4a2eb-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="4a2eb-106">Diese Eigenschaft gilt für Dolby Digital-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="4a2eb-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="4a2eb-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4a2eb-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a2eb-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4a2eb-108">Data type</span></span>

<span data-ttu-id="4a2eb-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4a2eb-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4a2eb-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="4a2eb-110">Property GUID</span></span>

<span data-ttu-id="4a2eb-111">**Codecapi \_ avencddproductionmixlevel**</span><span class="sxs-lookup"><span data-stu-id="4a2eb-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="4a2eb-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4a2eb-112">Property value</span></span>

<span data-ttu-id="4a2eb-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="4a2eb-113">This property has a linear range of values.</span></span> <span data-ttu-id="4a2eb-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="4a2eb-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2eb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a2eb-115">Remarks</span></span>

<span data-ttu-id="4a2eb-116">Wenn Sie diese Eigenschaft festlegen, legen Sie die Eigenschaft " [**avencddproductioninfoist**](avencddproductioninfoexists-property.md) " auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="4a2eb-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2eb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a2eb-117">Requirements</span></span>



| <span data-ttu-id="4a2eb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a2eb-118">Requirement</span></span> | <span data-ttu-id="4a2eb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2eb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2eb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a2eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2eb-121">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4a2eb-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4a2eb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a2eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2eb-123">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4a2eb-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4a2eb-124">Header</span><span class="sxs-lookup"><span data-stu-id="4a2eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2eb-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2eb-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a2eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2eb-127">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="4a2eb-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4a2eb-128">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4a2eb-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




