---
description: Die inaktive Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Cbasepin. ininaktive Methode (amfilter. h)
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
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370180"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="4426a-103">Cbasepin. inaktive-Methode</span><span class="sxs-lookup"><span data-stu-id="4426a-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="4426a-104">Die- `Inactive` Methode benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4426a-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4426a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4426a-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4426a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4426a-106">Parameters</span></span>

<span data-ttu-id="4426a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4426a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4426a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4426a-108">Return value</span></span>

<span data-ttu-id="4426a-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4426a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4426a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4426a-110">Remarks</span></span>

<span data-ttu-id="4426a-111">Wenn der Filter angehalten wird, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode auf allen verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="4426a-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="4426a-112">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="4426a-112">This method does nothing in the base class.</span></span> <span data-ttu-id="4426a-113">Abgeleitete Klassen sollten diese Methode überschreiben, um alle Ressourcen freizugeben, die von der [**cbasepin:: Active**](cbasepin-active.md) -Methode abgerufen werden. beispielsweise, um die Zuweisungen der PIN zu decoden.</span><span class="sxs-lookup"><span data-stu-id="4426a-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="4426a-114">Der interne Zustand des Filter Graph-Managers wird erst aktualisiert, nachdem diese Methode zurückgegeben wurde. Testen Sie daher nicht den Status dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="4426a-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4426a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4426a-115">Requirements</span></span>



| <span data-ttu-id="4426a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4426a-116">Requirement</span></span> | <span data-ttu-id="4426a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4426a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4426a-118">Header</span><span class="sxs-lookup"><span data-stu-id="4426a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4426a-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4426a-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4426a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4426a-120">Library</span></span><br/> | <dl> <span data-ttu-id="4426a-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4426a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4426a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4426a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4426a-123">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4426a-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




