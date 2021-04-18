---
description: Die endflush-Methode informiert den besitzenden Filter, einen Leerungs Vorgang zu beenden. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Cpullpin. endflush-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371257"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="b3ad9-104">Cpullpin. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="b3ad9-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="b3ad9-105">Die- `EndFlush` Methode informiert den besitzenden Filter, um einen Leerungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="b3ad9-106">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ad9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ad9-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="b3ad9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3ad9-108">Parameters</span></span>

<span data-ttu-id="b3ad9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3ad9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3ad9-110">Return value</span></span>

<span data-ttu-id="b3ad9-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ad9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3ad9-112">Remarks</span></span>

<span data-ttu-id="b3ad9-113">Die [**cpullpin:: Seek**](cpullpin-seek.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="b3ad9-114">Implementieren Sie diese Methode, um die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="b3ad9-115">Wenn die Ausgabe-PIN (s) Ihres Filters von **cbaseoutputpin** abgeleitet ist, rufen Sie die **cbaseoutputpin::D eliverendflush** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="b3ad9-116">Dieser Entwurf ermöglicht dem Filter, einfach durch Aufrufen von **Seek** im **cpullpin** -Objekt auf den Stream zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ad9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3ad9-117">Requirements</span></span>



| <span data-ttu-id="b3ad9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3ad9-118">Requirement</span></span> | <span data-ttu-id="b3ad9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b3ad9-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ad9-120">Header</span><span class="sxs-lookup"><span data-stu-id="b3ad9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b3ad9-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ad9-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b3ad9-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3ad9-122">Library</span></span><br/> | <dl> <span data-ttu-id="b3ad9-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b3ad9-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ad9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3ad9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ad9-125">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b3ad9-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




