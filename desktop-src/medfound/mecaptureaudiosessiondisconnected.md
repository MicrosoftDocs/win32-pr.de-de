---
description: Wird von einer audioerfassungs Quelle gesendet, wenn die audioumzierung getrennt wird, weil der Benutzer von einer Windows-Terminal Dienste-Sitzung (WTS) abgemeldet wurde.
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Mecaptureaudiosessiongetrennte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130036"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="12796-103">Mecaptureaudiosessiongetrennte-Ereignis</span><span class="sxs-lookup"><span data-stu-id="12796-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="12796-104">Wird von einer audioerfassungs Quelle gesendet, wenn die audioumzierung getrennt wird, weil der Benutzer von einer Windows-Terminal Dienste-Sitzung (WTS) abgemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="12796-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="12796-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="12796-105">Event values</span></span>

<span data-ttu-id="12796-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="12796-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="12796-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="12796-107">VARTYPE</span></span>               | <span data-ttu-id="12796-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12796-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="12796-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="12796-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="12796-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="12796-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="12796-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12796-111">Remarks</span></span>

<span data-ttu-id="12796-112">Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.</span><span class="sxs-lookup"><span data-stu-id="12796-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="12796-113">Die Erfassungs Quelle sendet dieses Ereignis, wenn es ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund " **disconnecsquonsessiongetrennte**" entspricht.</span><span class="sxs-lookup"><span data-stu-id="12796-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="12796-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12796-114">Requirements</span></span>



| <span data-ttu-id="12796-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12796-115">Requirement</span></span> | <span data-ttu-id="12796-116">Wert</span><span class="sxs-lookup"><span data-stu-id="12796-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12796-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12796-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12796-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12796-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="12796-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12796-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12796-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12796-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12796-121">Header</span><span class="sxs-lookup"><span data-stu-id="12796-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="12796-122"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12796-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12796-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12796-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12796-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12796-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
