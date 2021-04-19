---
description: Die notready-Methode signalisiert, dass ein Zustandsübergang noch nicht beendet ist.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Cbaserderderer. notready-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367195"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="c3899-103">Cbaserderderer. notready-Methode</span><span class="sxs-lookup"><span data-stu-id="c3899-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="c3899-104">Die- `NotReady` Methode signalisiert, dass ein Zustandsübergang noch nicht beendet ist.</span><span class="sxs-lookup"><span data-stu-id="c3899-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3899-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3899-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="c3899-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3899-106">Parameters</span></span>

<span data-ttu-id="c3899-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c3899-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3899-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3899-108">Return value</span></span>

<span data-ttu-id="c3899-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c3899-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3899-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3899-110">Remarks</span></span>

<span data-ttu-id="c3899-111">Diese Methode bewirkt, dass die [**cbaserenderer:: GetState**](cbaserenderer-getstate.md) -Methode VFW \_ S \_ State Intermediate zurückgibt \_ , wodurch angegeben wird, dass der Filter weiterhin in seinen aktuellen Zustand übergeht.</span><span class="sxs-lookup"><span data-stu-id="c3899-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="c3899-112">Der Filter ruft diese Methode auf, wenn ein Zustandsübergang aussteht.</span><span class="sxs-lookup"><span data-stu-id="c3899-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="c3899-113">(Dies tritt auf, wenn der Filter angehalten wird, bis er ein Beispiel empfängt.)</span><span class="sxs-lookup"><span data-stu-id="c3899-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="c3899-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3899-114">Requirements</span></span>



| <span data-ttu-id="c3899-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3899-115">Requirement</span></span> | <span data-ttu-id="c3899-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c3899-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3899-117">Header</span><span class="sxs-lookup"><span data-stu-id="c3899-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3899-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3899-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3899-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3899-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3899-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c3899-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3899-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3899-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3899-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c3899-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="c3899-123">**Prüfbereit**</span><span class="sxs-lookup"><span data-stu-id="c3899-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="c3899-124">**Bereit**</span><span class="sxs-lookup"><span data-stu-id="c3899-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




