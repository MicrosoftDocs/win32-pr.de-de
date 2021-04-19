---
description: Fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Cmsgthread. putthreadmsg-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372199"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="f48dd-103">Cmsgthread. putthreadmsg-Methode</span><span class="sxs-lookup"><span data-stu-id="f48dd-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="f48dd-104">Fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="f48dd-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f48dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f48dd-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="f48dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f48dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f48dd-107">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="f48dd-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f48dd-108">Anforderungs Code.</span><span class="sxs-lookup"><span data-stu-id="f48dd-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="f48dd-109">*dwmsgflags*</span><span class="sxs-lookup"><span data-stu-id="f48dd-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f48dd-110">Optionaler Flags-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f48dd-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f48dd-111">*lpmsgparam*</span><span class="sxs-lookup"><span data-stu-id="f48dd-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f48dd-112">Optionaler Zeiger auf einen Datenblock mit zusätzlichen Parametern oder Rückgabe Werten.</span><span class="sxs-lookup"><span data-stu-id="f48dd-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="f48dd-113">Muss statisch oder Heap zugeordnet sein, nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="f48dd-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="f48dd-114">*Peer Event*</span><span class="sxs-lookup"><span data-stu-id="f48dd-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="f48dd-115">Optionaler Zeiger auf ein Ereignis Objekt, das nach Abschluss signalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f48dd-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f48dd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f48dd-116">Return value</span></span>

<span data-ttu-id="f48dd-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f48dd-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f48dd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f48dd-118">Remarks</span></span>

<span data-ttu-id="f48dd-119">Diese Member-Funktion fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="f48dd-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="f48dd-120">Die Parameter dieser Member-Funktion werden in die Warteschlange eingereiht (in einem [**CMSG**](cmsg.md) -Objekt) und an die [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion des Arbeits Thread übergeben.</span><span class="sxs-lookup"><span data-stu-id="f48dd-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="f48dd-121">Diese Member-Funktion gibt sofort zurück, nachdem die Anforderung in die Warteschlange eingereiht wurde, und wartet nicht, bis der Thread die Anforderung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="f48dd-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="f48dd-122">Die **cmsgthread:: threadmessageproc** -Member-Funktion der abgeleiteten Klasse definiert die vier Parameter.</span><span class="sxs-lookup"><span data-stu-id="f48dd-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="f48dd-123">Diese Member-Funktion verwendet eine Multithreadsichere Liste, sodass mehrere Aufrufe dieser Element Funktion aus unterschiedlichen Threads sicher durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="f48dd-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="f48dd-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f48dd-124">Requirements</span></span>



| <span data-ttu-id="f48dd-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f48dd-125">Requirement</span></span> | <span data-ttu-id="f48dd-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f48dd-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48dd-127">Header</span><span class="sxs-lookup"><span data-stu-id="f48dd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f48dd-128"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f48dd-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f48dd-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f48dd-129">Library</span></span><br/> | <dl> <span data-ttu-id="f48dd-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f48dd-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48dd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f48dd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48dd-132">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f48dd-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




