---
description: Gibt Informationen zum Long-Term Reference (LTR)-Frame an und wird im Ausgabe Beispiel zurückgegeben.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354281"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a><span data-ttu-id="aa960-103">Mfsampleextension \_ longtermreferenceframeinfo-Attribut</span><span class="sxs-lookup"><span data-stu-id="aa960-103">MFSampleExtension\_LongTermReferenceFrameInfo attribute</span></span>

<span data-ttu-id="aa960-104">Gibt Informationen zum Long-Term Reference (LTR)-Frame an und wird im Ausgabe Beispiel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa960-104">Specifies Long Term Reference (LTR) frame info and is returned on the output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa960-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aa960-105">Data type</span></span>

<span data-ttu-id="aa960-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa960-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="aa960-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa960-107">Remarks</span></span>

<span data-ttu-id="aa960-108">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="aa960-108">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="aa960-109">Encoder müssen dieses Attribut für das Ausgabe Beispiel zurückgeben, wenn die Anwendung die Ltr-Frames steuert, die von [codecapi \_ avencvideoltrbuffercontrol](codecapi-avencvideoltrbuffercontrol.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa960-109">Encoders shall return this attribute on the output sample when the application controls LTR frames, which is specified by [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

<span data-ttu-id="aa960-110">Mfsampleextension \_ longtermreferenceframeinfo gibt bis zu zwei Felder zurück.</span><span class="sxs-lookup"><span data-stu-id="aa960-110">MFSampleExtension\_LongTermReferenceFrameInfo returns up to two fields.</span></span>

<span data-ttu-id="aa960-111">Das erste Feld (Bits \[ 0.. 15) \] ist *longtermframeidx* , das dem Ausgabe Frame zugeordnet ist, wenn er als Ltr-Frame markiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa960-111">The first field, bits\[0..15\], is *LongTermFrameIdx* associated with the output frame if it is marked as a LTR frame.</span></span> <span data-ttu-id="aa960-112">Der erste Wert ist 0xFFFF, wenn dieser Ausgabe Rahmen ein kurzfristiger Verweis Rahmen oder ein nicht Verweis Rahmen ist.</span><span class="sxs-lookup"><span data-stu-id="aa960-112">The first value is 0xffff, if this output frame is a short term reference frame or a non-reference frame.</span></span>

<span data-ttu-id="aa960-113">Das zweite Feld, Bits \[ 16.. 31 \] , ist eine Bitmap, die aus " *maxnumltrframes* " zahlreiche Bits besteht, die angeben, welche Ltr-Frames zum Codieren dieses Ausgabe Frames verwendet wurden, beginnend bei Bit 16.</span><span class="sxs-lookup"><span data-stu-id="aa960-113">The second field, bits\[16..31\], is a bitmap consisting of *MaxNumLTRFrames* many bits that indicate which LTR frame(s) were used for encoding this output frame, starting from bit 16.</span></span> <span data-ttu-id="aa960-114">Der Rest der Bits muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aa960-114">The rest of bits shall be set to 0.</span></span> <span data-ttu-id="aa960-115">Der zweite Wert ist 0, wenn dieser Ausgabe Rahmen nicht mithilfe von Ltr-Frames codiert wird.</span><span class="sxs-lookup"><span data-stu-id="aa960-115">The second value is 0 if this output frame is not encoded using any LTR frames.</span></span> <span data-ttu-id="aa960-116">*Maxnumltrframes* ist die maximale Anzahl von Ltr-Frames, die über [codecapi \_ avencvideoltrbuffercontrol](codecapi-avencvideoltrbuffercontrol.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aa960-116">*MaxNumLTRFrames* is the maximum number of LTR frames set through [CODECAPI\_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa960-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa960-117">Requirements</span></span>



| <span data-ttu-id="aa960-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa960-118">Requirement</span></span> | <span data-ttu-id="aa960-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aa960-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa960-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa960-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa960-121">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aa960-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="aa960-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa960-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa960-123">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aa960-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aa960-124">Header</span><span class="sxs-lookup"><span data-stu-id="aa960-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa960-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa960-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa960-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa960-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa960-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="aa960-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




