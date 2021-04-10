---
description: Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine geringe Decodierungs Latenz aufweist.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Avenccommonlowlatency-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213987"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="4780c-103">Avenccommonlowlatency (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4780c-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="4780c-104">Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine geringe Decodierungs Latenz aufweist.</span><span class="sxs-lookup"><span data-stu-id="4780c-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="4780c-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4780c-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4780c-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4780c-106">Data type</span></span>

<span data-ttu-id="4780c-107">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="4780c-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4780c-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="4780c-108">Property GUID</span></span>

<span data-ttu-id="4780c-109">**Codecapi \_ avenccommonlowlatency**</span><span class="sxs-lookup"><span data-stu-id="4780c-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="4780c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4780c-110">Remarks</span></span>

<span data-ttu-id="4780c-111">Die Decodierungs Latenz ist definiert als die Menge der Daten, die der Decoder Puffern muss.</span><span class="sxs-lookup"><span data-stu-id="4780c-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="4780c-112">Wenn Sie diese Eigenschaft beispielsweise auf **Variant \_ true** für einen MPEG-Video Encoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="4780c-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="4780c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4780c-113">Requirements</span></span>



| <span data-ttu-id="4780c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4780c-114">Requirement</span></span> | <span data-ttu-id="4780c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4780c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4780c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4780c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4780c-117">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4780c-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4780c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4780c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4780c-119">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4780c-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4780c-120">Header</span><span class="sxs-lookup"><span data-stu-id="4780c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4780c-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4780c-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4780c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4780c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4780c-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="4780c-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4780c-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4780c-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




