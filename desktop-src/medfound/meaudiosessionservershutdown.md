---
description: Wird vom audiorenderer ausgelöst, wenn das Windows-audioserversystem heruntergefahren wird. Der audiorenderer ist nun ungültig.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Meaudiosessionservershutdown-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345778"
---
# <a name="meaudiosessionservershutdown-event"></a><span data-ttu-id="15354-104">Meaudiosessionservershutdown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="15354-104">MEAudioSessionServerShutdown event</span></span>

<span data-ttu-id="15354-105">Wird vom audiorenderer ausgelöst, wenn das Windows-audioserversystem heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="15354-105">Raised by the audio renderer when the Windows audio server system is shut down.</span></span> <span data-ttu-id="15354-106">Der audiorenderer ist nun ungültig.</span><span class="sxs-lookup"><span data-stu-id="15354-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="15354-107">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="15354-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="15354-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="15354-108">Event values</span></span>

<span data-ttu-id="15354-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="15354-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="15354-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="15354-110">VARTYPE</span></span>                | <span data-ttu-id="15354-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15354-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="15354-112">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="15354-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="15354-113">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="15354-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="15354-114">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="15354-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="15354-115">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="15354-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="15354-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15354-116">Remarks</span></span>

<span data-ttu-id="15354-117">Dieses Ereignis wird von der streamsenke des audiorenderer gesendet.</span><span class="sxs-lookup"><span data-stu-id="15354-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="15354-118">Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis aus der Audiositzung empfängt, bei dem der Trennungsgrund gleich " **disconnectsonservershutdown**" ist.</span><span class="sxs-lookup"><span data-stu-id="15354-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonServerShutdown**.</span></span>

<span data-ttu-id="15354-119">Der [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Zeiger ist, wenn er festgelegt ist, nicht nützlich, da der Audiodatenstrom nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="15354-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="15354-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15354-120">Requirements</span></span>



| <span data-ttu-id="15354-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15354-121">Requirement</span></span> | <span data-ttu-id="15354-122">Wert</span><span class="sxs-lookup"><span data-stu-id="15354-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15354-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15354-123">Minimum supported client</span></span><br/> | <span data-ttu-id="15354-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15354-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15354-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15354-125">Minimum supported server</span></span><br/> | <span data-ttu-id="15354-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15354-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15354-127">Header</span><span class="sxs-lookup"><span data-stu-id="15354-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="15354-128"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15354-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15354-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15354-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15354-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15354-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="15354-131">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="15354-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
