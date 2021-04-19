---
description: Die waitmsg-Methode wartet darauf, dass das Ereignis signalisiert wird, während gesendete Nachrichten versendet werden.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Cammsgevent. waitmsg-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360383"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="a8914-103">Cammsgevent. waitmsg-Methode</span><span class="sxs-lookup"><span data-stu-id="a8914-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="a8914-104">Die- `WaitMsg` Methode wartet, bis das-Ereignis signalisiert wird, während gesendete Nachrichten versendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8914-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8914-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8914-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="a8914-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8914-107">*dwtimeout*</span><span class="sxs-lookup"><span data-stu-id="a8914-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a8914-108">Optionaler Timeout Wert in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="a8914-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8914-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8914-109">Return value</span></span>

<span data-ttu-id="a8914-110">Gibt " **true** " zurück, wenn das Ereignis signalisiert wird, oder " **false** ", wenn das Timeout aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8914-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8914-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8914-111">Remarks</span></span>

<span data-ttu-id="a8914-112">Diese Methode ruft die Funktion "Peer Message" auf, um Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8914-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="a8914-113">Diese Methode wird anstelle von " [**camevent:: Wait**](camevent-wait.md) " aufgerufen, wenn der Thread beim Warten auf ein Ereignis Nachrichten verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="a8914-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="a8914-114">Wenn der Thread keine Nachrichten verarbeitet und ein anderer Thread eine Nachricht sendet, kann ein Deadlock auftreten.</span><span class="sxs-lookup"><span data-stu-id="a8914-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="a8914-115">Nehmen Sie beispielsweise an, Sie erstellen einen Thread und blockieren dann, bis der Thread initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8914-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="a8914-116">Wenn der Thread durch Aufrufen der SendMessage-Funktion eine Nachricht an das Fenster sendet, führt dies zu einem Deadlock.</span><span class="sxs-lookup"><span data-stu-id="a8914-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="a8914-117">Dies liegt daran, dass SendMessage erst zurückgegeben wird, wenn die Nachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8914-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="a8914-118">Durch den Aufruf von waitmsg kann der SendMessage-Aufruf zurückgegeben werden, wodurch der Deadlock verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="a8914-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8914-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8914-119">Requirements</span></span>



| <span data-ttu-id="a8914-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8914-120">Requirement</span></span> | <span data-ttu-id="a8914-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a8914-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8914-122">Header</span><span class="sxs-lookup"><span data-stu-id="a8914-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a8914-123"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8914-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8914-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8914-124">Library</span></span><br/> | <dl> <span data-ttu-id="a8914-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a8914-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8914-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8914-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8914-127">**Cammsgevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8914-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




