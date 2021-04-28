---
description: 'CBasePin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: CBasePin.Active-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096107"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="f9db9-103">CBasePin.Active-Methode</span><span class="sxs-lookup"><span data-stu-id="f9db9-103">CBasePin.Active method</span></span>

<span data-ttu-id="f9db9-104">Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f9db9-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9db9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9db9-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="f9db9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9db9-106">Parameters</span></span>

<span data-ttu-id="f9db9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9db9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9db9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9db9-108">Return value</span></span>

<span data-ttu-id="f9db9-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f9db9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9db9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9db9-110">Remarks</span></span>

<span data-ttu-id="f9db9-111">Wenn der Filter von angehalten in angehalten wechselt, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode für alle verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="f9db9-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="f9db9-112">Diese Methode führt in der Basisklasse nichts aus.</span><span class="sxs-lookup"><span data-stu-id="f9db9-112">This method does nothing in the base class.</span></span> <span data-ttu-id="f9db9-113">Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann ein Pin Zuweisungen committen oder Hardwareressourcen abrufen.</span><span class="sxs-lookup"><span data-stu-id="f9db9-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="f9db9-114">Der interne Zustand des Filtergraph-Managers wird erst aktualisiert, nachdem diese Memberfunktion zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="f9db9-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9db9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9db9-115">Requirements</span></span>



| <span data-ttu-id="f9db9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9db9-116">Requirement</span></span> | <span data-ttu-id="f9db9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f9db9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9db9-118">Header</span><span class="sxs-lookup"><span data-stu-id="f9db9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f9db9-119"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f9db9-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f9db9-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9db9-120">Library</span></span><br/> | <dl> <span data-ttu-id="f9db9-121"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f9db9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9db9-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9db9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9db9-123">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f9db9-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




