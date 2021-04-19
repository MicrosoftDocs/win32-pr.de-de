---
description: Die beginflush-Methode informiert den besitzenden Filter, um die downstreamfilter zu leeren. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Cpullpin. beginflush-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359391"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="d22f5-104">Cpullpin. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="d22f5-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="d22f5-105">Die- `BeginFlush` Methode informiert den besitzenden Filter, um die downstreamfilter zu leeren.</span><span class="sxs-lookup"><span data-stu-id="d22f5-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="d22f5-106">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="d22f5-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d22f5-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="d22f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d22f5-108">Parameters</span></span>

<span data-ttu-id="d22f5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d22f5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d22f5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d22f5-110">Return value</span></span>

<span data-ttu-id="d22f5-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d22f5-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d22f5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d22f5-112">Remarks</span></span>

<span data-ttu-id="d22f5-113">Die [**cpullpin:: Seek**](cpullpin-seek.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d22f5-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="d22f5-114">Implementieren Sie diese Methode, um die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="d22f5-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="d22f5-115">Wenn die Ausgabe-PIN (s) Ihres Filters von [**cbaseoutputpin**](cbaseoutputpin.md)abgeleitet ist, rufen Sie die [**cbaseoutputpin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d22f5-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="d22f5-116">Dieser Entwurf ermöglicht dem Filter, einfach durch Aufrufen von **Seek** im **cpullpin** -Objekt auf den Stream zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d22f5-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22f5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d22f5-117">Requirements</span></span>



| <span data-ttu-id="d22f5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d22f5-118">Requirement</span></span> | <span data-ttu-id="d22f5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d22f5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22f5-120">Header</span><span class="sxs-lookup"><span data-stu-id="d22f5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d22f5-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22f5-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d22f5-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d22f5-122">Library</span></span><br/> | <dl> <span data-ttu-id="d22f5-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d22f5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22f5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d22f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22f5-125">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d22f5-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




