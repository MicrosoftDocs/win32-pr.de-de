---
description: 'Signalisiert einen schwerwiegenden Fehler. Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden. Wenn Sie imfmediaevent:: GetStatus aufrufen, erhalten Sie den Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Meerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356868"
---
# <a name="meerror-event"></a><span data-ttu-id="61351-105">Meerror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="61351-105">MEError event</span></span>

<span data-ttu-id="61351-106">Signalisiert einen schwerwiegenden Fehler.</span><span class="sxs-lookup"><span data-stu-id="61351-106">Signals a serious error.</span></span> <span data-ttu-id="61351-107">Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden.</span><span class="sxs-lookup"><span data-stu-id="61351-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="61351-108">[**Wenn Sie imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) aufrufen, erhalten Sie den Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="61351-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="61351-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="61351-109">Event values</span></span>

<span data-ttu-id="61351-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="61351-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="61351-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61351-111">VARTYPE</span></span>              | <span data-ttu-id="61351-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61351-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="61351-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="61351-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="61351-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="61351-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="61351-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61351-115">Remarks</span></span>

<span data-ttu-id="61351-116">Dieses Ereignis sollte nur für unerwartete Fehler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61351-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="61351-117">Senden Sie dieses Ereignis nicht, um zu signalisieren, dass eine asynchrone Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="61351-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="61351-118">Wenn eine asynchrone Methode fehlschlägt, wird der Fehlercode im normalen Ereignis für diese Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61351-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="61351-119">Wenn beim Streaming ein BEHEB barer Fehler auftritt, senden Sie das [menonfatalerror](menonfatalerror.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="61351-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="61351-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61351-120">Requirements</span></span>



| <span data-ttu-id="61351-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61351-121">Requirement</span></span> | <span data-ttu-id="61351-122">Wert</span><span class="sxs-lookup"><span data-stu-id="61351-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61351-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61351-123">Minimum supported client</span></span><br/> | <span data-ttu-id="61351-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61351-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="61351-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61351-125">Minimum supported server</span></span><br/> | <span data-ttu-id="61351-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61351-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="61351-127">Header</span><span class="sxs-lookup"><span data-stu-id="61351-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="61351-128"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61351-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61351-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61351-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61351-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61351-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




