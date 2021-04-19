---
description: Konstruktormethode.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Camevent. camevent-Konstruktor (wxutil. h)
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
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369934"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="f74da-103">Camevent. camevent-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="f74da-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="f74da-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f74da-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f74da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f74da-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f74da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f74da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f74da-107">*nicht verfügbar*</span><span class="sxs-lookup"><span data-stu-id="f74da-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="f74da-108">Boolescher Wert, der angibt, ob das Objekt ein manuelles Zurücksetzungs Ereignis oder ein Auto-Reset-Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="f74da-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="f74da-109">**True** gibt an, dass das Objekt ein manuelles Zurücksetzungs Ereignis ist.</span><span class="sxs-lookup"><span data-stu-id="f74da-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="f74da-110">Andernfalls handelt es sich um ein Auto Reset-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f74da-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="f74da-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="f74da-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f74da-112">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="f74da-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f74da-113">Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f74da-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="f74da-114">Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="f74da-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="f74da-115">Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**.</span><span class="sxs-lookup"><span data-stu-id="f74da-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="f74da-116">Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="f74da-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f74da-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f74da-117">Remarks</span></span>

<span data-ttu-id="f74da-118">Das Ereignis beginnt in einem nicht signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="f74da-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="f74da-119">Bei einem Auto-Reset-Ereignis setzt die Methode " [**camevent:: Wait**](camevent-wait.md) " das Ereignis auf "nicht signalisiert" zurück, wenn die Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f74da-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="f74da-120">Bei einem manuellen Reset-Ereignis bleibt das Ereignis signalisiert, bis Sie die Methode " [**camevent:: Reset**](camevent-reset.md) " aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="f74da-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f74da-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f74da-121">Requirements</span></span>



| <span data-ttu-id="f74da-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f74da-122">Requirement</span></span> | <span data-ttu-id="f74da-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f74da-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74da-124">Header</span><span class="sxs-lookup"><span data-stu-id="f74da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f74da-125"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f74da-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f74da-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f74da-126">Library</span></span><br/> | <dl> <span data-ttu-id="f74da-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f74da-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74da-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f74da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f74da-129">**Camevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f74da-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




