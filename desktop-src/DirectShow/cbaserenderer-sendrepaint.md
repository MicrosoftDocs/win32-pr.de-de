---
description: Die sendrepaint-Methode sendet ein Repaint-Ereignis an den Filter Graph-Manager.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Cbaserderderer. sendrepaint-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365495"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="01574-103">Cbaserderderer. sendrepaint-Methode</span><span class="sxs-lookup"><span data-stu-id="01574-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="01574-104">Die- `SendRepaint` Methode sendet ein Repaint-Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="01574-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="01574-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01574-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="01574-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01574-106">Parameters</span></span>

<span data-ttu-id="01574-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="01574-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01574-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01574-108">Return value</span></span>

<span data-ttu-id="01574-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="01574-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01574-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01574-110">Remarks</span></span>

<span data-ttu-id="01574-111">Diese Methode sendet ein [**EC \_ Repaint**](ec-repaint.md) -Ereignis an den Filter Graph-Manager, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="01574-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="01574-112">Die eingabepin ist verbunden.</span><span class="sxs-lookup"><span data-stu-id="01574-112">The input pin is connected.</span></span>
-   <span data-ttu-id="01574-113">Der Filter gibt keine Daten aus.</span><span class="sxs-lookup"><span data-stu-id="01574-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="01574-114">Das Ende des Streams wurde nicht erreicht.</span><span class="sxs-lookup"><span data-stu-id="01574-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="01574-115">Das [**cbaserderderer:: m \_ babort**](cbaserenderer-m-babort.md) -Flag ist **false**.</span><span class="sxs-lookup"><span data-stu-id="01574-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="01574-116">Das Flag " [**cbaserderderer:: m \_ brepaintstatus**](cbaserenderer-m-brepaintstatus.md) " ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="01574-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="01574-117">Abhängig vom Status des Diagramms kann das EC \_ Repaint-Ereignis bewirken, dass der upstreamfilter eine Stichprobe erneut sendet, das Filter Diagramm, um den aktuellen Speicherort zu suchen, oder den Filter-Graph-Manager, um vorübergehend anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="01574-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="01574-118">(Siehe [**EC \_ Repaint**](ec-repaint.md).) Dieses Ereignis ist potenziell ineffizient und sollte daher sparsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01574-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="01574-119">Videorenderer müssen jedoch manchmal die Anzeige aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="01574-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="01574-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01574-120">Requirements</span></span>



| <span data-ttu-id="01574-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01574-121">Requirement</span></span> | <span data-ttu-id="01574-122">Wert</span><span class="sxs-lookup"><span data-stu-id="01574-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01574-123">Header</span><span class="sxs-lookup"><span data-stu-id="01574-123">Header</span></span><br/>  | <dl> <span data-ttu-id="01574-124"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01574-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01574-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01574-125">Library</span></span><br/> | <dl> <span data-ttu-id="01574-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="01574-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01574-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01574-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01574-128">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="01574-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




