---
description: 'CDynamicOutputPin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: CDynamicOutputPin.Active-Methode (Amfilter.h)
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
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099328"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="f398d-103">CDynamicOutputPin.Active-Methode</span><span class="sxs-lookup"><span data-stu-id="f398d-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="f398d-104">Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f398d-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="f398d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f398d-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="f398d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f398d-106">Parameters</span></span>

<span data-ttu-id="f398d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f398d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f398d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f398d-108">Return value</span></span>

<span data-ttu-id="f398d-109">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="f398d-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f398d-110">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="f398d-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f398d-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f398d-111">Return code</span></span>                                                                            | <span data-ttu-id="f398d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f398d-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f398d-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f398d-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f398d-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f398d-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f398d-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f398d-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f398d-116">Fehler.</span><span class="sxs-lookup"><span data-stu-id="f398d-116">Failure.</span></span> <span data-ttu-id="f398d-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f398d-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f398d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f398d-118">Remarks</span></span>

<span data-ttu-id="f398d-119">Diese Methode überschreibt die [**CBaseOutputPin::Active-Methode.**](cbaseoutputpin-active.md)</span><span class="sxs-lookup"><span data-stu-id="f398d-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="f398d-120">Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f398d-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="f398d-121">Wenn der besitzende Filter **SetConfigInfo** nicht aufgerufen hat, gibt diese Methode E \_ FAIL zurück.</span><span class="sxs-lookup"><span data-stu-id="f398d-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f398d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f398d-122">Requirements</span></span>



| <span data-ttu-id="f398d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f398d-123">Requirement</span></span> | <span data-ttu-id="f398d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f398d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f398d-125">Header</span><span class="sxs-lookup"><span data-stu-id="f398d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f398d-126"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="f398d-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f398d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f398d-127">Library</span></span><br/> | <dl> <span data-ttu-id="f398d-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f398d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f398d-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f398d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f398d-130">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f398d-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




