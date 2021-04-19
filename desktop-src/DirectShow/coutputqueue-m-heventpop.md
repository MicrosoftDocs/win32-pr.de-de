---
description: 'Optionales Ereignis, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt. Der Wert ist anfänglich NULL. Aufrufen der coutputqueue:: setpopevent-Methode, um ein Ereignis handle anzugeben.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Coutputqueue:: m_hEventPop-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358370"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="c880c-105">Coutputqueue:: m \_ heventpop-Member</span><span class="sxs-lookup"><span data-stu-id="c880c-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="c880c-106">Optionales Ereignis, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="c880c-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="c880c-107">Der Wert ist anfänglich **null**.</span><span class="sxs-lookup"><span data-stu-id="c880c-107">The value is initially **NULL**.</span></span> <span data-ttu-id="c880c-108">Aufrufen der [**coutputqueue:: setpopevent**](coutputqueue-setpopevent.md) -Methode, um ein Ereignis handle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c880c-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c880c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c880c-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="c880c-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c880c-110">Requirements</span></span>



| <span data-ttu-id="c880c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c880c-111">Requirement</span></span> | <span data-ttu-id="c880c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c880c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c880c-113">Header</span><span class="sxs-lookup"><span data-stu-id="c880c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c880c-114"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c880c-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c880c-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c880c-115">Library</span></span><br/> | <dl> <span data-ttu-id="c880c-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c880c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c880c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c880c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c880c-118">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c880c-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




