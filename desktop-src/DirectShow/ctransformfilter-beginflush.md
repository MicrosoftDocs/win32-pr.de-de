---
description: 'CTransformFilter.BeginFlush-Methode: Die BeginFlush-Methode startet einen Leerungsvorgang.'
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: CTransformFilter.BeginFlush-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085158"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="14ddc-103">CTransformFilter.BeginFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="14ddc-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="14ddc-104">Die `BeginFlush` -Methode startet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="14ddc-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ddc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ddc-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="14ddc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14ddc-106">Parameters</span></span>

<span data-ttu-id="14ddc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="14ddc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14ddc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14ddc-108">Return value</span></span>

<span data-ttu-id="14ddc-109">Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="14ddc-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ddc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14ddc-110">Remarks</span></span>

<span data-ttu-id="14ddc-111">Zu Beginn eines Leerungsvorgang ruft die [**CTransformInputPin::BeginFlush-Methode**](ctransforminputpin-beginflush.md) des Eingabepins diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="14ddc-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="14ddc-112">Diese Methode übergibt den `BeginFlush` Aufruf downstream.</span><span class="sxs-lookup"><span data-stu-id="14ddc-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="14ddc-113">Wenn die abgeleitete Klasse einen Arbeitsthread verwendet, um Stichproben zu liefern, sollte sie alle Daten in der Warteschlange während eines Leerungsvorgang verwerfen.</span><span class="sxs-lookup"><span data-stu-id="14ddc-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="14ddc-114">Dies kann entweder in der -Methode `BeginFlush` oder in der [**EndFlush-Methode**](ctransformfilter-endflush.md) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="14ddc-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="14ddc-115">Beachten Sie jedoch, dass Aufrufe `BeginFlush` von nicht mit dem Streamingthread synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="14ddc-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="14ddc-116">Wenn die -Methode die in der Warteschlange gespeicherten Daten verwirft, muss der Filter darauf achten, dass keine daten zwischen den Aufrufen und `BeginFlush` `BeginFlush` **EndFlush mehr verarbeiten.**</span><span class="sxs-lookup"><span data-stu-id="14ddc-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="14ddc-117">Weitere Informationen finden Sie unter [Datenfluss für Filterentwickler.](data-flow-for-filter-developers.md)</span><span class="sxs-lookup"><span data-stu-id="14ddc-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14ddc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14ddc-118">Requirements</span></span>



| <span data-ttu-id="14ddc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14ddc-119">Requirement</span></span> | <span data-ttu-id="14ddc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="14ddc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ddc-121">Header</span><span class="sxs-lookup"><span data-stu-id="14ddc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="14ddc-122"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="14ddc-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="14ddc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14ddc-123">Library</span></span><br/> | <dl> <span data-ttu-id="14ddc-124"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="14ddc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ddc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14ddc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ddc-126">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="14ddc-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




