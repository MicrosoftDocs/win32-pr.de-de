---
description: Die waitdispatchingmessages-Funktion wartet darauf, dass ein Objekt signalisiert wird, während Fenster Meldungen verteilt werden.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Waitdispatchingmessages-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351269"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="ac4f8-103">Waitdispatchingmessages-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac4f8-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="ac4f8-104">Die- `WaitDispatchingMessages` Funktion wartet auf die Signalisierung eines Objekts während der Verteilung von Fenster Meldungen.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac4f8-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="ac4f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac4f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4f8-107">*hobject*</span><span class="sxs-lookup"><span data-stu-id="ac4f8-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4f8-108">Handle des Objekts, auf das gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="ac4f8-109">*dwwait*</span><span class="sxs-lookup"><span data-stu-id="ac4f8-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4f8-110">Timeout Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="ac4f8-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ac4f8-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4f8-112">Optionales Handle für ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="ac4f8-113">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="ac4f8-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4f8-114">Optionale Fenster Meldung, die eine zu Verteil dende Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="ac4f8-115">*hevent*</span><span class="sxs-lookup"><span data-stu-id="ac4f8-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4f8-116">Optionales Handle für ein Ereignis, auf das gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4f8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac4f8-117">Return value</span></span>

<span data-ttu-id="ac4f8-118">Gibt den Wert aus der **WaitForMultipleObjects** -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4f8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac4f8-119">Remarks</span></span>

<span data-ttu-id="ac4f8-120">Wenn ein Objekt ein Fenster besitzt, sollte es beim Warten Fenster Meldungen verteilen.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="ac4f8-121">Diese Funktion ermöglicht es dem-Objekt, während der Verteilung von Nachrichten auf ein Ereignis, ein Semaphor oder ein anderes gegenseitiges Ausschluss Objekt zu warten.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4f8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4f8-122">Requirements</span></span>



| <span data-ttu-id="ac4f8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac4f8-123">Requirement</span></span> | <span data-ttu-id="ac4f8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ac4f8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4f8-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac4f8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ac4f8-126"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac4f8-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ac4f8-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac4f8-127">Library</span></span><br/> | <dl> <span data-ttu-id="ac4f8-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ac4f8-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4f8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac4f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4f8-130">Diverse Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ac4f8-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




