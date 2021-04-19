---
description: 'Array von Stichproben der Größe coutputqueue:: m \_ lbatchsize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Coutputqueue:: m_ppSamples-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361983"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="674f0-103">Coutputqueue:: m \_ ppsamples-Member</span><span class="sxs-lookup"><span data-stu-id="674f0-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="674f0-104">Array von Stichproben der Größe [**coutputqueue:: m \_ lbatchsize**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="674f0-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="674f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="674f0-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="674f0-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="674f0-106">Remarks</span></span>

<span data-ttu-id="674f0-107">Der Arbeits Thread ruft Beispiele aus der Warteschlange ab und platziert Sie in diesem Array.</span><span class="sxs-lookup"><span data-stu-id="674f0-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="674f0-108">Er übergibt das Array an die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode.</span><span class="sxs-lookup"><span data-stu-id="674f0-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="674f0-109">Wenn das Objekt keinen Arbeits Thread verwendet, platziert das Objekt Samples direkt in dieses Array.</span><span class="sxs-lookup"><span data-stu-id="674f0-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="674f0-110">Die Member-Variable [**coutputqueue \_ :: m**](coutputqueue-m-list.md) enthält die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="674f0-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="674f0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="674f0-111">Requirements</span></span>



| <span data-ttu-id="674f0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="674f0-112">Requirement</span></span> | <span data-ttu-id="674f0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="674f0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674f0-114">Header</span><span class="sxs-lookup"><span data-stu-id="674f0-114">Header</span></span><br/>  | <dl> <span data-ttu-id="674f0-115"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="674f0-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="674f0-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="674f0-116">Library</span></span><br/> | <dl> <span data-ttu-id="674f0-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="674f0-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674f0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="674f0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674f0-119">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="674f0-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




