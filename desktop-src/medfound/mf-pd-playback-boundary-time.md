---
description: Speichert die Zeit (in 100-Nanosekunden-Einheiten), bei der die Präsentation beginnen muss, relativ zum Anfang der Medienquelle.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: MF_PD_PLAYBACK_BOUNDARY_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050500"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="15190-103">MF \_ - \_ \_ \_ Zeit Attribut für die Wiedergabe von Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="15190-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="15190-104">Speichert die Zeit (in 100-Nanosekunden-Einheiten), bei der die Präsentation beginnen muss, relativ zum Anfang der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="15190-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="15190-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="15190-105">Data type</span></span>

<span data-ttu-id="15190-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="15190-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="15190-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="15190-107">Get/set</span></span>

<span data-ttu-id="15190-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="15190-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="15190-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="15190-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="15190-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="15190-110">Applies to</span></span>

[<span data-ttu-id="15190-111">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="15190-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="15190-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15190-112">Remarks</span></span>

<span data-ttu-id="15190-113">Das MF \_ - \_ \_ \_ Zeit Attribut für die Zeit Wiedergabe Begrenzung ist für Medienquellen in einer Wiedergabeliste optional.</span><span class="sxs-lookup"><span data-stu-id="15190-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="15190-114">Dieser Wert gibt die tatsächliche Startzeit der Präsentation an.</span><span class="sxs-lookup"><span data-stu-id="15190-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="15190-115">Angenommen, eine Wiedergabeliste enthält Medienquellen *Element1*, *Element2* und *Element3* in einer Sequenz.</span><span class="sxs-lookup"><span data-stu-id="15190-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="15190-116">15 Sekunden nach dem Start der *Element1* -Wiedergabe tritt eine dynamische Datenstrom Änderung auf.</span><span class="sxs-lookup"><span data-stu-id="15190-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="15190-117">Der neue Stream muss 15 Sekunden in der Präsentation wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="15190-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="15190-118">Der Keyframe, der der Präsentationszeit von 15 Sekunden am nächsten liegt, liegt jedoch bei 12 Sekunden für den neuen Stream.</span><span class="sxs-lookup"><span data-stu-id="15190-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="15190-119">Um die neue Präsentation 15 Sekunden zu starten, ist ein Markin erforderlich, damit die decodierten Stichproben von 12 Sekunden auf 15 Sekunden abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="15190-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="15190-120">Vor der Umstellung wird das Ereignis [menewpresentation](menewpresentation.md) von der Medienquelle ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="15190-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="15190-121">Dadurch wird der Präsentations Deskriptor zurückgegeben, der das [MF- \_ \_ \_ Element \_ ID](mf-pd-playback-element-id.md) -Attribut für *Element1* enthält.</span><span class="sxs-lookup"><span data-stu-id="15190-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="15190-122">Darüber hinaus enthält es das Attribut für die Begrenzung der MF- \_ \_ Zeit Wiedergabe Begrenzung, \_ \_ das auf 15 Sekunden festgelegt ist, um den Zeitpunkt der Umstellung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="15190-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="15190-123">Die Medienquelle führt das Markin nach 15 Sekunden nach der Decodierung aus, sodass die Anzeige von Frames von 12 Sekunden auf 15 Sekunden verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="15190-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="15190-124">Dieser Wert wirkt sich nur auf die Markin-Zeit aus und wirkt sich nicht darauf aus, wie die Medien Sitzung Zeitstempel anpasst.</span><span class="sxs-lookup"><span data-stu-id="15190-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="15190-125">Dieses Attribut wird ignoriert, es sei denn, die Medienquelle gibt durch das [MF PD-Attribut \_ \_ \_ \_ ID](mf-pd-playback-element-id.md) -Attribut an, dass diese Präsentation das gleiche Wiedergabe Element wie das vorherige Element ist.</span><span class="sxs-lookup"><span data-stu-id="15190-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="15190-126">Das MF-Attribut für die \_ \_ wiederwiedergabe Begrenzung \_ \_ ist vergleichbar mit dem MF-Attribut " [ \_ toponode \_ mediastart](mf-toponode-mediastart-attribute.md) ", das für den topologieknoten festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="15190-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="15190-127">Für Anwendungen, die unter Windows Vista ausgeführt werden, sollten Medienquellen, die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) implementieren, **MF \_ toponode \_ mediastart** anstelle von MF- \_ \_ \_ Zeit Wiedergabe Begrenzungs \_ Zeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="15190-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="15190-128">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="15190-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15190-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15190-129">Requirements</span></span>



| <span data-ttu-id="15190-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15190-130">Requirement</span></span> | <span data-ttu-id="15190-131">Wert</span><span class="sxs-lookup"><span data-stu-id="15190-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15190-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15190-132">Minimum supported client</span></span><br/> | <span data-ttu-id="15190-133">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="15190-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="15190-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15190-134">Minimum supported server</span></span><br/> | <span data-ttu-id="15190-135">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="15190-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="15190-136">Header</span><span class="sxs-lookup"><span data-stu-id="15190-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="15190-137"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15190-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15190-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15190-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15190-139">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="15190-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15190-140">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="15190-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




