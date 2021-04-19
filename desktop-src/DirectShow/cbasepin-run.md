---
description: Die Run-Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Cbasepin. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369711"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="5f483-103">Cbasepin. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="5f483-103">CBasePin.Run method</span></span>

<span data-ttu-id="5f483-104">Die- `Run` Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f483-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f483-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f483-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="5f483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f483-107">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="5f483-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5f483-108">Die Startzeit, die an die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode des Filters übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5f483-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f483-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f483-109">Return value</span></span>

<span data-ttu-id="5f483-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5f483-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f483-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f483-111">Remarks</span></span>

<span data-ttu-id="5f483-112">Wenn der Filter von "angehalten" in "wird ausgeführt" wechselt, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode für alle Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="5f483-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="5f483-113">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5f483-113">This method does nothing in the base class.</span></span> <span data-ttu-id="5f483-114">Abgeleitete Klassen können diese Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5f483-114">Derived classes can override this method.</span></span> <span data-ttu-id="5f483-115">Beispielsweise kann eine PIN einen Arbeits Thread starten, der Beispiele liefert.</span><span class="sxs-lookup"><span data-stu-id="5f483-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="5f483-116">Der interne Zustand des Filter Graph-Managers wird erst aktualisiert, nachdem diese Element Funktion zurückgegeben wurde. Testen Sie daher nicht den Status dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="5f483-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f483-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f483-117">Requirements</span></span>



| <span data-ttu-id="5f483-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f483-118">Requirement</span></span> | <span data-ttu-id="5f483-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5f483-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f483-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f483-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5f483-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f483-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f483-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f483-122">Library</span></span><br/> | <dl> <span data-ttu-id="5f483-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5f483-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f483-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f483-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f483-125">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5f483-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




