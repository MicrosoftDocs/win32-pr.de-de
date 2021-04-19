---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Cdynamicoutputpin. Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362162"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="11286-103">Cdynamicoutputpin. Active-Methode</span><span class="sxs-lookup"><span data-stu-id="11286-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="11286-104">Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="11286-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="11286-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11286-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="11286-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11286-106">Parameters</span></span>

<span data-ttu-id="11286-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="11286-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11286-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11286-108">Return value</span></span>

<span data-ttu-id="11286-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="11286-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="11286-110">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="11286-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="11286-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="11286-111">Return code</span></span>                                                                            | <span data-ttu-id="11286-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11286-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11286-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11286-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="11286-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="11286-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="11286-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="11286-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="11286-116">Fehler.</span><span class="sxs-lookup"><span data-stu-id="11286-116">Failure.</span></span> <span data-ttu-id="11286-117">[**Cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="11286-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11286-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11286-118">Remarks</span></span>

<span data-ttu-id="11286-119">Diese Methode überschreibt die [**cbaseoutputpin:: Active**](cbaseoutputpin-active.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="11286-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="11286-120">Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="11286-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="11286-121">Wenn der besitzende Filter nicht **setconfiginfo** aufgerufen hat, gibt diese Methode E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="11286-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="11286-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11286-122">Requirements</span></span>



| <span data-ttu-id="11286-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11286-123">Requirement</span></span> | <span data-ttu-id="11286-124">Wert</span><span class="sxs-lookup"><span data-stu-id="11286-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11286-125">Header</span><span class="sxs-lookup"><span data-stu-id="11286-125">Header</span></span><br/>  | <dl> <span data-ttu-id="11286-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11286-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="11286-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11286-127">Library</span></span><br/> | <dl> <span data-ttu-id="11286-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="11286-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11286-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11286-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11286-130">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="11286-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




