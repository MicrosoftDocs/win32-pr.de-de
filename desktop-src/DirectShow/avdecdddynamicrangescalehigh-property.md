---
description: Gibt den auf hoher Ebene ausgeschnittenen Wert an, wenn der Decoder ein dynamisches Bereichs Steuerelement für einen Dolby AC-3-Audiodatenstrom ausführt.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Avdecdddynamicrangescalehigh-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482278"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="75bbe-103">Avdecdddynamicrangescalehigh (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="75bbe-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="75bbe-104">Gibt den auf hoher Ebene ausgeschnittenen Wert an, wenn der Decoder ein dynamisches Bereichs Steuerelement für einen Dolby AC-3-Audiodatenstrom ausführt.</span><span class="sxs-lookup"><span data-stu-id="75bbe-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="75bbe-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="75bbe-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="75bbe-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="75bbe-106">Data type</span></span>

<span data-ttu-id="75bbe-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="75bbe-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="75bbe-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="75bbe-108">Property GUID</span></span>

<span data-ttu-id="75bbe-109">**Codecapi \_ avdecdddynamicrangescalehigh**</span><span class="sxs-lookup"><span data-stu-id="75bbe-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="75bbe-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="75bbe-110">Property value</span></span>

<span data-ttu-id="75bbe-111">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="75bbe-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="75bbe-112">Wert</span><span class="sxs-lookup"><span data-stu-id="75bbe-112">Value</span></span> | <span data-ttu-id="75bbe-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75bbe-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="75bbe-114">0</span><span class="sxs-lookup"><span data-stu-id="75bbe-114">0</span></span>     | <span data-ttu-id="75bbe-115">Keine dynamische Bereichs Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="75bbe-115">No dynamic range compression.</span></span> <span data-ttu-id="75bbe-116">Bewahren Sie den gesamten dynamischen Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="75bbe-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="75bbe-117">100</span><span class="sxs-lookup"><span data-stu-id="75bbe-117">100</span></span>   | <span data-ttu-id="75bbe-118">Vollständige dynamische Bereichs Komprimierung anwenden.</span><span class="sxs-lookup"><span data-stu-id="75bbe-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="75bbe-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75bbe-119">Remarks</span></span>

<span data-ttu-id="75bbe-120">Diese Eigenschaft gilt nur, wenn der Wert der [**avdecddoperationalmode**](avdecddoperationalmode-property.md) -Eigenschaft die Zeile eavdecddoperationalmode ist \_ .</span><span class="sxs-lookup"><span data-stu-id="75bbe-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="75bbe-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75bbe-121">Requirements</span></span>



| <span data-ttu-id="75bbe-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75bbe-122">Requirement</span></span> | <span data-ttu-id="75bbe-123">Wert</span><span class="sxs-lookup"><span data-stu-id="75bbe-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75bbe-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75bbe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="75bbe-125">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="75bbe-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="75bbe-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75bbe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="75bbe-127">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="75bbe-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="75bbe-128">Header</span><span class="sxs-lookup"><span data-stu-id="75bbe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="75bbe-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75bbe-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75bbe-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75bbe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bbe-131">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="75bbe-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="75bbe-132">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="75bbe-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




