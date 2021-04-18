---
description: Die onwaitend-Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Cbaserenderer. onwaitend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358140"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="e0079-103">Cbaserenderer. onwaitend-Methode</span><span class="sxs-lookup"><span data-stu-id="e0079-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="e0079-104">Die `OnWaitEnd` -Methode wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet.</span><span class="sxs-lookup"><span data-stu-id="e0079-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0079-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0079-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="e0079-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0079-106">Parameters</span></span>

<span data-ttu-id="e0079-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e0079-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0079-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0079-108">Return value</span></span>

<span data-ttu-id="e0079-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0079-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0079-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0079-110">Remarks</span></span>

<span data-ttu-id="e0079-111">Die [**cbaserderderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode ruft diese Methode auf, wenn Sie mit dem warten auf die Präsentationszeit eines Beispiels fertig ist.</span><span class="sxs-lookup"><span data-stu-id="e0079-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="e0079-112">Diese Methode führt in der Basisklasse keine Aktionen aus, Sie kann jedoch von der abgeleiteten Klasse überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e0079-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="e0079-113">Wenn Sie die Qualitätskontrolle implementieren, können Sie diese Methode zusammen mit der [**cbaserdenderer:: onwaitstart**](cbaserenderer-onwaitstart.md) -Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="e0079-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="e0079-114">Sie können diese Methoden verwenden, um die Leistung des Filters zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="e0079-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0079-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0079-115">Requirements</span></span>



| <span data-ttu-id="e0079-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0079-116">Requirement</span></span> | <span data-ttu-id="e0079-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e0079-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0079-118">Header</span><span class="sxs-lookup"><span data-stu-id="e0079-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e0079-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0079-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0079-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0079-120">Library</span></span><br/> | <dl> <span data-ttu-id="e0079-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e0079-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0079-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0079-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0079-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e0079-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




