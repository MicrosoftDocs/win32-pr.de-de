---
description: Die beginflush-Methode startet einen Löschvorgang.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Coutputqueue. beginflush-Methode (outputq. h)
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
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361584"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="03724-103">Coutputqueue. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="03724-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="03724-104">Die- `BeginFlush` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="03724-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="03724-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03724-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="03724-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03724-106">Parameters</span></span>

<span data-ttu-id="03724-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="03724-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03724-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03724-108">Return value</span></span>

<span data-ttu-id="03724-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="03724-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03724-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03724-110">Remarks</span></span>

<span data-ttu-id="03724-111">Diese Methode legt die Element Variable [**coutputqueue:: m \_ bleerung**](coutputqueue-m-bflushing.md) auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="03724-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="03724-112">Wenn das Objekt einen Thread verwendet, ruft der Thread die [**coutputqueue:: freesamples**](coutputqueue-freesamples.md) -Methode auf, um alle ausstehenden Beispiele freizugeben.</span><span class="sxs-lookup"><span data-stu-id="03724-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="03724-113">Andernfalls ruft das-Objekt während der [**coutputqueue:: endflush**](coutputqueue-endflush.md) -Methode **freesamples** auf.</span><span class="sxs-lookup"><span data-stu-id="03724-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="03724-114">Diese Methode legt auch die [**coutputqueue:: m- \_ HR**](coutputqueue-m-hr.md) -Member-Variable auf "false" fest \_ , was bewirkt, dass das-Objekt alle neuen-Beispiele verwerfen kann.</span><span class="sxs-lookup"><span data-stu-id="03724-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="03724-115">Das Objekt übergibt die Leerungs Benachrichtigung durch Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für die Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="03724-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="03724-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03724-116">Requirements</span></span>



| <span data-ttu-id="03724-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03724-117">Requirement</span></span> | <span data-ttu-id="03724-118">Wert</span><span class="sxs-lookup"><span data-stu-id="03724-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03724-119">Header</span><span class="sxs-lookup"><span data-stu-id="03724-119">Header</span></span><br/>  | <dl> <span data-ttu-id="03724-120"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03724-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03724-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03724-121">Library</span></span><br/> | <dl> <span data-ttu-id="03724-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="03724-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03724-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03724-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03724-124">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03724-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




