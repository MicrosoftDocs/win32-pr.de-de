---
description: Die Ready-Methode signalisiert, dass ein Zustandsübergang abgeschlossen ist.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Cbaserderderer. Ready-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369280"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="c7211-103">Cbaserderderer. Ready-Methode</span><span class="sxs-lookup"><span data-stu-id="c7211-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="c7211-104">Die- `Ready` Methode signalisiert, dass ein Zustandsübergang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="c7211-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7211-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7211-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="c7211-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7211-106">Parameters</span></span>

<span data-ttu-id="c7211-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7211-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7211-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7211-108">Return value</span></span>

<span data-ttu-id="c7211-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c7211-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7211-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7211-110">Remarks</span></span>

<span data-ttu-id="c7211-111">Diese Methode bewirkt, dass die [**cbasergetderer:: GetState**](cbaserenderer-getstate.md) -Methode "S OK" zurückgibt \_ , was bedeutet, dass der Filter den Übergang in seinen aktuellen Zustand abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="c7211-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="c7211-112">Der Filter ruft diese Methode immer dann auf, wenn Sie einen Zustandsübergang abschließt.</span><span class="sxs-lookup"><span data-stu-id="c7211-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7211-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7211-113">Requirements</span></span>



| <span data-ttu-id="c7211-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7211-114">Requirement</span></span> | <span data-ttu-id="c7211-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7211-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7211-116">Header</span><span class="sxs-lookup"><span data-stu-id="c7211-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c7211-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7211-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7211-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7211-118">Library</span></span><br/> | <dl> <span data-ttu-id="c7211-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c7211-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7211-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7211-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7211-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c7211-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="c7211-122">**Cbaserererderer:: checkready**</span><span class="sxs-lookup"><span data-stu-id="c7211-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="c7211-123">**Cbaserderderer:: notready**</span><span class="sxs-lookup"><span data-stu-id="c7211-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




