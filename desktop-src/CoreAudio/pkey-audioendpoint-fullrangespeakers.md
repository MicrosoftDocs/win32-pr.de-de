---
description: Die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127441"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="66067-103">Pkey- \_ audioendpoint \_ fullrangespeakers</span><span class="sxs-lookup"><span data-stu-id="66067-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="66067-104">Die **pkey \_ audioendpoint \_ fullrangespeakers** -Eigenschaft gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="66067-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="66067-105">Die Maske gibt die physische Konfiguration der vollständigen Referenten an und gibt die Zuweisung von Kanälen zu diesen Referenten an.</span><span class="sxs-lookup"><span data-stu-id="66067-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="66067-106">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66067-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="66067-107">Der **uintval** -Member der **PROPVARIANT** -Struktur enthält eine kanalkonfigurationsmaske, die in den **uint**-Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="66067-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="66067-108">Ein Volltext-Redner ist in der Lage, Sounds über den vollen Bereich von Bass bis Treble zu spielen.</span><span class="sxs-lookup"><span data-stu-id="66067-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="66067-109">In der Regel sind größere Redner in vollem Umfang, aber kleinere Redner sind deutlich weniger in der Lage, Bass Sounds wiedergeben zu können.</span><span class="sxs-lookup"><span data-stu-id="66067-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="66067-110">In Windows Vista verwendet die Audioengine diese Eigenschaft zum Verwalten von Bass Ebenen im audioausgabestream, der vom audioendpunktgerät wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="66067-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="66067-111">Die Kanal konfigurationsmaske für diese Eigenschaft hat das gleiche Format wie die channelkonfigurationsmaske für die [**pkey \_ audioendpoint \_ physicalspeakers**](pkey-audioendpoint-physicalspeakers.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="66067-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="66067-112">Weitere Informationen zu kanalkonfigurationsmasken finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="66067-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="66067-113">Die Beschreibung der Eigenschaft "ksproperty \_ \_ AudioChannel \_ config" in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="66067-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="66067-114">Das Whitepaper "audiotreiberunterstützung für Home-Theater-Sprecher-Konfigurationen" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".</span><span class="sxs-lookup"><span data-stu-id="66067-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="66067-115">Das System ruft die Kanal konfigurationsmaske für die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="66067-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="66067-116">Der Benutzer gibt diese Informationen über die Windows-Multimedia-Systemsteuerung ein, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="66067-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="66067-117">Weitere Informationen zu Mmsys.cpl finden Sie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="66067-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="66067-118">Die Kanal konfigurationsmaske für die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft eines audioendpunktgeräts ist eine Teilmenge der channelkonfigurationsmaske für die pkey \_ audioendpoint \_ physicalspeakers-Eigenschaft desselben Geräts.</span><span class="sxs-lookup"><span data-stu-id="66067-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="66067-119">Wenn ein audioendpunktgerät beispielsweise einen Satz von 5,1-umschließenden Lautsprechern steuert, ist die channelkonfigurationsmaske für die pkey \_ audioendpoint \_ physicalspeakers-Eigenschaft der ksaudio- \_ Sprecher \_ 5point1.</span><span class="sxs-lookup"><span data-stu-id="66067-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="66067-120">Diese Maske gibt das vorhanden sein von Front-Left, Front-Right, Front-Center, Side-Left und Side-right Speakers – plus eines Subwoofers an.</span><span class="sxs-lookup"><span data-stu-id="66067-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="66067-121">Wenn die nach-links-und Front-Right-Redner groß genug sind, um Bass Sounds zu bilden, aber die kleineren Front-Center-und Seite-Sprecher sind nicht, dann ist die channelkonfigurationsmaske für die pkey- \_ audioendpoint \_ fullrangespeakers-Eigenschaft ksaudio- \_ Sprecher \_ Stereo, der nur die Front-Left-und Front-Right-Sprecher anzeigt.</span><span class="sxs-lookup"><span data-stu-id="66067-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="66067-122">Kanalkonfigurationsmasken \_ der ksaudiosprecher \_ 5point1 und \_ ksaudiosprecherstereo \_ sind in der Header Datei "ksmedia. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="66067-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="66067-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66067-123">Requirements</span></span>



| <span data-ttu-id="66067-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66067-124">Requirement</span></span> | <span data-ttu-id="66067-125">Wert</span><span class="sxs-lookup"><span data-stu-id="66067-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66067-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66067-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66067-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66067-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="66067-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66067-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66067-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66067-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66067-130">Header</span><span class="sxs-lookup"><span data-stu-id="66067-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="66067-131"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66067-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66067-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66067-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66067-133">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="66067-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="66067-134">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="66067-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="66067-135">**Pkey \_ audioendpoint \_ physicalspeakers (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="66067-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




