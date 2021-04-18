---
description: Die onstopstreaming-Methode wird aufgerufen, wenn der Filter das Streaming stoppt.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Cbaserderderer. onstopstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372747"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="f49a1-103">Cbaserderderer. onstopstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="f49a1-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="f49a1-104">Die- `OnStopStreaming` Methode wird aufgerufen, wenn der Filter das Streaming stoppt.</span><span class="sxs-lookup"><span data-stu-id="f49a1-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="f49a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f49a1-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="f49a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f49a1-106">Parameters</span></span>

<span data-ttu-id="f49a1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f49a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f49a1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f49a1-108">Return value</span></span>

<span data-ttu-id="f49a1-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f49a1-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f49a1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f49a1-110">Remarks</span></span>

<span data-ttu-id="f49a1-111">Die [**cbaserdenderer:: stopstreaming**](cbaserenderer-stopstreaming.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f49a1-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="f49a1-112">Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f49a1-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f49a1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f49a1-113">Requirements</span></span>



| <span data-ttu-id="f49a1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f49a1-114">Requirement</span></span> | <span data-ttu-id="f49a1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f49a1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f49a1-116">Header</span><span class="sxs-lookup"><span data-stu-id="f49a1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f49a1-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f49a1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f49a1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f49a1-118">Library</span></span><br/> | <dl> <span data-ttu-id="f49a1-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f49a1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f49a1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f49a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f49a1-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f49a1-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




