---
description: Wird vom audiorenderer ausgelöst, wenn die Verbindung zwischen der Audiositzung und einer Windows-Terminaldienstesitzung (WTS) getrennt ist. Der audiorenderer ist nun ungültig.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Meaudiosessiongetrennte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db2d31349585d26c61cb2940cea70ddaf0617901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347001"
---
# <a name="meaudiosessiondisconnected-event"></a><span data-ttu-id="ccd83-104">Meaudiosessiongetrennte-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ccd83-104">MEAudioSessionDisconnected event</span></span>

<span data-ttu-id="ccd83-105">Wird vom audiorenderer ausgelöst, wenn die Verbindung zwischen der Audiositzung und einer Windows-Terminaldienstesitzung (WTS) getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="ccd83-105">Raised by the audio renderer when the audio session is disconnected from a Windows Terminal Services (WTS) session.</span></span> <span data-ttu-id="ccd83-106">Der audiorenderer ist nun ungültig.</span><span class="sxs-lookup"><span data-stu-id="ccd83-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="ccd83-107">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="ccd83-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="ccd83-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ccd83-108">Event values</span></span>

<span data-ttu-id="ccd83-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ccd83-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ccd83-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ccd83-110">VARTYPE</span></span>                | <span data-ttu-id="ccd83-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccd83-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd83-112">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="ccd83-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="ccd83-113">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ccd83-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="ccd83-114">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="ccd83-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="ccd83-115">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ccd83-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ccd83-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccd83-116">Remarks</span></span>

<span data-ttu-id="ccd83-117">Dieses Ereignis wird von der streamsenke des audiorenderer gesendet.</span><span class="sxs-lookup"><span data-stu-id="ccd83-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="ccd83-118">Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund gleich disconnectionsonsessiontrennt ist.</span><span class="sxs-lookup"><span data-stu-id="ccd83-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonSessionDisconnected.</span></span>

<span data-ttu-id="ccd83-119">Der [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Zeiger ist, wenn er festgelegt ist, nicht nützlich, da der Audiodatenstrom nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ccd83-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd83-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccd83-120">Requirements</span></span>



| <span data-ttu-id="ccd83-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccd83-121">Requirement</span></span> | <span data-ttu-id="ccd83-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ccd83-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd83-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccd83-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd83-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd83-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccd83-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccd83-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd83-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccd83-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccd83-127">Header</span><span class="sxs-lookup"><span data-stu-id="ccd83-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd83-128"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccd83-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd83-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccd83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd83-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccd83-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ccd83-131">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="ccd83-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
