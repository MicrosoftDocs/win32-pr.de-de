---
description: Gibt an, ob ein Videorahmen Zeilen Sprung oder progressiv ist.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357432"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="94959-103">MF Sample Extension- \_ interschnür Attribut</span><span class="sxs-lookup"><span data-stu-id="94959-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="94959-104">Gibt an, ob ein Videorahmen Zeilen Sprung oder progressiv ist.</span><span class="sxs-lookup"><span data-stu-id="94959-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="94959-105">**True** gibt an, dass der Frame mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="94959-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="94959-106">**False** gibt an, dass der Frame progressiv ist.</span><span class="sxs-lookup"><span data-stu-id="94959-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="94959-107">Wenn nicht festgelegt, beschreibt der Medientyp das Interlacing.</span><span class="sxs-lookup"><span data-stu-id="94959-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="94959-108">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="94959-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="94959-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="94959-109">Data type</span></span>

<span data-ttu-id="94959-110">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94959-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="94959-111">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="94959-111">Get/set</span></span>

<span data-ttu-id="94959-112">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="94959-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="94959-113">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="94959-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="94959-114">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="94959-114">Applies to</span></span>

[<span data-ttu-id="94959-115">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="94959-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="94959-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94959-116">Remarks</span></span>

<span data-ttu-id="94959-117">Legen Sie für Videoinhalte, die gemischte und verschachtelte Rahmen enthalten, den Medientyp auf Zeilen Sprung fest, und verwenden Sie dieses Attribut für jeden Frame, um anzugeben, ob der Frame progressiv oder Zeilen Sprung ist.</span><span class="sxs-lookup"><span data-stu-id="94959-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="94959-118">Legen Sie für Videoinhalte, die vollständig mit Zeilen Sprung versehen sind, den Medientyp auf Zeilen Sprung und auslassen dieses Attributs fest, oder legen Sie es für jedes Beispiel auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="94959-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="94959-119">Legen Sie für den Medientyp, der vollständig progressiv ist, den Medientyp auf progressiv fest, und lassen Sie dieses Attribut aus, oder legen Sie es in jeder Stichprobe auf **false**</span><span class="sxs-lookup"><span data-stu-id="94959-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="94959-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="94959-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="94959-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94959-121">Requirements</span></span>



| <span data-ttu-id="94959-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94959-122">Requirement</span></span> | <span data-ttu-id="94959-123">Wert</span><span class="sxs-lookup"><span data-stu-id="94959-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94959-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94959-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94959-125">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="94959-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="94959-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94959-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94959-127">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="94959-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="94959-128">Header</span><span class="sxs-lookup"><span data-stu-id="94959-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="94959-129"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="94959-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94959-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94959-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94959-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="94959-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94959-132">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="94959-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="94959-133">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="94959-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="94959-134">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="94959-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="94959-135">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="94959-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="94959-136">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="94959-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="94959-137">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="94959-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




