---
description: Die startstreaming-Methode initiiert das Streaming, wenn der Filter in den Status wird ausgeführt wechselt.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Cbaserderderer. startstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352135"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="88141-103">Cbaserderderer. startstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="88141-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="88141-104">Die- `StartStreaming` Methode initiiert das Streaming, wenn der Filter in den Status wird ausgeführt wechselt.</span><span class="sxs-lookup"><span data-stu-id="88141-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="88141-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88141-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="88141-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88141-106">Parameters</span></span>

<span data-ttu-id="88141-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="88141-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88141-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88141-108">Return value</span></span>

<span data-ttu-id="88141-109">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="88141-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88141-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88141-110">Remarks</span></span>

<span data-ttu-id="88141-111">Wenn der Filter ein Beispiel enthält, wird das Beispiel für das Rendering geplant.</span><span class="sxs-lookup"><span data-stu-id="88141-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="88141-112">Andernfalls sendet der Filter ein Ereignis vom Typ " [**EC \_ Complete**](ec-complete.md) " an den Filter Graph-Manager, wenn eine ausstehende streambenachrichtigung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="88141-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="88141-113">Diese Methode ruft die [**cbaserdenderer:: onstartstreaming**](cbaserenderer-onstartstreaming.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="88141-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="88141-114">Diese Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="88141-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="88141-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88141-115">Requirements</span></span>



| <span data-ttu-id="88141-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88141-116">Requirement</span></span> | <span data-ttu-id="88141-117">Wert</span><span class="sxs-lookup"><span data-stu-id="88141-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88141-118">Header</span><span class="sxs-lookup"><span data-stu-id="88141-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88141-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88141-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88141-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88141-120">Library</span></span><br/> | <dl> <span data-ttu-id="88141-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88141-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88141-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88141-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88141-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88141-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




