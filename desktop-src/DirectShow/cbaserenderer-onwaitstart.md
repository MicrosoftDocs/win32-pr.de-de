---
description: Die onwaitstart-Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Cbaserderderer. onwaitstart-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362153"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="229e6-103">Cbaserderderer. onwaitstart-Methode</span><span class="sxs-lookup"><span data-stu-id="229e6-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="229e6-104">Die `OnWaitStart` -Methode wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten.</span><span class="sxs-lookup"><span data-stu-id="229e6-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="229e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="229e6-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="229e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="229e6-106">Parameters</span></span>

<span data-ttu-id="229e6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="229e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="229e6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="229e6-108">Return value</span></span>

<span data-ttu-id="229e6-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="229e6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="229e6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="229e6-110">Remarks</span></span>

<span data-ttu-id="229e6-111">Die [**cbaserderderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode ruft diese Methode auf, wenn Sie beginnt, auf die Präsentationszeit eines Beispiels zu warten.</span><span class="sxs-lookup"><span data-stu-id="229e6-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="229e6-112">Diese Methode führt in der Basisklasse keine Aktionen aus, Sie kann jedoch von der abgeleiteten Klasse überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="229e6-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="229e6-113">Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**cbaserenderer:: onwaitend**](cbaserenderer-onwaitend.md) -Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="229e6-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="229e6-114">Sie können diese Methoden verwenden, um die Leistung des Filters zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="229e6-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="229e6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="229e6-115">Requirements</span></span>



| <span data-ttu-id="229e6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="229e6-116">Requirement</span></span> | <span data-ttu-id="229e6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="229e6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="229e6-118">Header</span><span class="sxs-lookup"><span data-stu-id="229e6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="229e6-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="229e6-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="229e6-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="229e6-120">Library</span></span><br/> | <dl> <span data-ttu-id="229e6-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="229e6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229e6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="229e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229e6-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="229e6-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




