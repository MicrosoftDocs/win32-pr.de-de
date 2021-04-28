---
description: 'CABEvent.CABEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: CABEvent.CABEvent-Konstruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096531"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="6a02b-103">CABEvent.CABEvent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6a02b-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="6a02b-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="6a02b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a02b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a02b-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6a02b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a02b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a02b-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="6a02b-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="6a02b-108">Ein boolescher Wert, der angibt, ob es sich bei dem Objekt um ein Ereignis mit manueller oder automatischer Zurücksetzung handelt.</span><span class="sxs-lookup"><span data-stu-id="6a02b-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="6a02b-109">True gibt an, dass das Objekt ein Ereignis für die manuelle Zurücksetzung ist.</span><span class="sxs-lookup"><span data-stu-id="6a02b-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="6a02b-110">Andernfalls handelt es sich um ein Ereignis für die automatische Zurücksetzung.</span><span class="sxs-lookup"><span data-stu-id="6a02b-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="6a02b-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="6a02b-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6a02b-112">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="6a02b-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6a02b-113">Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6a02b-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="6a02b-114">In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="6a02b-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="6a02b-115">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6a02b-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="6a02b-116">Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="6a02b-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a02b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a02b-117">Remarks</span></span>

<span data-ttu-id="6a02b-118">Das Ereignis beginnt in einem nicht signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="6a02b-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="6a02b-119">Bei einem Ereignis für die automatische Zurücksetzung setzt die [**RESETEvent::Wait-Methode**](camevent-wait.md) das Ereignis auf nicht signalisiert zurück, wenn die Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a02b-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="6a02b-120">Bei einem Ereignis für die manuelle Zurücksetzung bleibt das Ereignis signalisiert, bis Sie die [**METHODE RESETEvent::Reset**](camevent-reset.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6a02b-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a02b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a02b-121">Requirements</span></span>



| <span data-ttu-id="6a02b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a02b-122">Requirement</span></span> | <span data-ttu-id="6a02b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6a02b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a02b-124">Header</span><span class="sxs-lookup"><span data-stu-id="6a02b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6a02b-125"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a02b-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6a02b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a02b-126">Library</span></span><br/> | <dl> <span data-ttu-id="6a02b-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6a02b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a02b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6a02b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a02b-129">**WEBCAMEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6a02b-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




