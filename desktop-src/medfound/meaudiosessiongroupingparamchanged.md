---
description: Wird vom audiorenderer ausgelöst, wenn sich die Gruppierungs Parameter für die Audiositzung ändern.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Meaudiosessiongroupingparamchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214840"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="a6ce2-103">Meaudiosessiongroupingparamchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a6ce2-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="a6ce2-104">Wird vom audiorenderer ausgelöst, wenn sich die Gruppierungs Parameter für die Audiositzung ändern.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="a6ce2-105">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="a6ce2-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="a6ce2-106">Event values</span></span>

<span data-ttu-id="a6ce2-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a6ce2-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a6ce2-108">VARTYPE</span></span>                | <span data-ttu-id="a6ce2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6ce2-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ce2-110">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="a6ce2-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="a6ce2-111">Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a6ce2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6ce2-112">Remarks</span></span>

<span data-ttu-id="a6ce2-113">Dieses Ereignis wird von der streamsenke des audiorenderer gesendet.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="a6ce2-114">Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: ongroupingparamchanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) -Ereignis von der Audiositzung empfängt.</span><span class="sxs-lookup"><span data-stu-id="a6ce2-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="a6ce2-115">Um die neuen Gruppierungs Parameter abzurufen, nennen Sie [**imfaudiopolicy:: getgroupingparam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="a6ce2-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ce2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6ce2-116">Requirements</span></span>



| <span data-ttu-id="a6ce2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6ce2-117">Requirement</span></span> | <span data-ttu-id="a6ce2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a6ce2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ce2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6ce2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ce2-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6ce2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a6ce2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6ce2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ce2-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6ce2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6ce2-123">Header</span><span class="sxs-lookup"><span data-stu-id="a6ce2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ce2-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ce2-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ce2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6ce2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ce2-126">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6ce2-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a6ce2-127">**IMF audiopolicy:: getgroupingparam**</span><span class="sxs-lookup"><span data-stu-id="a6ce2-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="a6ce2-128">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="a6ce2-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
