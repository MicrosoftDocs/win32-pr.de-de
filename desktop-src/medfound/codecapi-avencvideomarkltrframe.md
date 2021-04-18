---
description: Markiert den aktuellen Frame als einen Ltr-Frame.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524627"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="3c547-103">Codecapi \_ avencvideomarkltrframe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3c547-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="3c547-104">Markiert den aktuellen Frame als einen Ltr-Frame.</span><span class="sxs-lookup"><span data-stu-id="3c547-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c547-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3c547-105">Data type</span></span>

<span data-ttu-id="3c547-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="3c547-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3c547-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="3c547-107">Property GUID</span></span>

<span data-ttu-id="3c547-108">**Codecapi \_ avencvideomarkltrframe**</span><span class="sxs-lookup"><span data-stu-id="3c547-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="3c547-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c547-109">Remarks</span></span>

<span data-ttu-id="3c547-110">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="3c547-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="3c547-111">Der Wert dieses Steuer Elements ist der Wert der H. 264-Syntax *longtermframittelx* , die dem aktuellen Frame zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3c547-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="3c547-112">Wenn sich der aktuelle Frame nicht in der Basisschicht befindet, z. b. wenn die *Temporale \_ ID* des Syntax Elements nicht gleich 0 ist, gilt diese Eigenschaft für den nächsten Basisschicht Rahmen in der Codierungs Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="3c547-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="3c547-113">Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zum Markieren eines Ltr-Frames mithilfe der codecapi- \_ Eigenschaft "avencvideomarkltrframe" ausgegeben wurde und der Encoder einen Frame noch nicht als Ltr gekennzeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="3c547-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="3c547-114">Mit anderen Worten, der Encoder sollte codecapi- \_ krecvideomarkltrframe-Anforderungen nicht in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="3c547-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="3c547-115">Wenn eine codecapi-Anforderung für den Vorgang " \_ avencvideomarkltrframe" übermittelt wird, während eine andere codecapi-Datei " \_ avencvideomarkltrframe" noch aussteht, sollte die ältere Anforderung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3c547-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="3c547-116">Die Eigenschaft "codecapi \_ avencvideomarkltrframe" ist dynamisch und kann während der Codierungs Sitzung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c547-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c547-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c547-117">Requirements</span></span>



| <span data-ttu-id="3c547-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c547-118">Requirement</span></span> | <span data-ttu-id="3c547-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3c547-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c547-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c547-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c547-121">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3c547-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="3c547-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c547-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c547-123">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3c547-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3c547-124">Header</span><span class="sxs-lookup"><span data-stu-id="3c547-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c547-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c547-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c547-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c547-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c547-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c547-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




