---
description: 'CBasePin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: CBasePin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099338"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="f739f-103">CBasePin.Inactive-Methode</span><span class="sxs-lookup"><span data-stu-id="f739f-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="f739f-104">Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f739f-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="f739f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f739f-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="f739f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f739f-106">Parameters</span></span>

<span data-ttu-id="f739f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f739f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f739f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f739f-108">Return value</span></span>

<span data-ttu-id="f739f-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f739f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f739f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f739f-110">Remarks</span></span>

<span data-ttu-id="f739f-111">Wenn der Filter beendet wird, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode für alle verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="f739f-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="f739f-112">Diese Methode führt in der Basisklasse nichts aus.</span><span class="sxs-lookup"><span data-stu-id="f739f-112">This method does nothing in the base class.</span></span> <span data-ttu-id="f739f-113">Abgeleitete Klassen sollten diese Methode überschreiben, um alle Ressourcen frei zu lassen, die von der [**CBasePin::Active-Methode erhalten**](cbasepin-active.md) wurden. Zum Beispiel zum Decommit der Zuweisungen des Pins.</span><span class="sxs-lookup"><span data-stu-id="f739f-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="f739f-114">Der interne Zustand des Filterdiagramm-Managers wird erst aktualisiert, nachdem diese Methode zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="f739f-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f739f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f739f-115">Requirements</span></span>



| <span data-ttu-id="f739f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f739f-116">Requirement</span></span> | <span data-ttu-id="f739f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f739f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f739f-118">Header</span><span class="sxs-lookup"><span data-stu-id="f739f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f739f-119"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="f739f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f739f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f739f-120">Library</span></span><br/> | <dl> <span data-ttu-id="f739f-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f739f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f739f-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f739f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f739f-123">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f739f-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




