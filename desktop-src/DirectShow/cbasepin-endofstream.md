---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode. Diese Methode nur für Eingabe Pins aufzurufen.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Cbasepin. EndOf Stream-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364459"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="bbef9-105">Cbasepin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="bbef9-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="bbef9-106">Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="bbef9-107">Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bbef9-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="bbef9-108">Diese Methode nur für Eingabe Pins aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbef9-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbef9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbef9-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="bbef9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbef9-110">Parameters</span></span>

<span data-ttu-id="bbef9-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bbef9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbef9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbef9-112">Return value</span></span>

<span data-ttu-id="bbef9-113">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="bbef9-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbef9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbef9-114">Remarks</span></span>

<span data-ttu-id="bbef9-115">Der Filter sollte Streamende Benachrichtigungen an die Eingabe Pins verbundener Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="bbef9-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="bbef9-116">Wenn der Filter ein Renderer ist, sollte er eine [**EC \_ Complete**](ec-complete.md) Event-Benachrichtigung an den Filter Graph-Manager senden.</span><span class="sxs-lookup"><span data-stu-id="bbef9-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="bbef9-117">Weitere Informationen finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="bbef9-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="bbef9-118">In der Basisklasse führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="bbef9-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="bbef9-119">Abgeleitete Klassen sollten diese Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bbef9-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbef9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbef9-120">Requirements</span></span>



| <span data-ttu-id="bbef9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbef9-121">Requirement</span></span> | <span data-ttu-id="bbef9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bbef9-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbef9-123">Header</span><span class="sxs-lookup"><span data-stu-id="bbef9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bbef9-124"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbef9-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bbef9-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bbef9-125">Library</span></span><br/> | <dl> <span data-ttu-id="bbef9-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bbef9-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbef9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbef9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbef9-128">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bbef9-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




