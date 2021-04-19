---
description: Die completestatechange-Methode bestimmt, ob ein Übergang zum angehaltenen Zustand abgeschlossen ist.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Cbaserderderer. completestatechange-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370174"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="e00bf-103">Cbaserderderer. completestatechange-Methode</span><span class="sxs-lookup"><span data-stu-id="e00bf-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="e00bf-104">Die- `CompleteStateChange` Methode bestimmt, ob ein Übergang zum angehaltenen Zustand beendet ist.</span><span class="sxs-lookup"><span data-stu-id="e00bf-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e00bf-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="e00bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e00bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00bf-107">*OldState*</span><span class="sxs-lookup"><span data-stu-id="e00bf-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="e00bf-108">Zustand vor dem Übergang.</span><span class="sxs-lookup"><span data-stu-id="e00bf-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00bf-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e00bf-109">Return value</span></span>

<span data-ttu-id="e00bf-110">Gibt S \_ OK zurück, wenn der Übergang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="e00bf-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="e00bf-111">Andernfalls gibt S \_ false zurück.</span><span class="sxs-lookup"><span data-stu-id="e00bf-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00bf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e00bf-112">Remarks</span></span>

<span data-ttu-id="e00bf-113">Die [**cbaserererermethode::P ause**](cbaserenderer-pause.md) -Methode ruft diese Methode auf, um den Status Übergangsstatus zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e00bf-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="e00bf-114">Im Allgemeinen wird die Umstellung auf angehalten erst beendet, wenn der Filter ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="e00bf-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="e00bf-115">In einigen Situationen wird der Übergang jedoch sofort abgeschlossen, z. b. wenn der Filter nicht verbunden ist, oder wenn das Ende des Streams erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="e00bf-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="e00bf-116">Diese Methode überprüft die verschiedenen Kriterien und ruft dann die [**cbaserenderer:: Ready**](cbaserenderer-ready.md) -Methode oder die [**cbaserenderer:: notready**](cbaserenderer-notready.md) -Methode auf, um den Übergangsstatus zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e00bf-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00bf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e00bf-117">Requirements</span></span>



| <span data-ttu-id="e00bf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e00bf-118">Requirement</span></span> | <span data-ttu-id="e00bf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e00bf-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e00bf-120">Header</span><span class="sxs-lookup"><span data-stu-id="e00bf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e00bf-121"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e00bf-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e00bf-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e00bf-122">Library</span></span><br/> | <dl> <span data-ttu-id="e00bf-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e00bf-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00bf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e00bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00bf-125">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e00bf-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




