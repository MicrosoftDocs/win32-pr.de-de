---
description: Die EndOfStream-Methode wird aufgerufen, nachdem das-Objekt das letzte Beispiel übermittelt hat. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Cpullpin. EndOf Stream-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366826"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="67ef3-104">Cpullpin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="67ef3-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="67ef3-105">Die- `EndOfStream` Methode wird aufgerufen, nachdem das-Objekt das letzte Beispiel übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="67ef3-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="67ef3-106">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="67ef3-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ef3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67ef3-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="67ef3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67ef3-108">Parameters</span></span>

<span data-ttu-id="67ef3-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67ef3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67ef3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67ef3-110">Return value</span></span>

<span data-ttu-id="67ef3-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="67ef3-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ef3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67ef3-112">Remarks</span></span>

<span data-ttu-id="67ef3-113">Verwenden Sie diese Methode, um [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="67ef3-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="67ef3-114">Wenn die Ausgabe-PIN (s) Ihres Filters von [**cbaseoutputpin**](cbaseoutputpin.md)abgeleitet ist, rufen Sie die [**cbaseoutputpin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="67ef3-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ef3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67ef3-115">Requirements</span></span>



| <span data-ttu-id="67ef3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67ef3-116">Requirement</span></span> | <span data-ttu-id="67ef3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="67ef3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ef3-118">Header</span><span class="sxs-lookup"><span data-stu-id="67ef3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="67ef3-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="67ef3-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="67ef3-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67ef3-120">Library</span></span><br/> | <dl> <span data-ttu-id="67ef3-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="67ef3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ef3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67ef3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ef3-123">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="67ef3-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




