---
description: Die onwaitend-Methode wird aufgerufen, wenn eine Wartezeit endet.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Cbasevideorenderer. onwaitend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358258"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="7bd52-103">Cbasevideorenderer. onwaitend-Methode</span><span class="sxs-lookup"><span data-stu-id="7bd52-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="7bd52-104">Die onwaitend-Methode wird aufgerufen, wenn eine Wartezeit endet.</span><span class="sxs-lookup"><span data-stu-id="7bd52-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bd52-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="7bd52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd52-106">Parameters</span></span>

<span data-ttu-id="7bd52-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7bd52-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bd52-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bd52-108">Return value</span></span>

<span data-ttu-id="7bd52-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7bd52-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd52-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bd52-110">Remarks</span></span>

<span data-ttu-id="7bd52-111">Diese Member-Funktion führt nur die Leistungs Protokollierung durch.</span><span class="sxs-lookup"><span data-stu-id="7bd52-111">This member function does only performance logging.</span></span> <span data-ttu-id="7bd52-112">Sie wird aufgerufen, wenn der Thread nicht im Fenster wartet oder das nächste Beispiel als gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="7bd52-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="7bd52-113">Es könnte schließlich verwendet werden, um Informationen zu sammeln, die die Synchronisierung steuern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd52-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bd52-114">Requirements</span></span>



| <span data-ttu-id="7bd52-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bd52-115">Requirement</span></span> | <span data-ttu-id="7bd52-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7bd52-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd52-117">Header</span><span class="sxs-lookup"><span data-stu-id="7bd52-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7bd52-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bd52-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7bd52-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bd52-119">Library</span></span><br/> | <dl> <span data-ttu-id="7bd52-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7bd52-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd52-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd52-122">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7bd52-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




