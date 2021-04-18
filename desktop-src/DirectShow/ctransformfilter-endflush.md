---
description: Die endflush-Methode beendet einen Löschvorgang.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Ctransformfilter. endflush-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372402"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="0b6d1-103">Ctransformfilter. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="0b6d1-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="0b6d1-104">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b6d1-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="0b6d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b6d1-106">Parameters</span></span>

<span data-ttu-id="0b6d1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b6d1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b6d1-108">Return value</span></span>

<span data-ttu-id="0b6d1-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6d1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b6d1-110">Remarks</span></span>

<span data-ttu-id="0b6d1-111">Am Ende eines Leerungs Vorgangs ruft die [**ctransforminputpin:: endflush**](ctransforminputpin-endflush.md) -Methode der Eingabe-PIN diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="0b6d1-112">Diese Methode übergibt den- `EndFlush` Rückruf.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="0b6d1-113">Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Beispielen verwendet, muss Sie alle in der Warteschlange befindlichen Daten vor dem Senden des `EndFlush` Aufrufers verwerfen.</span><span class="sxs-lookup"><span data-stu-id="0b6d1-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="0b6d1-114">Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0b6d1-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6d1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b6d1-115">Requirements</span></span>



| <span data-ttu-id="0b6d1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b6d1-116">Requirement</span></span> | <span data-ttu-id="0b6d1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0b6d1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6d1-118">Header</span><span class="sxs-lookup"><span data-stu-id="0b6d1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0b6d1-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b6d1-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b6d1-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b6d1-120">Library</span></span><br/> | <dl> <span data-ttu-id="0b6d1-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0b6d1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b6d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6d1-123">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0b6d1-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




