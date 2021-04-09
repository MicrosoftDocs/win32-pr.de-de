---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H. 264-Video Decodierung.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860448"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="c690f-103">Avdecvideoacceleration \_ H264 Property</span><span class="sxs-lookup"><span data-stu-id="c690f-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="c690f-104">Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H. 264-Video Decodierung.</span><span class="sxs-lookup"><span data-stu-id="c690f-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="c690f-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c690f-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c690f-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c690f-106">Data type</span></span>

<span data-ttu-id="c690f-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c690f-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c690f-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="c690f-108">Property GUID</span></span>

<span data-ttu-id="c690f-109">**Codecapi \_ avdecvideoacceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="c690f-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="c690f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c690f-110">Remarks</span></span>

<span data-ttu-id="c690f-111">Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die H. 264-Video Decodierung.</span><span class="sxs-lookup"><span data-stu-id="c690f-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="c690f-112">Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c690f-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="c690f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c690f-113">Requirements</span></span>



| <span data-ttu-id="c690f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c690f-114">Requirement</span></span> | <span data-ttu-id="c690f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c690f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c690f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c690f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c690f-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c690f-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c690f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c690f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c690f-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c690f-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c690f-120">Header</span><span class="sxs-lookup"><span data-stu-id="c690f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c690f-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c690f-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c690f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c690f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c690f-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="c690f-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c690f-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c690f-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




