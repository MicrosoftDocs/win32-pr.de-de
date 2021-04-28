---
description: 'CDynamicOutputPin.DeliverEndFlush-Methode: Die DeliverEndFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: CDynamicOutputPin.DeliverEndFlush-Methode (Amfilter.h)
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
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095708"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="f8ef8-103">CDynamicOutputPin.DeliverEndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="f8ef8-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="f8ef8-104">Die `DeliverEndFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ef8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ef8-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="f8ef8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ef8-106">Parameters</span></span>

<span data-ttu-id="f8ef8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8ef8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8ef8-108">Return value</span></span>

<span data-ttu-id="f8ef8-109">Gibt S \_ OK zurück, wenn erfolgreich, oder einen **HRESULT-Wert,** der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ef8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8ef8-110">Remarks</span></span>

<span data-ttu-id="f8ef8-111">Diese Methode überschreibt die [**CBaseOutputPin::D eliverEndFlush-Methode.**](cbaseoutputpin-deliverendflush.md)</span><span class="sxs-lookup"><span data-stu-id="f8ef8-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="f8ef8-112">Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ef8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ef8-113">Requirements</span></span>



| <span data-ttu-id="f8ef8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8ef8-114">Requirement</span></span> | <span data-ttu-id="f8ef8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f8ef8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ef8-116">Header</span><span class="sxs-lookup"><span data-stu-id="f8ef8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ef8-117"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ef8-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8ef8-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8ef8-118">Library</span></span><br/> | <dl> <span data-ttu-id="f8ef8-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ef8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ef8-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8ef8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ef8-121">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8ef8-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




