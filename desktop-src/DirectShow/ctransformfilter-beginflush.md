---
description: Die beginflush-Methode startet einen Löschvorgang.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Ctransformfilter. beginflush-Methode (Transfrm. h)
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
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373662"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="024be-103">Ctransformfilter. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="024be-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="024be-104">Die- `BeginFlush` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="024be-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="024be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="024be-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="024be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="024be-106">Parameters</span></span>

<span data-ttu-id="024be-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="024be-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="024be-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="024be-108">Return value</span></span>

<span data-ttu-id="024be-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="024be-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="024be-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="024be-110">Remarks</span></span>

<span data-ttu-id="024be-111">Zu Beginn eines Leerungs Vorgangs ruft die [**ctransforminputpin:: beginflush**](ctransforminputpin-beginflush.md) -Methode der Eingabe-PIN diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="024be-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="024be-112">Diese Methode übergibt den- `BeginFlush` Rückruf.</span><span class="sxs-lookup"><span data-stu-id="024be-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="024be-113">Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Beispielen verwendet, sollte Sie alle in der Warteschlange befindlichen Daten während eines Löschvorgangs verwerfen.</span><span class="sxs-lookup"><span data-stu-id="024be-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="024be-114">Dies kann entweder in der- `BeginFlush` Methode oder in der [**endflush**](ctransformfilter-endflush.md) -Methode erfolgen.</span><span class="sxs-lookup"><span data-stu-id="024be-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="024be-115">Beachten Sie jedoch, dass Aufrufe von `BeginFlush` nicht mit dem streamingthread synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="024be-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="024be-116">Wenn die `BeginFlush` -Methode die in der Warteschlange befindlichen Daten verwirft, muss der Filter darauf achten, dass keine weiteren Daten zwischen den `BeginFlush` -und **endflush** -aufrufen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="024be-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="024be-117">Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="024be-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="024be-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="024be-118">Requirements</span></span>



| <span data-ttu-id="024be-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="024be-119">Requirement</span></span> | <span data-ttu-id="024be-120">Wert</span><span class="sxs-lookup"><span data-stu-id="024be-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024be-121">Header</span><span class="sxs-lookup"><span data-stu-id="024be-121">Header</span></span><br/>  | <dl> <span data-ttu-id="024be-122"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="024be-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="024be-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="024be-123">Library</span></span><br/> | <dl> <span data-ttu-id="024be-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="024be-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024be-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="024be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024be-126">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="024be-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




