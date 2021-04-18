---
description: Die Queue Sample-Methode fügt ein Beispiel in die Warteschlange ein.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Coutputqueue. Queue Sample-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352835"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="2d9c7-103">Coutputqueue. queuesample-Methode</span><span class="sxs-lookup"><span data-stu-id="2d9c7-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="2d9c7-104">Die- `QueueSample` Methode fügt ein Beispiel in die Warteschlange</span><span class="sxs-lookup"><span data-stu-id="2d9c7-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d9c7-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="2d9c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d9c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d9c7-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="2d9c7-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9c7-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d9c7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d9c7-109">Return value</span></span>

<span data-ttu-id="2d9c7-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d9c7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d9c7-111">Remarks</span></span>

<span data-ttu-id="2d9c7-112">Diese Methode fügt dem Ende der Warteschlange ein Beispiel hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="2d9c7-113">Halten Sie den kritischen Abschnitt vor dem Aufruf dieser Methode ein, und rufen Sie ihn nur auf, wenn das Objekt einen Thread zum Übermitteln von Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="2d9c7-114">Um zu ermitteln, ob das Objekt einen Thread verwendet, nennen Sie die [**coutputqueue:: IsQueued**](coutputqueue-isqueued.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="2d9c7-115">Diese Methode kann auch verwendet werden, um Steuerungs Meldungen in der Warteschlange zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="2d9c7-116">Eine Kontroll Meldung ist eine definierte Konstante (in einen langen \_ ptr-Typ umgewandelt), die den Thread anweist, eine Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="2d9c7-117">Die **coutputqueue** -Klasse definiert die in der folgenden Tabelle gezeigten Steuer Meldungen.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="2d9c7-118">`Message`</span><span class="sxs-lookup"><span data-stu-id="2d9c7-118">Message</span></span>       | <span data-ttu-id="2d9c7-119">Aktion</span><span class="sxs-lookup"><span data-stu-id="2d9c7-119">Action</span></span>                                 |
| <span data-ttu-id="2d9c7-120">EOS- \_ Paket</span><span class="sxs-lookup"><span data-stu-id="2d9c7-120">EOS\_PACKET</span></span>   | <span data-ttu-id="2d9c7-121">Übermitteln Sie eine Benachrichtigung zum Ende des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="2d9c7-122">neues \_ Segment</span><span class="sxs-lookup"><span data-stu-id="2d9c7-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="2d9c7-123">Übermitteln Sie ein neues Segment.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="2d9c7-124">Paket zurücksetzen \_</span><span class="sxs-lookup"><span data-stu-id="2d9c7-124">RESET\_PACKET</span></span> | <span data-ttu-id="2d9c7-125">Setzt den Status der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="2d9c7-126">\_Paket senden</span><span class="sxs-lookup"><span data-stu-id="2d9c7-126">SEND\_PACKET</span></span>  | <span data-ttu-id="2d9c7-127">Senden eines partiellen Batches von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="2d9c7-128">Dabei handelt es sich um eine geschützte Methode, die von der **coutputqueue** -Klasse intern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d9c7-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d9c7-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d9c7-129">Requirements</span></span>



| <span data-ttu-id="2d9c7-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d9c7-130">Requirement</span></span> | <span data-ttu-id="2d9c7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2d9c7-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9c7-132">Header</span><span class="sxs-lookup"><span data-stu-id="2d9c7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2d9c7-133"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d9c7-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d9c7-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d9c7-134">Library</span></span><br/> | <dl> <span data-ttu-id="2d9c7-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2d9c7-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d9c7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d9c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9c7-137">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2d9c7-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




