---
description: Enthält den Bezeichner des Wiedergabelisten Elements in der Präsentation.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359551"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="9ffdf-103">\_Attribut- \_ ID \_ - \_ Attribut der MF-PD</span><span class="sxs-lookup"><span data-stu-id="9ffdf-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="9ffdf-104">Enthält den Bezeichner des Wiedergabelisten Elements in der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="9ffdf-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9ffdf-105">Data type</span></span>

<span data-ttu-id="9ffdf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9ffdf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9ffdf-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9ffdf-107">Get/set</span></span>

<span data-ttu-id="9ffdf-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9ffdf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9ffdf-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9ffdf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9ffdf-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="9ffdf-110">Applies to</span></span>

[<span data-ttu-id="9ffdf-111">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="9ffdf-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="9ffdf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ffdf-112">Remarks</span></span>

<span data-ttu-id="9ffdf-113">Medienquellen, die Wiedergabelisten übermitteln, können dieses Attribut optional für die Präsentations Deskriptoren festlegen.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="9ffdf-114">Wenn eine Medienquelle eine Wiedergabeliste bereitstellt, sendet Sie ein [menewpresentation](menewpresentation.md) -Ereignis für jedes Wiedergabelisten Element nach dem ersten.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="9ffdf-115">Dieses Ereignis enthält einen Präsentations Deskriptor für das neue Wiedergabelisten Element.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="9ffdf-116">Die Medienquelle kann den Elementen Bezeichner zuweisen, indem Sie \_ \_ \_ \_ für jeden Präsentations Deskriptor, einschließlich der von [**imfmediasource:: kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)erstellten, das Attribut "MF PD Playback" ID-Attribut, festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="9ffdf-117">Eine Medienquelle kann das [menewpresentation](menewpresentation.md) -Ereignis auch aufgrund eines dynamischen streamschalters oder einer Änderung in der Anzahl der Streams senden.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="9ffdf-118">In dieser Situation sollte der Wert der MF-ID für die \_ \_ Wiedergabe \_ Element-ID in \_ beiden Präsentationen gleich bleiben, um anzugeben, dass beide Präsentationen dasselbe Wiedergabelisten Element darstellen.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="9ffdf-119">Wenn zwei aufeinander folgende Präsentationen denselben Wert für dieses Attribut aufweisen, erwartet die Microsoft Media Foundation Pipeline, dass die Zeitstempel während des Übergangs fortlaufend bleiben.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="9ffdf-120">Daher darf die Medienquelle das [ \_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle](mf-event-source-actual-start-attribute.md) nicht verwenden, wenn Sie zur nächsten Präsentation übergeht.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="9ffdf-121">Medienquellen, die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) implementieren, sollten das Element " [MF \_ toponode \_ Sequence \_ elementId](mf-toponode-sequence-elementid-attribute.md) " anstelle des "MF PD"- \_ \_ \_ \_ Attributs "ID" verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="9ffdf-122">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9ffdf-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffdf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ffdf-123">Requirements</span></span>



| <span data-ttu-id="9ffdf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ffdf-124">Requirement</span></span> | <span data-ttu-id="9ffdf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9ffdf-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffdf-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ffdf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffdf-127">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9ffdf-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9ffdf-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ffdf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffdf-129">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9ffdf-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9ffdf-130">Header</span><span class="sxs-lookup"><span data-stu-id="9ffdf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ffdf-131"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffdf-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffdf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ffdf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffdf-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9ffdf-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ffdf-134">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="9ffdf-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




