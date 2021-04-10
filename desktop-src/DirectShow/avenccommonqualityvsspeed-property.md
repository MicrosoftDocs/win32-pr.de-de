---
description: Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an. Diese Eigenschaft ist in allen raten Steuerungs Modi gültig.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Avenccommonqualityvsspeed-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125245"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="5449d-104">Avenccommonqualityvsspeed (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5449d-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="5449d-105">Gibt den Kompromiss zwischen Codierungsqualität und Geschwindigkeit an.</span><span class="sxs-lookup"><span data-stu-id="5449d-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="5449d-106">Diese Eigenschaft ist in allen raten Steuerungs Modi gültig.</span><span class="sxs-lookup"><span data-stu-id="5449d-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="5449d-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5449d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5449d-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5449d-108">Data type</span></span>

<span data-ttu-id="5449d-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="5449d-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5449d-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="5449d-110">Property GUID</span></span>

<span data-ttu-id="5449d-111">**Codecapi \_ avenccommonqualityvsspeed**</span><span class="sxs-lookup"><span data-stu-id="5449d-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="5449d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5449d-112">Property value</span></span>

<span data-ttu-id="5449d-113">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="5449d-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="5449d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5449d-114">Value</span></span> | <span data-ttu-id="5449d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5449d-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="5449d-116">0</span><span class="sxs-lookup"><span data-stu-id="5449d-116">0</span></span>     | <span data-ttu-id="5449d-117">Niedrigere Qualität, schnellere Codierung.</span><span class="sxs-lookup"><span data-stu-id="5449d-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="5449d-118">100</span><span class="sxs-lookup"><span data-stu-id="5449d-118">100</span></span>   | <span data-ttu-id="5449d-119">Höhere Qualität, langsamere Codierung.</span><span class="sxs-lookup"><span data-stu-id="5449d-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5449d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5449d-120">Requirements</span></span>



| <span data-ttu-id="5449d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5449d-121">Requirement</span></span> | <span data-ttu-id="5449d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5449d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5449d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5449d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5449d-124">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5449d-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5449d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5449d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5449d-126">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5449d-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5449d-127">Header</span><span class="sxs-lookup"><span data-stu-id="5449d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5449d-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5449d-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5449d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5449d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5449d-130">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="5449d-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5449d-131">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5449d-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




