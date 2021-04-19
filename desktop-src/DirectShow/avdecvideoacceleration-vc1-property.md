---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für das Decodieren von VC-1-Videos.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: AVDecVideoAcceleration_VC1-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343147"
---
# <a name="avdecvideoacceleration_vc1-property"></a><span data-ttu-id="8d871-103">Avdecvideoacceleration \_ VC1 (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8d871-103">AVDecVideoAcceleration\_VC1 property</span></span>

<span data-ttu-id="8d871-104">Aktiviert oder deaktiviert die Hardwarebeschleunigung für das Decodieren von VC-1-Videos.</span><span class="sxs-lookup"><span data-stu-id="8d871-104">Enables or disables hardware acceleration for VC-1 video decoding.</span></span>

<span data-ttu-id="8d871-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8d871-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8d871-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8d871-106">Data type</span></span>

<span data-ttu-id="8d871-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8d871-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8d871-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="8d871-108">Property GUID</span></span>

<span data-ttu-id="8d871-109">**Codecapi \_ avdecvideoacceleration \_ VC1**</span><span class="sxs-lookup"><span data-stu-id="8d871-109">**CODECAPI\_AVDecVideoAcceleration\_VC1**</span></span>

## <a name="remarks"></a><span data-ttu-id="8d871-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d871-110">Remarks</span></span>

<span data-ttu-id="8d871-111">Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die Video Decodierung von VC-1.</span><span class="sxs-lookup"><span data-stu-id="8d871-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for VC-1 video decoding.</span></span> <span data-ttu-id="8d871-112">Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8d871-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d871-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d871-113">Requirements</span></span>



| <span data-ttu-id="8d871-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d871-114">Requirement</span></span> | <span data-ttu-id="8d871-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8d871-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d871-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d871-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8d871-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8d871-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8d871-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d871-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8d871-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8d871-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8d871-120">Header</span><span class="sxs-lookup"><span data-stu-id="8d871-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d871-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d871-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d871-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d871-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d871-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="8d871-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8d871-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8d871-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




