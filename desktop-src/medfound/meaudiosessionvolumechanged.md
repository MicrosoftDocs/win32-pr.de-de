---
description: Wird vom streamingaudiorenderer (SAR) gesendet, wenn sich das Volume oder der stumm Zustand der Audiositzung ändert.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Meaudiosessionvolumechaning-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359897"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="b211d-103">Meaudiosessionvolumechaning-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b211d-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="b211d-104">Wird vom streamingaudiorenderer (SAR) gesendet, wenn sich das Volume oder der stumm Zustand der Audiositzung ändert.</span><span class="sxs-lookup"><span data-stu-id="b211d-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="b211d-105">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="b211d-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="b211d-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="b211d-106">Event values</span></span>

<span data-ttu-id="b211d-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="b211d-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b211d-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b211d-108">VARTYPE</span></span>                | <span data-ttu-id="b211d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b211d-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b211d-110">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="b211d-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="b211d-111">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="b211d-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="b211d-112">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="b211d-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="b211d-113">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b211d-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b211d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b211d-114">Remarks</span></span>

<span data-ttu-id="b211d-115">Dieses Ereignis wird von der streamsenke der SAR ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b211d-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="b211d-116">Das Ereignis wird ausgelöst, wenn der SAR ein [**iaudiosessionevents:: onsimplevolumechaning**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) -Ereignis aus der Audiositzung empfängt.</span><span class="sxs-lookup"><span data-stu-id="b211d-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="b211d-117">Um die neue Volumeebene abzurufen und den Zustand stumm zu schalten, nennen Sie [**imfsimpleaudiovolume:: getmastervolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) und [**imfsimpleaudiovolume:: getstumm**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="b211d-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="b211d-118">Der SAR sendet dieses Ereignis, wenn das Volume durch eine externe Aktion geändert wird – z. b. wenn der Benutzer das Volume über das System Volume-Control Program (sndvol) ändert.</span><span class="sxs-lookup"><span data-stu-id="b211d-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="b211d-119">Der SAR sendet das Ereignis nicht, wenn die Anwendung das Volume direkt in der SAR ändert.</span><span class="sxs-lookup"><span data-stu-id="b211d-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="b211d-120">Außerdem sendet der SAR dieses Ereignis nicht, wenn sich das Kanal Volume ändert ([**iaudiosessionevents:: onchannelvolumechaning**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="b211d-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b211d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b211d-121">Requirements</span></span>



| <span data-ttu-id="b211d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b211d-122">Requirement</span></span> | <span data-ttu-id="b211d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b211d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b211d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b211d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b211d-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b211d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b211d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b211d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b211d-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b211d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b211d-128">Header</span><span class="sxs-lookup"><span data-stu-id="b211d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b211d-129"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b211d-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b211d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b211d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b211d-131">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b211d-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b211d-132">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="b211d-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
