---
description: Gibt an, ob das erste Feld in einem Zeilen Sprung Rahmen wiederholt werden soll. Dieses Attribut gilt für Medien Beispiele.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130520"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="85d72-104">MF Sample Extension \_ repeatfirstfield-Attribut</span><span class="sxs-lookup"><span data-stu-id="85d72-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="85d72-105">Gibt an, ob das erste Feld in einem Zeilen Sprung Rahmen wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="85d72-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="85d72-106">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="85d72-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="85d72-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="85d72-107">Data type</span></span>

<span data-ttu-id="85d72-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85d72-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="85d72-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="85d72-109">Get/set</span></span>

<span data-ttu-id="85d72-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="85d72-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="85d72-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="85d72-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="85d72-112">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="85d72-112">Applies to</span></span>

[<span data-ttu-id="85d72-113">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="85d72-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="85d72-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85d72-114">Remarks</span></span>

<span data-ttu-id="85d72-115">Wenn der Wert **false** ist oder das-Attribut nicht festgelegt ist, wird das erste Feld nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="85d72-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="85d72-116">Wenn der Wert **true** ist, wird das erste Feld wiederholt.</span><span class="sxs-lookup"><span data-stu-id="85d72-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="85d72-117">Der Wert **true** ist nur gültig, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="85d72-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="85d72-118">Der Medientyp ist gemischt und progressiv.</span><span class="sxs-lookup"><span data-stu-id="85d72-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="85d72-119">(Das Attribut " [**MF \_ MT \_ Interlace \_ Mode**](mf-mt-interlace-mode-attribute.md) " für den Medientyp ist " **MF videointerlace \_ mixedinterlaceorprogressive**").</span><span class="sxs-lookup"><span data-stu-id="85d72-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="85d72-120">Der Frame ist progressiv, und das [**\_ interschnür Attribut "mfsampleextension**](mfsampleextension-interlaced-attribute.md) " im Beispiel ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="85d72-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="85d72-121">Das Attribut " [**MF SampleExtension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md) " ist für das Beispiel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85d72-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="85d72-122">Der Wert kann " **true** " oder " **false**" sein.</span><span class="sxs-lookup"><span data-stu-id="85d72-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="85d72-123">Die Reihenfolge der Felder wird durch dieses Attribut bestimmt.</span><span class="sxs-lookup"><span data-stu-id="85d72-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="85d72-124">Dieses Attribut wird für 3:2 Pulldown verwendet.</span><span class="sxs-lookup"><span data-stu-id="85d72-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="85d72-125">In der folgenden Tabelle wird die Reihenfolge angezeigt, in der Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="85d72-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="85d72-126">MF Sample Extension \_ repeatfirstfield</span><span class="sxs-lookup"><span data-stu-id="85d72-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="85d72-127">MF Sample Extension \_ bottomfieldfirst</span><span class="sxs-lookup"><span data-stu-id="85d72-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="85d72-128">Feld Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="85d72-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="85d72-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85d72-129">**TRUE**</span></span>                            | <span data-ttu-id="85d72-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85d72-130">**TRUE**</span></span>                            | <span data-ttu-id="85d72-131">Niedriger, oberer, niedriger</span><span class="sxs-lookup"><span data-stu-id="85d72-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="85d72-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85d72-132">**TRUE**</span></span>                            | <span data-ttu-id="85d72-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85d72-133">**FALSE**</span></span>                           | <span data-ttu-id="85d72-134">Upper, Lower, Upper</span><span class="sxs-lookup"><span data-stu-id="85d72-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="85d72-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85d72-135">**FALSE**</span></span>                           | <span data-ttu-id="85d72-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85d72-136">**TRUE**</span></span>                            | <span data-ttu-id="85d72-137">Niedriger, oberer</span><span class="sxs-lookup"><span data-stu-id="85d72-137">Lower, upper</span></span>        |
| <span data-ttu-id="85d72-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85d72-138">**FALSE**</span></span>                           | <span data-ttu-id="85d72-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85d72-139">**FALSE**</span></span>                           | <span data-ttu-id="85d72-140">Obere, untere</span><span class="sxs-lookup"><span data-stu-id="85d72-140">Upper, lower</span></span>        |



 

<span data-ttu-id="85d72-141">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="85d72-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d72-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85d72-142">Requirements</span></span>



| <span data-ttu-id="85d72-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85d72-143">Requirement</span></span> | <span data-ttu-id="85d72-144">Wert</span><span class="sxs-lookup"><span data-stu-id="85d72-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85d72-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85d72-145">Minimum supported client</span></span><br/> | <span data-ttu-id="85d72-146">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="85d72-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="85d72-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85d72-147">Minimum supported server</span></span><br/> | <span data-ttu-id="85d72-148">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="85d72-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="85d72-149">Header</span><span class="sxs-lookup"><span data-stu-id="85d72-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="85d72-150"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d72-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85d72-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85d72-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d72-152">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="85d72-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85d72-153">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="85d72-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="85d72-154">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="85d72-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="85d72-155">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="85d72-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




