---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für MPEG-2-Video Decodierung.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: AVDecVideoAcceleration_MPEG2-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747249"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a><span data-ttu-id="9621a-103">Avdecvideoacceleration- \_ Eigenschaft (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9621a-103">AVDecVideoAcceleration\_MPEG2 property</span></span>

<span data-ttu-id="9621a-104">Aktiviert oder deaktiviert die Hardwarebeschleunigung für MPEG-2-Video Decodierung.</span><span class="sxs-lookup"><span data-stu-id="9621a-104">Enables or disables hardware acceleration for MPEG-2 video decoding.</span></span>

<span data-ttu-id="9621a-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9621a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9621a-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9621a-106">Data type</span></span>

<span data-ttu-id="9621a-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9621a-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9621a-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="9621a-108">Property GUID</span></span>

<span data-ttu-id="9621a-109">**Codecapi \_ avdecvideoacceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="9621a-109">**CODECAPI\_AVDecVideoAcceleration\_MPEG2**</span></span>

## <a name="remarks"></a><span data-ttu-id="9621a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9621a-110">Remarks</span></span>

<span data-ttu-id="9621a-111">Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die MPEG-2-Video Decodierung.</span><span class="sxs-lookup"><span data-stu-id="9621a-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for MPEG-2 video decoding.</span></span> <span data-ttu-id="9621a-112">Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9621a-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9621a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9621a-113">Requirements</span></span>



| <span data-ttu-id="9621a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9621a-114">Requirement</span></span> | <span data-ttu-id="9621a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9621a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9621a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9621a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9621a-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9621a-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9621a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9621a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9621a-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9621a-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9621a-120">Header</span><span class="sxs-lookup"><span data-stu-id="9621a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9621a-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9621a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9621a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9621a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9621a-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="9621a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9621a-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9621a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




