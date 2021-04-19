---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Cbasepin. Active-Methode (amfilter. h)
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
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369180"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="21abf-103">Cbasepin. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="21abf-103">CBasePin.Active method</span></span>

<span data-ttu-id="21abf-104">Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="21abf-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="21abf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21abf-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="21abf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21abf-106">Parameters</span></span>

<span data-ttu-id="21abf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="21abf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21abf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21abf-108">Return value</span></span>

<span data-ttu-id="21abf-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="21abf-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="21abf-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21abf-110">Remarks</span></span>

<span data-ttu-id="21abf-111">Wenn der Filter von "angehalten" in "angehalten" wechselt, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode auf allen verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="21abf-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="21abf-112">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="21abf-112">This method does nothing in the base class.</span></span> <span data-ttu-id="21abf-113">Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann eine PIN einen Commit für Zuordnungen durchsetzen oder Hardware Ressourcen abrufen.</span><span class="sxs-lookup"><span data-stu-id="21abf-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="21abf-114">Der interne Zustand des Filter Graph-Managers wird erst aktualisiert, nachdem diese Element Funktion zurückgegeben wurde. Testen Sie daher nicht den Status dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="21abf-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="21abf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21abf-115">Requirements</span></span>



| <span data-ttu-id="21abf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21abf-116">Requirement</span></span> | <span data-ttu-id="21abf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="21abf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21abf-118">Header</span><span class="sxs-lookup"><span data-stu-id="21abf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="21abf-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21abf-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="21abf-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21abf-120">Library</span></span><br/> | <dl> <span data-ttu-id="21abf-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="21abf-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21abf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21abf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21abf-123">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="21abf-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




