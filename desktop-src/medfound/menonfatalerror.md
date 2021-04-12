---
description: Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Menonfatalerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344619"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="59916-103">Menonfatalerror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="59916-103">MENonFatalError event</span></span>

<span data-ttu-id="59916-104">Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="59916-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="59916-105">Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden.</span><span class="sxs-lookup"><span data-stu-id="59916-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="59916-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="59916-106">Event values</span></span>

<span data-ttu-id="59916-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="59916-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="59916-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="59916-108">VARTYPE</span></span>            | <span data-ttu-id="59916-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59916-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="59916-110">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="59916-110">VT\_UI4</span></span><br/> | <span data-ttu-id="59916-111">**HRESULT** -Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="59916-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="59916-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="59916-112">Attributes</span></span>

<span data-ttu-id="59916-113">Für dieses Ereignis sind keine Attribute definiert.</span><span class="sxs-lookup"><span data-stu-id="59916-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="59916-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59916-114">Remarks</span></span>

<span data-ttu-id="59916-115">Dieses Ereignis signalisiert einen unerwarteten, aber wiederherstellbaren Fehler beim Streaming.</span><span class="sxs-lookup"><span data-stu-id="59916-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="59916-116">Beispielsweise kann eine Medienquelle dieses Ereignis senden, wenn es ein Paket löscht.</span><span class="sxs-lookup"><span data-stu-id="59916-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="59916-117">Senden Sie dieses Ereignis nicht, um zu signalisieren, dass eine asynchrone Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="59916-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="59916-118">Wenn eine asynchrone Methode fehlschlägt, wird der Fehlercode im normalen Ereignis für diese Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59916-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="59916-119">Wenn ein nicht BEHEB barer Streamingfehler auftritt, senden Sie das [meerror](meerror.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="59916-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="59916-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59916-120">Requirements</span></span>



| <span data-ttu-id="59916-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59916-121">Requirement</span></span> | <span data-ttu-id="59916-122">Wert</span><span class="sxs-lookup"><span data-stu-id="59916-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59916-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59916-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59916-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59916-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="59916-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59916-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59916-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59916-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="59916-127">Header</span><span class="sxs-lookup"><span data-stu-id="59916-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59916-128"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59916-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59916-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59916-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59916-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59916-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




