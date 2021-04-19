---
description: Legt die maximale echt Zeiteingabe Rate der Video Frames fest, die an den Encoder ausgegeben werden.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344236"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="5e8cd-103">Codecapi- \_ Eigenschaft "avencmaxframerate"</span><span class="sxs-lookup"><span data-stu-id="5e8cd-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="5e8cd-104">Legt die maximale echt Zeiteingabe Rate der Video Frames fest, die an den Encoder ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e8cd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5e8cd-105">Data type</span></span>

<span data-ttu-id="5e8cd-106">**Ulongulong** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="5e8cd-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5e8cd-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="5e8cd-107">Property GUID</span></span>

<span data-ttu-id="5e8cd-108">**Codecapi \_ avencmaxframerate**</span><span class="sxs-lookup"><span data-stu-id="5e8cd-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8cd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e8cd-109">Remarks</span></span>

<span data-ttu-id="5e8cd-110">Diese Eigenschaft ermöglicht es dem Aufrufer, die maximale echt Zeiteingabe Rate der Video Frames anzugeben, die an den Encoder übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="5e8cd-111">Dadurch erhält der Encoder einen Hinweis auf die Geschwindigkeit, mit der die eingehenden Frames verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="5e8cd-112">Dies ist hilfreich bei Encodern, die sich auf Grundlage der Auflösung und der Framerate des Quellvideos in einer bestimmten Energie Zustands Konfiguration befinden.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="5e8cd-113">Die Framerate wird als Verhältnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="5e8cd-114">Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="5e8cd-115">Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="5e8cd-116">Wenn die Framerate 29,97 fps beträgt, ist das Verhältnis 30.000/1001.</span><span class="sxs-lookup"><span data-stu-id="5e8cd-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8cd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e8cd-117">Requirements</span></span>



| <span data-ttu-id="5e8cd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e8cd-118">Requirement</span></span> | <span data-ttu-id="5e8cd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5e8cd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8cd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e8cd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8cd-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e8cd-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e8cd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e8cd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8cd-123">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e8cd-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e8cd-124">Header</span><span class="sxs-lookup"><span data-stu-id="5e8cd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8cd-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8cd-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e8cd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e8cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8cd-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e8cd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5e8cd-128">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="5e8cd-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

