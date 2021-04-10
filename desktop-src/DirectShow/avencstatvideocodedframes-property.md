---
description: Gibt die Anzahl der codierten Video Frames zurück.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Avencstatus videocodedframes-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124807"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="aca39-103">Avencstatus videocodedframes (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aca39-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="aca39-104">Gibt die Anzahl der codierten Video Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="aca39-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="aca39-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="aca39-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="aca39-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aca39-106">Data type</span></span>

<span data-ttu-id="aca39-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aca39-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aca39-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="aca39-108">Property GUID</span></span>

<span data-ttu-id="aca39-109">**Codecapi \_ avencstatus videocodedframes**</span><span class="sxs-lookup"><span data-stu-id="aca39-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="aca39-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aca39-110">Remarks</span></span>

<span data-ttu-id="aca39-111">Diese Eigenschaft ist nach Abschluss der Codierung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aca39-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="aca39-112">Der Wert dieser Eigenschaft entspricht der Eigenschaft " [**avencstatus videototalframes**](avencstatvideototalframes-property.md) " abzüglich der Anzahl der gelöschten Frames.</span><span class="sxs-lookup"><span data-stu-id="aca39-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="aca39-113">Der Encoder kann Frames ablegen, um innerhalb der angegebenen Bitrate Einschränkungen zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="aca39-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="aca39-114">Möglicherweise werden auch Frames am Ende des Streams abgelegt (siehe Eigenschaft " [**avenccommonstreamendhandling**](avenccommonstreamendhandling-property.md) ").</span><span class="sxs-lookup"><span data-stu-id="aca39-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="aca39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aca39-115">Requirements</span></span>



| <span data-ttu-id="aca39-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aca39-116">Requirement</span></span> | <span data-ttu-id="aca39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aca39-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aca39-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aca39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aca39-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aca39-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aca39-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aca39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aca39-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aca39-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aca39-122">Header</span><span class="sxs-lookup"><span data-stu-id="aca39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca39-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca39-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca39-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aca39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca39-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="aca39-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aca39-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="aca39-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




