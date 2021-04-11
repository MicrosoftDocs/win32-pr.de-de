---
description: Wird durch eine streamsenke ausgelöst, wenn der senken-Medientyp nicht mehr gültig ist.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Mestreamsinkformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215158"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="0aaed-103">Mestreamsinkformatchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0aaed-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="0aaed-104">Wird durch eine streamsenke ausgelöst, wenn der Medientyp der Senke nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0aaed-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="0aaed-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="0aaed-105">Event values</span></span>

<span data-ttu-id="0aaed-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="0aaed-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0aaed-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0aaed-107">VARTYPE</span></span>              | <span data-ttu-id="0aaed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aaed-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0aaed-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="0aaed-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0aaed-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="0aaed-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0aaed-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aaed-111">Remarks</span></span>

<span data-ttu-id="0aaed-112">Eine streamsenke kann dies auch dann auslösen, wenn etwas passiert, das den Medientyp der Stream-Senke ungültig macht.</span><span class="sxs-lookup"><span data-stu-id="0aaed-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="0aaed-113">Beispielsweise sendet der erweiterte Videorenderer (EVR) dieses Ereignis, wenn die Anzeige geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0aaed-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="0aaed-114">Der **HRESULT** -Wert, der von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) abgerufen wird, kann darauf hinweisen, warum der Medientyp nicht mehr gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0aaed-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aaed-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0aaed-115">Requirements</span></span>



| <span data-ttu-id="0aaed-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0aaed-116">Requirement</span></span> | <span data-ttu-id="0aaed-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0aaed-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aaed-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0aaed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0aaed-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aaed-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0aaed-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0aaed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0aaed-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0aaed-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0aaed-122">Header</span><span class="sxs-lookup"><span data-stu-id="0aaed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aaed-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aaed-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aaed-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aaed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aaed-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0aaed-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0aaed-126">Medien senken</span><span class="sxs-lookup"><span data-stu-id="0aaed-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




