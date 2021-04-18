---
description: Die setpopevent-Methode gibt ein Ereignis an, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Coutputqueue. setpopevent-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365913"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="34e43-103">Coutputqueue. setpopevent-Methode</span><span class="sxs-lookup"><span data-stu-id="34e43-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="34e43-104">Die- `SetPopEvent` Methode gibt ein Ereignis an, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="34e43-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34e43-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="34e43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34e43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e43-107">*hevent*</span><span class="sxs-lookup"><span data-stu-id="34e43-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="34e43-108">Handle für ein Ereignis, das vom Aufrufer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="34e43-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e43-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34e43-109">Return value</span></span>

<span data-ttu-id="34e43-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="34e43-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e43-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34e43-111">Requirements</span></span>



| <span data-ttu-id="34e43-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34e43-112">Requirement</span></span> | <span data-ttu-id="34e43-113">Wert</span><span class="sxs-lookup"><span data-stu-id="34e43-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e43-114">Header</span><span class="sxs-lookup"><span data-stu-id="34e43-114">Header</span></span><br/>  | <dl> <span data-ttu-id="34e43-115"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34e43-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34e43-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34e43-116">Library</span></span><br/> | <dl> <span data-ttu-id="34e43-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="34e43-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e43-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e43-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e43-119">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="34e43-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




