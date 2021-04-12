---
description: Gibt die Feld Dominanz für einen verschachtelten Videorahmen an.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344868"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="61e47-103">MF Sample Extension \_ bottomfieldfirst-Attribut</span><span class="sxs-lookup"><span data-stu-id="61e47-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="61e47-104">Gibt die Feld Dominanz für einen verschachtelten Videorahmen an.</span><span class="sxs-lookup"><span data-stu-id="61e47-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="61e47-105">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="61e47-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="61e47-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61e47-106">Data type</span></span>

<span data-ttu-id="61e47-107">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61e47-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="61e47-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="61e47-108">Get/set</span></span>

<span data-ttu-id="61e47-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="61e47-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="61e47-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="61e47-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="61e47-111">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="61e47-111">Applies to</span></span>

[<span data-ttu-id="61e47-112">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="61e47-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="61e47-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61e47-113">Remarks</span></span>

<span data-ttu-id="61e47-114">Wenn der Videorahmen Zeilen Sprung enthält und das Beispiel zwei verschachtelte Felder enthält, gibt dieses Attribut an, welches Feld zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="61e47-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="61e47-115">**True** gibt an, dass das untere Feld das erste Mal ist.</span><span class="sxs-lookup"><span data-stu-id="61e47-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="61e47-116">**False** gibt an, dass das oberste Feld zuerst ist.</span><span class="sxs-lookup"><span data-stu-id="61e47-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="61e47-117">Wenn der Frame Zeilen Sprung ist und das Beispiel ein einzelnes Feld enthält, gibt dieses Attribut an, welches Feld das Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="61e47-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="61e47-118">**True** gibt an, dass das Beispiel das untere Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="61e47-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="61e47-119">Wenn der Wert **false** ist, enthält das Beispiel das oberste Feld.</span><span class="sxs-lookup"><span data-stu-id="61e47-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="61e47-120">Wenn der Frame progressiv ist, beschreibt dieses Attribut, wie die Felder angeordnet werden sollen, wenn die Ausgabe mit Zeilen Sprung versehen wird.</span><span class="sxs-lookup"><span data-stu-id="61e47-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="61e47-121">**True** gibt an, dass das untere Feld zuerst ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="61e47-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="61e47-122">Wenn **false**, sollte das oberste Feld zuerst ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61e47-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="61e47-123">Wenn dieses Attribut nicht festgelegt wird, beschreibt der Medientyp die Feld Dominanz.</span><span class="sxs-lookup"><span data-stu-id="61e47-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="61e47-124">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="61e47-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e47-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61e47-125">Requirements</span></span>



| <span data-ttu-id="61e47-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61e47-126">Requirement</span></span> | <span data-ttu-id="61e47-127">Wert</span><span class="sxs-lookup"><span data-stu-id="61e47-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61e47-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61e47-128">Minimum supported client</span></span><br/> | <span data-ttu-id="61e47-129">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="61e47-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="61e47-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61e47-130">Minimum supported server</span></span><br/> | <span data-ttu-id="61e47-131">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="61e47-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="61e47-132">Header</span><span class="sxs-lookup"><span data-stu-id="61e47-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e47-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="61e47-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e47-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61e47-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e47-135">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="61e47-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="61e47-136">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="61e47-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="61e47-137">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="61e47-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="61e47-138">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="61e47-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




