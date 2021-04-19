---
description: Die deliverendflush-Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Cdynamicoutputpin. deliverendflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367546"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="8c470-103">Cdynamicoutputpin. deliverendflush-Methode</span><span class="sxs-lookup"><span data-stu-id="8c470-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="8c470-104">Die- `DeliverEndFlush` Methode fordert die verbundene Eingabe-PIN an, um einen Leerungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8c470-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c470-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c470-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="8c470-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c470-106">Parameters</span></span>

<span data-ttu-id="8c470-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c470-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c470-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c470-108">Return value</span></span>

<span data-ttu-id="8c470-109">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="8c470-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c470-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c470-110">Remarks</span></span>

<span data-ttu-id="8c470-111">Diese Methode überschreibt die [**cbaseoutputpin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8c470-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="8c470-112">Das Ereignis [**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8c470-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c470-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c470-113">Requirements</span></span>



| <span data-ttu-id="8c470-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c470-114">Requirement</span></span> | <span data-ttu-id="8c470-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8c470-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c470-116">Header</span><span class="sxs-lookup"><span data-stu-id="8c470-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8c470-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c470-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c470-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c470-118">Library</span></span><br/> | <dl> <span data-ttu-id="8c470-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8c470-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c470-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c470-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c470-121">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8c470-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




