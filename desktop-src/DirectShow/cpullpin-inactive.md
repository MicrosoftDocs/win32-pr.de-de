---
description: Die inaktive Methode beendet den Arbeits Thread, der Daten aus der Ausgabe-PIN abruft. Mit dieser Methode wird auch der Zuweiser decommittet.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Cpullpin. inaktive Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367739"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="54bc5-104">Cpullpin. inaktive Methode</span><span class="sxs-lookup"><span data-stu-id="54bc5-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="54bc5-105">Die- `Inactive` Methode beendet den Arbeits Thread, der Daten aus der Ausgabe-PIN abruft.</span><span class="sxs-lookup"><span data-stu-id="54bc5-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="54bc5-106">Mit dieser Methode wird auch der Zuweiser decommittet.</span><span class="sxs-lookup"><span data-stu-id="54bc5-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="54bc5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54bc5-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="54bc5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54bc5-108">Parameters</span></span>

<span data-ttu-id="54bc5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="54bc5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54bc5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54bc5-110">Return value</span></span>

<span data-ttu-id="54bc5-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="54bc5-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="54bc5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54bc5-112">Remarks</span></span>

<span data-ttu-id="54bc5-113">Ruft diese Methode auf, wenn der besitzende Filter inaktiv wird.</span><span class="sxs-lookup"><span data-stu-id="54bc5-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="54bc5-114">(Wenn Ihre Eingabe-PIN von [**cbasepin**](cbasepin.md)abgeleitet ist, überschreiben Sie die [**cbasepin:: inaktive**](cbasepin-inactive.md) -Methode.)</span><span class="sxs-lookup"><span data-stu-id="54bc5-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="54bc5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54bc5-115">Requirements</span></span>



| <span data-ttu-id="54bc5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54bc5-116">Requirement</span></span> | <span data-ttu-id="54bc5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="54bc5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54bc5-118">Header</span><span class="sxs-lookup"><span data-stu-id="54bc5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="54bc5-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="54bc5-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="54bc5-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54bc5-120">Library</span></span><br/> | <dl> <span data-ttu-id="54bc5-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="54bc5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54bc5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54bc5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bc5-123">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="54bc5-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




