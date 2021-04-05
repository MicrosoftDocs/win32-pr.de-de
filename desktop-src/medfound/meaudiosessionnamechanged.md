---
description: Wird vom audiorenderer ausgelöst, wenn sich der Anzeige Name der Audiositzung ändert.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Meaudiosessionnamechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752880"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="3d2cd-103">Meaudiosessionnamechanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3d2cd-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="3d2cd-104">Wird vom audiorenderer ausgelöst, wenn sich der Anzeige Name der Audiositzung ändert.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="3d2cd-105">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="3d2cd-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="3d2cd-106">Event values</span></span>

<span data-ttu-id="3d2cd-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3d2cd-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3d2cd-108">VARTYPE</span></span>                | <span data-ttu-id="3d2cd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d2cd-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2cd-110">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="3d2cd-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="3d2cd-111">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3d2cd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d2cd-112">Remarks</span></span>

<span data-ttu-id="3d2cd-113">Dieses Ereignis wird von der streamsenke des audiorenderer gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="3d2cd-114">Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: ondisplaynamechanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) -Ereignis von der Audiositzung empfängt.</span><span class="sxs-lookup"><span data-stu-id="3d2cd-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="3d2cd-115">Um den neuen anzeigen Amen abzurufen, nennen Sie [**imfaudiopolicy:: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span><span class="sxs-lookup"><span data-stu-id="3d2cd-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2cd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d2cd-116">Requirements</span></span>



| <span data-ttu-id="3d2cd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d2cd-117">Requirement</span></span> | <span data-ttu-id="3d2cd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3d2cd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2cd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d2cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2cd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d2cd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d2cd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d2cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2cd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d2cd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d2cd-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d2cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d2cd-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d2cd-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d2cd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d2cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2cd-126">**IMF audiopolicy:: GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="3d2cd-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="3d2cd-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d2cd-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3d2cd-128">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="3d2cd-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
