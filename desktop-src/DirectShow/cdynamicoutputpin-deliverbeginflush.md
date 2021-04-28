---
description: 'CDynamicOutputPin.DeliverBeginFlush-Methode: Die DeliverBeginFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: CDynamicOutputPin.DeliverBeginFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099318"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="2f2fc-103">CDynamicOutputPin.DeliverBeginFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="2f2fc-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="2f2fc-104">Die `DeliverBeginFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="2f2fc-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2fc-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="2f2fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f2fc-106">Parameters</span></span>

<span data-ttu-id="2f2fc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2f2fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f2fc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f2fc-108">Return value</span></span>

<span data-ttu-id="2f2fc-109">Gibt S \_ OK zurück, wenn erfolgreich, oder einen **HRESULT-Wert,** der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="2f2fc-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2fc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f2fc-110">Remarks</span></span>

<span data-ttu-id="2f2fc-111">Diese Methode überschreibt die [**CBaseOutputPin::D eliverBeginFlush-Methode.**](cbaseoutputpin-deliverbeginflush.md)</span><span class="sxs-lookup"><span data-stu-id="2f2fc-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="2f2fc-112">Es legt das [**CDynamicOutputPin::m \_ hStopEvent-Ereignis**](cdynamicoutputpin-m-hstopevent.md) fest.</span><span class="sxs-lookup"><span data-stu-id="2f2fc-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2fc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f2fc-113">Requirements</span></span>



| <span data-ttu-id="2f2fc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f2fc-114">Requirement</span></span> | <span data-ttu-id="2f2fc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2f2fc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2fc-116">Header</span><span class="sxs-lookup"><span data-stu-id="2f2fc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2f2fc-117"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="2f2fc-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f2fc-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f2fc-118">Library</span></span><br/> | <dl> <span data-ttu-id="2f2fc-119"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2f2fc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2fc-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f2fc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2fc-121">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2f2fc-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




