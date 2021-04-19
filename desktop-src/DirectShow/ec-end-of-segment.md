---
description: Das Ende eines Segments wurde erreicht.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373751"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="b2424-103">EC- \_ Ende \_ des \_ Segments</span><span class="sxs-lookup"><span data-stu-id="b2424-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="b2424-104">Das Ende eines Segments wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="b2424-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2424-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2424-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2424-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b2424-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b2424-107">(**Konstante** **Verweis \_ Zeit** \* ) Zeiger auf einen **Verweis \_ Zeitwert** , der die akkumulierte streamzeit seit dem Start des Segments in 100-Nanosecond-Einheiten angibt.</span><span class="sxs-lookup"><span data-stu-id="b2424-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="b2424-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b2424-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b2424-109">(**DWORD**) Segment Nummer (null basiert).</span><span class="sxs-lookup"><span data-stu-id="b2424-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b2424-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b2424-110">Default Action</span></span>

<span data-ttu-id="b2424-111">Der Filter Graph-Manager überprüft die Anzahl der Ereignisse des **EC- \_ Endes \_ von \_ Segmenten mit** der Anzahl der Ereignisse, die vom [**EC- \_ Segment \_ gestartet**](ec-segment-started.md) wurden.</span><span class="sxs-lookup"><span data-stu-id="b2424-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="b2424-112">Wenn Sie gleich sind, wird das **EC- \_ Ende \_ des \_ Segment** Ereignisses an die Anwendung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b2424-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="b2424-113">Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b2424-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2424-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2424-114">Remarks</span></span>

<span data-ttu-id="b2424-115">Dieser Ereignis Code unterstützt nahtlose Schleifen.</span><span class="sxs-lookup"><span data-stu-id="b2424-115">This event code supports seamless looping.</span></span> <span data-ttu-id="b2424-116">Wenn ein Aufruf der [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode das Element für die \_ Suche nach Segmenten enthält \_ , sendet der Quell Filter diesen Ereignis Code anstelle des Aufrufs von [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="b2424-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2424-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2424-117">Requirements</span></span>



| <span data-ttu-id="b2424-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2424-118">Requirement</span></span> | <span data-ttu-id="b2424-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b2424-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2424-120">Header</span><span class="sxs-lookup"><span data-stu-id="b2424-120">Header</span></span><br/> | <dl> <span data-ttu-id="b2424-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2424-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2424-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2424-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2424-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b2424-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b2424-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2424-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




