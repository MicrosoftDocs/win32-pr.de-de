---
description: Die waitforrendertime-Methode wartet auf die Präsentationszeit des aktuellen Beispiels.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Cbaserderderer. waitforrendertime-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364037"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="76b92-103">Cbaserderderer. waitforrendertime-Methode</span><span class="sxs-lookup"><span data-stu-id="76b92-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="76b92-104">Die `WaitForRenderTime` -Methode wartet auf die Präsentationszeit des aktuellen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="76b92-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b92-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="76b92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76b92-106">Parameters</span></span>

<span data-ttu-id="76b92-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="76b92-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76b92-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76b92-108">Return value</span></span>

<span data-ttu-id="76b92-109">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="76b92-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="76b92-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76b92-110">Return code</span></span>                                                                                           | <span data-ttu-id="76b92-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76b92-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76b92-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76b92-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="76b92-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="76b92-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="76b92-114"><dt>**VFW \_ E \_ Status \_ geändert**</dt></span><span class="sxs-lookup"><span data-stu-id="76b92-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="76b92-115">Der Filter Zustand wurde vor dem Eintreffen der Präsentationszeit geändert.</span><span class="sxs-lookup"><span data-stu-id="76b92-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76b92-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76b92-116">Remarks</span></span>

<span data-ttu-id="76b92-117">Diese Methode wartet, bis eine der folgenden Aktionen auftritt:</span><span class="sxs-lookup"><span data-stu-id="76b92-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="76b92-118">Die Präsentationszeit des Beispiels kommt an, an der Stelle, an der das Beispiel gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="76b92-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="76b92-119">Der Filter beendet oder beginnt mit dem leeren von Daten.</span><span class="sxs-lookup"><span data-stu-id="76b92-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="76b92-120">Wenn die Präsentationszeit erreicht wird, wird das Ereignis [**cbasererderderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) signalisiert.</span><span class="sxs-lookup"><span data-stu-id="76b92-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="76b92-121">Wenn sich der Status ändert, wird das Ereignis [**cbaserererererertderer:: m \_ threadsignal**](cbaserenderer-m-threadsignal.md) signalisiert.</span><span class="sxs-lookup"><span data-stu-id="76b92-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="76b92-122">Diese Methode wartet auf beide Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="76b92-122">This method waits on both events.</span></span> <span data-ttu-id="76b92-123">Die abgeleitete Klasse kann diese Methode überschreiben, um ggf. auf zusätzliche Ereignisse zu warten.</span><span class="sxs-lookup"><span data-stu-id="76b92-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="76b92-124">Diese Methode ruft die [**cbaserenderer:: onwaitstart**](cbaserenderer-onwaitstart.md) -Methode auf, wenn der Warte Vorgang beginnt, und die [**cbaserenderer:: onwaitend**](cbaserenderer-onwaitend.md) -Methode, wenn der Warte Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="76b92-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="76b92-125">Keine der Methoden führt etwas in der Basisklasse aus, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="76b92-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b92-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b92-126">Requirements</span></span>



| <span data-ttu-id="76b92-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76b92-127">Requirement</span></span> | <span data-ttu-id="76b92-128">Wert</span><span class="sxs-lookup"><span data-stu-id="76b92-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b92-129">Header</span><span class="sxs-lookup"><span data-stu-id="76b92-129">Header</span></span><br/>  | <dl> <span data-ttu-id="76b92-130"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76b92-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="76b92-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76b92-131">Library</span></span><br/> | <dl> <span data-ttu-id="76b92-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="76b92-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76b92-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76b92-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b92-134">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="76b92-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




