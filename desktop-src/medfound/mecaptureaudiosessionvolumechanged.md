---
description: Wird von einer audioerfassungs Quelle gesendet, wenn das Volume geändert wird.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Mecaptureaudiosessionvolumechaning-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356546"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="2aa13-103">Mecaptureaudiosessionvolumechaning-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2aa13-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="2aa13-104">Wird von einer audioerfassungs Quelle gesendet, wenn das Volume geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2aa13-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="2aa13-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="2aa13-105">Event values</span></span>

<span data-ttu-id="2aa13-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="2aa13-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2aa13-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2aa13-107">VARTYPE</span></span>               | <span data-ttu-id="2aa13-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2aa13-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="2aa13-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="2aa13-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="2aa13-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="2aa13-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2aa13-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aa13-111">Remarks</span></span>

<span data-ttu-id="2aa13-112">Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.</span><span class="sxs-lookup"><span data-stu-id="2aa13-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="2aa13-113">Die audioerfassungs Quelle sendet dieses Ereignis, wenn das Volume durch eine externe Aktion geändert wird – z. b. wenn der Benutzer das Volume über die Systemsteuerung ändert.</span><span class="sxs-lookup"><span data-stu-id="2aa13-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="2aa13-114">Die Erfassungs Quelle sendet das Ereignis nicht, wenn die Anwendung das Volume direkt in der Quelle ändert.</span><span class="sxs-lookup"><span data-stu-id="2aa13-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa13-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2aa13-115">Requirements</span></span>



| <span data-ttu-id="2aa13-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2aa13-116">Requirement</span></span> | <span data-ttu-id="2aa13-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2aa13-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa13-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2aa13-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa13-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aa13-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="2aa13-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2aa13-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa13-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aa13-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2aa13-122">Header</span><span class="sxs-lookup"><span data-stu-id="2aa13-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa13-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa13-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa13-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aa13-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa13-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2aa13-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




