---
description: Wird vom audiorenderer ausgelöst, wenn sich das Symbol für die Audiositzung ändert.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Meaudiosessionieschanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350493"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="0b8b6-103">Meaudiosessionieschanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0b8b6-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="0b8b6-104">Wird vom audiorenderer ausgelöst, wenn sich das Symbol für die Audiositzung ändert.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="0b8b6-105">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0b8b6-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="0b8b6-106">Event values</span></span>

<span data-ttu-id="0b8b6-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0b8b6-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0b8b6-108">VARTYPE</span></span>                | <span data-ttu-id="0b8b6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b8b6-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b6-110">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="0b8b6-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="0b8b6-111">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="0b8b6-112">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="0b8b6-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0b8b6-113">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0b8b6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b8b6-114">Remarks</span></span>

<span data-ttu-id="0b8b6-115">Dieses Ereignis wird von der streamsenke des audiorenderer gesendet.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="0b8b6-116">Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: oniconpathchanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) -Ereignis von der Audiositzung empfängt.</span><span class="sxs-lookup"><span data-stu-id="0b8b6-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="0b8b6-117">Um das neue Symbol abzurufen, nennen Sie [**imfaudiopolicy:: geticopath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="0b8b6-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8b6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b8b6-118">Requirements</span></span>



| <span data-ttu-id="0b8b6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b8b6-119">Requirement</span></span> | <span data-ttu-id="0b8b6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0b8b6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b8b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b8b6-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b8b6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b8b6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b8b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b8b6-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b8b6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b8b6-125">Header</span><span class="sxs-lookup"><span data-stu-id="0b8b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b8b6-126"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b8b6-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b8b6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8b6-128">**Imbaudiopolicy:: getirepath**</span><span class="sxs-lookup"><span data-stu-id="0b8b6-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="0b8b6-129">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b8b6-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0b8b6-130">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="0b8b6-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
