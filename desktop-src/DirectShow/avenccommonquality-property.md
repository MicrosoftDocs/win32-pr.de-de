---
description: Gibt die Qualitätsstufe für die Codierung an.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Avenccommonquality-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482510"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="8ee6a-103">Avenccommonquality (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8ee6a-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="8ee6a-104">Gibt die Qualitätsstufe für die Codierung an.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="8ee6a-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8ee6a-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8ee6a-106">Data type</span></span>

<span data-ttu-id="8ee6a-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8ee6a-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8ee6a-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="8ee6a-108">Property GUID</span></span>

<span data-ttu-id="8ee6a-109">**Codecapi \_ avenccommonquality**</span><span class="sxs-lookup"><span data-stu-id="8ee6a-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="8ee6a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8ee6a-110">Property value</span></span>

<span data-ttu-id="8ee6a-111">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="8ee6a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee6a-112">Value</span></span> | <span data-ttu-id="8ee6a-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ee6a-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="8ee6a-114">0</span><span class="sxs-lookup"><span data-stu-id="8ee6a-114">0</span></span>     | <span data-ttu-id="8ee6a-115">Minimale Qualität, kleinere Ausgabegröße.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="8ee6a-116">100</span><span class="sxs-lookup"><span data-stu-id="8ee6a-116">100</span></span>   | <span data-ttu-id="8ee6a-117">Maximale Qualität, größere Ausgabegröße.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="8ee6a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee6a-118">Remarks</span></span>

<span data-ttu-id="8ee6a-119">Diese Eigenschaft steuert die Qualitätsstufe, wenn der Encoder keine eingeschränkte Bitrate verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="8ee6a-120">Die Eigenschaft " [**avenccommonratecontrolmode**](avenccommonratecontrolmode-property.md) " bestimmt, ob die Bitrate eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="8ee6a-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee6a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee6a-121">Requirements</span></span>



| <span data-ttu-id="8ee6a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee6a-122">Requirement</span></span> | <span data-ttu-id="8ee6a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee6a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee6a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ee6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee6a-125">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8ee6a-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8ee6a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ee6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee6a-127">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8ee6a-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8ee6a-128">Header</span><span class="sxs-lookup"><span data-stu-id="8ee6a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee6a-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee6a-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee6a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ee6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee6a-131">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="8ee6a-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8ee6a-132">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ee6a-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




