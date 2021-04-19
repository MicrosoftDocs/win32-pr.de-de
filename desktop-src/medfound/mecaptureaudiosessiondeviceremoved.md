---
description: Wird von einer audioerfassungs-Quelle gesendet, wenn das Gerät entfernt wird.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Mecaptureaudiosessiondeviceremoved-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349690"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a><span data-ttu-id="a090b-103">Mecaptureaudiosessiondeviceremoved-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a090b-103">MECaptureAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="a090b-104">Wird von einer audioerfassungs-Quelle gesendet, wenn das Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a090b-104">Sent by an audio capture source when the device is removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="a090b-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="a090b-105">Event values</span></span>

<span data-ttu-id="a090b-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="a090b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a090b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a090b-107">VARTYPE</span></span>               | <span data-ttu-id="a090b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a090b-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="a090b-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="a090b-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="a090b-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="a090b-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a090b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a090b-111">Remarks</span></span>

<span data-ttu-id="a090b-112">Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.</span><span class="sxs-lookup"><span data-stu-id="a090b-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="a090b-113">Die Erfassungs Quelle sendet dieses Ereignis, wenn es ein [**iaudiosessionevents:: onsessiondevi-**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund gleich **disconnecsquondeviceremoval** ist.</span><span class="sxs-lookup"><span data-stu-id="a090b-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a090b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a090b-114">Requirements</span></span>



| <span data-ttu-id="a090b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a090b-115">Requirement</span></span> | <span data-ttu-id="a090b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a090b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a090b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a090b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a090b-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a090b-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a090b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a090b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a090b-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a090b-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a090b-121">Header</span><span class="sxs-lookup"><span data-stu-id="a090b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a090b-122"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a090b-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a090b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a090b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a090b-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a090b-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
