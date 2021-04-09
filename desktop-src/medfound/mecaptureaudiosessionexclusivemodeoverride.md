---
description: Wird von einer audioerfassungs Quelle gesendet, wenn das Audiogerät von einem anderen Programm im exklusiven Modus geöffnet wird.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Mecaptureaudiosessionexclusivemodeoverride-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751280"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="297d6-103">Mecaptureaudiosessionexclusivemodeoverride-Ereignis</span><span class="sxs-lookup"><span data-stu-id="297d6-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="297d6-104">Wird von einer audioerfassungs Quelle gesendet, wenn das Audiogerät von einem anderen Programm im exklusiven Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="297d6-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="297d6-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="297d6-105">Event values</span></span>

<span data-ttu-id="297d6-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="297d6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="297d6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="297d6-107">VARTYPE</span></span>               | <span data-ttu-id="297d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="297d6-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="297d6-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="297d6-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="297d6-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="297d6-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="297d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="297d6-111">Remarks</span></span>

<span data-ttu-id="297d6-112">Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.</span><span class="sxs-lookup"><span data-stu-id="297d6-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="297d6-113">Die Erfassungs Quelle sendet dieses Ereignis, wenn es ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund gleich **disconnecsquonexclusivemodeoverride** ist.</span><span class="sxs-lookup"><span data-stu-id="297d6-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="297d6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="297d6-114">Requirements</span></span>



| <span data-ttu-id="297d6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="297d6-115">Requirement</span></span> | <span data-ttu-id="297d6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="297d6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297d6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="297d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="297d6-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="297d6-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="297d6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="297d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="297d6-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="297d6-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="297d6-121">Header</span><span class="sxs-lookup"><span data-stu-id="297d6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="297d6-122"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="297d6-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297d6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="297d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297d6-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="297d6-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
