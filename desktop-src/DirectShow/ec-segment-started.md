---
description: Ein neues Segment wurde gestartet.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359242"
---
# <a name="ec_segment_started"></a><span data-ttu-id="050ec-103">EC- \_ Segment \_ gestartet</span><span class="sxs-lookup"><span data-stu-id="050ec-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="050ec-104">Ein neues Segment wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="050ec-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="050ec-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="050ec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="050ec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="050ec-107">(**Konstante** **Verweis \_ Zeit** \* ) Zeiger auf einen **Verweis \_ Zeitwert** , der die akkumulierte streamzeit seit dem Start des Segments in 100-Nanosecond-Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="050ec-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="050ec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="050ec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="050ec-109">(**DWORD**) Segment Nummer (null basiert).</span><span class="sxs-lookup"><span data-stu-id="050ec-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="050ec-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="050ec-110">Default Action</span></span>

<span data-ttu-id="050ec-111">Dieses Ereignis wird nicht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="050ec-111">This event is not sent to the application.</span></span> <span data-ttu-id="050ec-112">Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="050ec-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="050ec-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="050ec-113">Remarks</span></span>

<span data-ttu-id="050ec-114">Wenn ein Filter am Ende eines Segments ein [**EC- \_ Ende \_ des \_ Segments**](ec-end-of-segment.md) sendet, sendet dieses Ereignis am Anfang des Segments.</span><span class="sxs-lookup"><span data-stu-id="050ec-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="050ec-115">Der Filter Graph-Manager verwendet diese Ereignis Benachrichtigung, um zu berechnen, wie viele EC- \_ Ende \_ der \_ Segment Benachrichtigungen am Ende des Segments zu erwarten sind.</span><span class="sxs-lookup"><span data-stu-id="050ec-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="050ec-116">Standardmäßig senden Filter keine EC- [**\_ Ende \_ von \_ Segment**](ec-end-of-segment.md) Ereignissen am Ende von Segmenten und sollten daher dieses Ereignis nicht senden.</span><span class="sxs-lookup"><span data-stu-id="050ec-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="050ec-117">Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="050ec-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="050ec-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="050ec-118">Requirements</span></span>



| <span data-ttu-id="050ec-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="050ec-119">Requirement</span></span> | <span data-ttu-id="050ec-120">Wert</span><span class="sxs-lookup"><span data-stu-id="050ec-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="050ec-121">Header</span><span class="sxs-lookup"><span data-stu-id="050ec-121">Header</span></span><br/> | <dl> <span data-ttu-id="050ec-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="050ec-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050ec-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="050ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050ec-124">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="050ec-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="050ec-125">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="050ec-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




