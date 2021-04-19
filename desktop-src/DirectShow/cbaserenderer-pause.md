---
description: Die Pause-Methode hält den Filter an.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Cbaserderderer. Pause-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362152"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="fa6bb-103">Cbaserderderer. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="fa6bb-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="fa6bb-104">Die `Pause` Methode hält den Filter an.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa6bb-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="fa6bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa6bb-106">Parameters</span></span>

<span data-ttu-id="fa6bb-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa6bb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa6bb-108">Return value</span></span>

<span data-ttu-id="fa6bb-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fa6bb-110">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="fa6bb-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fa6bb-111">Return code</span></span>                                                                             | <span data-ttu-id="fa6bb-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa6bb-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="fa6bb-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bb-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fa6bb-114">Der Übergang ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="fa6bb-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bb-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fa6bb-116">Der Übergang ist nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa6bb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa6bb-117">Remarks</span></span>

<span data-ttu-id="fa6bb-118">Diese Methode überschreibt die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="fa6bb-119">Sie führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fa6bb-119">It performs the following steps:</span></span>

-   <span data-ttu-id="fa6bb-120">Ruft die **cbasefilter::P ause** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="fa6bb-121">Führt einen Commit für die Zuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-121">Commits the allocator.</span></span> <span data-ttu-id="fa6bb-122">(Weitere Informationen finden Sie unter [**imemzuordcator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="fa6bb-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="fa6bb-123">Wenn der vorherige Zustand beendet wurde, gibt der Filter jedes enthaltene Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="fa6bb-124">(Das Beispiel ist nicht mehr gültig.)</span><span class="sxs-lookup"><span data-stu-id="fa6bb-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="fa6bb-125">Ruft die [**cbaserenderer:: completestatechange**](cbaserenderer-completestatechange.md) -Methode auf und gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa6bb-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6bb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa6bb-126">Requirements</span></span>



| <span data-ttu-id="fa6bb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa6bb-127">Requirement</span></span> | <span data-ttu-id="fa6bb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fa6bb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6bb-129">Header</span><span class="sxs-lookup"><span data-stu-id="fa6bb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fa6bb-130"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bb-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa6bb-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa6bb-131">Library</span></span><br/> | <dl> <span data-ttu-id="fa6bb-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa6bb-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa6bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6bb-134">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fa6bb-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




