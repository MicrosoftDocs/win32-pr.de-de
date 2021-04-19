---
description: Die freesamples-Methode gibt alle ausstehenden Beispiele frei.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Coutputqueue. freesamples-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369149"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="4b788-103">Coutputqueue. freesamples-Methode</span><span class="sxs-lookup"><span data-stu-id="4b788-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="4b788-104">Die- `FreeSamples` Methode gibt alle ausstehenden Beispiele frei.</span><span class="sxs-lookup"><span data-stu-id="4b788-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b788-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b788-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="4b788-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b788-106">Parameters</span></span>

<span data-ttu-id="4b788-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4b788-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b788-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b788-108">Return value</span></span>

<span data-ttu-id="4b788-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b788-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b788-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b788-110">Remarks</span></span>

<span data-ttu-id="4b788-111">Mit dieser Methode werden alle ausstehenden Beispiele aus der Warteschlange und aus dem Beispiel Array entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b788-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b788-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b788-112">Requirements</span></span>



| <span data-ttu-id="4b788-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b788-113">Requirement</span></span> | <span data-ttu-id="4b788-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4b788-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b788-115">Header</span><span class="sxs-lookup"><span data-stu-id="4b788-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4b788-116"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b788-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b788-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b788-117">Library</span></span><br/> | <dl> <span data-ttu-id="4b788-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4b788-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b788-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b788-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b788-120">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4b788-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




