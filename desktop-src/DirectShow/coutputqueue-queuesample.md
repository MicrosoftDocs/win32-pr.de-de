---
description: Die QueueSample-Methode reiht ein Beispiel in die Warteschlange ein.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: COutputQueue.QueueSample-Methode (Outputq.h)
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
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910068"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="ea656-103">COutputQueue.QueueSample-Methode</span><span class="sxs-lookup"><span data-stu-id="ea656-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="ea656-104">Die `QueueSample` -Methode reiht ein Beispiel in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="ea656-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea656-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea656-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ea656-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea656-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ea656-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ea656-108">Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ea656-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea656-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea656-109">Return value</span></span>

<span data-ttu-id="ea656-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ea656-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea656-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea656-111">Remarks</span></span>

<span data-ttu-id="ea656-112">Diese Methode fügt dem Ende der Warteschlange ein Beispiel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea656-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="ea656-113">Halten Sie den kritischen Abschnitt vor dem Aufrufen dieser Methode, und rufen Sie ihn nur auf, wenn das -Objekt einen Thread verwendet, um Beispiele zu liefern.</span><span class="sxs-lookup"><span data-stu-id="ea656-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="ea656-114">Um zu bestimmen, ob das Objekt einen Thread verwendet, rufen Sie die [**COutputQueue::IsQueued-Methode**](coutputqueue-isqueued.md) auf.</span><span class="sxs-lookup"><span data-stu-id="ea656-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="ea656-115">Diese Methode kann auch verwendet werden, um Steuernachrichten in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="ea656-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="ea656-116">Eine Steuermeldung ist eine definierte Konstante (in einen LONG PTR-Typ wandelt), die den Thread anweisen, \_ eine Aktion durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="ea656-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="ea656-117">Die **COutputQueue-Klasse** definiert die in der folgenden Tabelle gezeigten Steuerungsmeldungen.</span><span class="sxs-lookup"><span data-stu-id="ea656-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="ea656-118">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ea656-118">Label</span></span> | <span data-ttu-id="ea656-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ea656-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="ea656-120">`Message`</span><span class="sxs-lookup"><span data-stu-id="ea656-120">Message</span></span>       | <span data-ttu-id="ea656-121">Aktion</span><span class="sxs-lookup"><span data-stu-id="ea656-121">Action</span></span>                                 |
| <span data-ttu-id="ea656-122">PAKET VOM \_ PAKET "EOS"</span><span class="sxs-lookup"><span data-stu-id="ea656-122">EOS\_PACKET</span></span>   | <span data-ttu-id="ea656-123">Stellen Sie eine Benachrichtigung über das Ende des Datenstroms zu.</span><span class="sxs-lookup"><span data-stu-id="ea656-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="ea656-124">NEUES \_ SEGMENT</span><span class="sxs-lookup"><span data-stu-id="ea656-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="ea656-125">Geben Sie ein neues Segment an.</span><span class="sxs-lookup"><span data-stu-id="ea656-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="ea656-126">PAKET \_ ZURÜCKSETZEN</span><span class="sxs-lookup"><span data-stu-id="ea656-126">RESET\_PACKET</span></span> | <span data-ttu-id="ea656-127">Setzen Sie den Status der Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="ea656-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="ea656-128">PAKET \_ SENDEN</span><span class="sxs-lookup"><span data-stu-id="ea656-128">SEND\_PACKET</span></span>  | <span data-ttu-id="ea656-129">Senden Sie einen Teilbatch von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="ea656-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="ea656-130">Dies ist eine geschützte Methode, die von der **COutputQueue-Klasse** intern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea656-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea656-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea656-131">Requirements</span></span>



| <span data-ttu-id="ea656-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea656-132">Requirement</span></span> | <span data-ttu-id="ea656-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ea656-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea656-134">Header</span><span class="sxs-lookup"><span data-stu-id="ea656-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ea656-135"><dt>Outputq.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea656-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea656-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea656-136">Library</span></span><br/> | <dl> <span data-ttu-id="ea656-137"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ea656-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea656-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea656-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea656-139">**COutputQueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea656-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




