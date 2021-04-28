---
description: 'COutputQueue.BeginFlush-Methode: Die BeginFlush-Methode startet einen Leerungsvorgang.'
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: COutputQueue.BeginFlush-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099028"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="9cdee-103">COutputQueue.BeginFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="9cdee-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="9cdee-104">Die `BeginFlush` -Methode startet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="9cdee-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cdee-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="9cdee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cdee-106">Parameters</span></span>

<span data-ttu-id="9cdee-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9cdee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cdee-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cdee-108">Return value</span></span>

<span data-ttu-id="9cdee-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9cdee-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdee-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cdee-110">Remarks</span></span>

<span data-ttu-id="9cdee-111">Diese Methode legt die [**COutputQueue::m \_ bFlushing-Membervariable**](coutputqueue-m-bflushing.md) auf **TRUE fest.**</span><span class="sxs-lookup"><span data-stu-id="9cdee-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="9cdee-112">Wenn das Objekt einen Thread verwendet, ruft der Thread die [**COutputQueue::FreeSamples-Methode**](coutputqueue-freesamples.md) auf, um ausstehende Stichproben frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="9cdee-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="9cdee-113">Andernfalls ruft das -Objekt **FreeSamples während** der [**COutputQueue::EndFlush-Methode**](coutputqueue-endflush.md) auf.</span><span class="sxs-lookup"><span data-stu-id="9cdee-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="9cdee-114">Diese Methode legt auch die [**COutputQueue::m hr-Membervariable \_**](coutputqueue-m-hr.md) auf S FALSE fest, wodurch das Objekt alle \_ neuen Stichproben verwirft.</span><span class="sxs-lookup"><span data-stu-id="9cdee-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="9cdee-115">Das -Objekt übergibt die Leerungsbenachrichtigung downstream, indem es die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Eingabepin aufruft.</span><span class="sxs-lookup"><span data-stu-id="9cdee-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdee-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cdee-116">Requirements</span></span>



| <span data-ttu-id="9cdee-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cdee-117">Requirement</span></span> | <span data-ttu-id="9cdee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9cdee-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdee-119">Header</span><span class="sxs-lookup"><span data-stu-id="9cdee-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9cdee-120"><dt>Outputq.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdee-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9cdee-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9cdee-121">Library</span></span><br/> | <dl> <span data-ttu-id="9cdee-122"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdee-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cdee-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9cdee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cdee-124">**COutputQueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9cdee-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




