---
description: Gibt den Kompromiss zwischen Bewegung und noch Bildern an. Diese Eigenschaft gilt nur für den Modus für die Konstante Bitrate (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Avencvideocbrmutiontradeoff-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958033"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="766c4-104">Avencvideocbrmutiontradeoff (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="766c4-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="766c4-105">Gibt den Kompromiss zwischen Bewegung und noch Bildern an.</span><span class="sxs-lookup"><span data-stu-id="766c4-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="766c4-106">Diese Eigenschaft gilt nur für den Modus für die Konstante Bitrate (CBR).</span><span class="sxs-lookup"><span data-stu-id="766c4-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="766c4-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="766c4-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="766c4-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="766c4-108">Data type</span></span>

<span data-ttu-id="766c4-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="766c4-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="766c4-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="766c4-110">Property GUID</span></span>

<span data-ttu-id="766c4-111">**Codecapi \_ avencvideocbrmutiontradeoff**</span><span class="sxs-lookup"><span data-stu-id="766c4-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="766c4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="766c4-112">Property value</span></span>

<span data-ttu-id="766c4-113">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="766c4-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="766c4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="766c4-114">Value</span></span> | <span data-ttu-id="766c4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="766c4-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="766c4-116">0</span><span class="sxs-lookup"><span data-stu-id="766c4-116">0</span></span>     | <span data-ttu-id="766c4-117">Für Images optimieren</span><span class="sxs-lookup"><span data-stu-id="766c4-117">Optimize for still images</span></span> |
| <span data-ttu-id="766c4-118">100</span><span class="sxs-lookup"><span data-stu-id="766c4-118">100</span></span>   | <span data-ttu-id="766c4-119">Für Bewegung optimieren.</span><span class="sxs-lookup"><span data-stu-id="766c4-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="766c4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="766c4-120">Requirements</span></span>



| <span data-ttu-id="766c4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="766c4-121">Requirement</span></span> | <span data-ttu-id="766c4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="766c4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="766c4-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="766c4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="766c4-124">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="766c4-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="766c4-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="766c4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="766c4-126">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="766c4-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="766c4-127">Header</span><span class="sxs-lookup"><span data-stu-id="766c4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="766c4-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="766c4-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="766c4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="766c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766c4-130">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="766c4-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="766c4-131">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="766c4-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




