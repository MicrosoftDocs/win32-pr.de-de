---
description: Gibt an, ob ein Deinterlacing-Videoframe aus dem oberen Feld oder dem unteren Feld abgeleitet wurde.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349137"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="27cbd-103">MF SampleExtension \_ derivedfromtopfield-Attribut</span><span class="sxs-lookup"><span data-stu-id="27cbd-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="27cbd-104">Gibt an, ob ein Deinterlacing-Videoframe aus dem oberen Feld oder dem unteren Feld abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="27cbd-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="27cbd-105">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="27cbd-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="27cbd-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="27cbd-106">Data type</span></span>

<span data-ttu-id="27cbd-107">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27cbd-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="27cbd-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="27cbd-108">Get/set</span></span>

<span data-ttu-id="27cbd-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="27cbd-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="27cbd-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="27cbd-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="27cbd-111">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="27cbd-111">Applies to</span></span>

[<span data-ttu-id="27cbd-112">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="27cbd-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="27cbd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27cbd-113">Remarks</span></span>

<span data-ttu-id="27cbd-114">Dieses Attribut ist nur für Deinterlacing-Beispiele gültig.</span><span class="sxs-lookup"><span data-stu-id="27cbd-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="27cbd-115">Legen Sie dieses Attribut fest, wenn der Frame durch Interpolation eines der Felder deinstaliert wurde.</span><span class="sxs-lookup"><span data-stu-id="27cbd-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="27cbd-116">Wenn der Wert **true** ist, wurde das untere Feld aus dem oberen Feld interpoliert.</span><span class="sxs-lookup"><span data-stu-id="27cbd-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="27cbd-117">Wenn der Wert **false** ist, wurde das obere Feld aus dem unteren Feld interpoliert.</span><span class="sxs-lookup"><span data-stu-id="27cbd-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="27cbd-118">Wenn das-Attribut nicht festgelegt ist, wurde der Frame nicht deinstalterlacing.</span><span class="sxs-lookup"><span data-stu-id="27cbd-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="27cbd-119">Der Frame ist entweder ein echter progressiver Frame, oder es handelt sich um einen verschachtelten Frame.</span><span class="sxs-lookup"><span data-stu-id="27cbd-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="27cbd-120">Dieses Attribut dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="27cbd-120">This attribute is informational.</span></span> <span data-ttu-id="27cbd-121">Ein Software-Deinterlacer konnte dieses Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="27cbd-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="27cbd-122">Wenn dieses Attribut festgelegt ist, gibt es einen Hinweis, dass Sie das ursprüngliche Feld wiederherstellen können, indem Sie die interpoliert-Scan Zeilen ablegen.</span><span class="sxs-lookup"><span data-stu-id="27cbd-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="27cbd-123">Wenn das Attribut z. b. **true** ist, können Sie das ursprüngliche obere Feld Wiederherstellen, indem Sie das interpoliert untere Feld ablegen.</span><span class="sxs-lookup"><span data-stu-id="27cbd-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="27cbd-124">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="27cbd-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="27cbd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27cbd-125">Requirements</span></span>



| <span data-ttu-id="27cbd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27cbd-126">Requirement</span></span> | <span data-ttu-id="27cbd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27cbd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27cbd-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27cbd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="27cbd-129">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="27cbd-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="27cbd-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27cbd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="27cbd-131">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="27cbd-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="27cbd-132">Header</span><span class="sxs-lookup"><span data-stu-id="27cbd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="27cbd-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="27cbd-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27cbd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27cbd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cbd-135">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="27cbd-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27cbd-136">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="27cbd-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="27cbd-137">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="27cbd-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="27cbd-138">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="27cbd-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




