---
description: Die completeconnect-Methode schließt eine Verbindung mit einer Eingabe-PIN ab.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Cdynamicoutputpin. completeconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367142"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="2a27f-103">Cdynamicoutputpin. completeconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="2a27f-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="2a27f-104">Die- `CompleteConnect` Methode schließt eine Verbindung mit einer Eingabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="2a27f-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a27f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a27f-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="2a27f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a27f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a27f-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="2a27f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="2a27f-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="2a27f-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a27f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a27f-109">Return value</span></span>

<span data-ttu-id="2a27f-110">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="2a27f-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a27f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a27f-111">Remarks</span></span>

<span data-ttu-id="2a27f-112">Diese Methode überschreibt die [**cbaseoutputpin:: completeconnect**](cbaseoutputpin-completeconnect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2a27f-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="2a27f-113">Zur Unterstützung dynamischer Neuverbindungen führt diese Methode einen Commit für die Zuweisung aus, wenn der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2a27f-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="2a27f-114">In der Basisklasse können Verbindungen nur auftreten, wenn der Filter angehalten wird, sodass für die Zuweisung immer ein Commit in der [**cbaseoutputpin:: Active**](cbaseoutputpin-active.md) -Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a27f-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a27f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a27f-115">Requirements</span></span>



| <span data-ttu-id="2a27f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a27f-116">Requirement</span></span> | <span data-ttu-id="2a27f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2a27f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a27f-118">Header</span><span class="sxs-lookup"><span data-stu-id="2a27f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2a27f-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a27f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2a27f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a27f-120">Library</span></span><br/> | <dl> <span data-ttu-id="2a27f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2a27f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a27f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a27f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a27f-123">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2a27f-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




