---
description: Die onstartstreaming-Methode wird aufgerufen, wenn der Filter das Streaming startet.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Cbaserderderer. onstartstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366685"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="04cc6-103">Cbaserderderer. onstartstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="04cc6-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="04cc6-104">Die- `OnStartStreaming` Methode wird aufgerufen, wenn der Filter das Streaming startet.</span><span class="sxs-lookup"><span data-stu-id="04cc6-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="04cc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04cc6-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="04cc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04cc6-106">Parameters</span></span>

<span data-ttu-id="04cc6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="04cc6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04cc6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04cc6-108">Return value</span></span>

<span data-ttu-id="04cc6-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="04cc6-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="04cc6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04cc6-110">Remarks</span></span>

<span data-ttu-id="04cc6-111">Die [**cbaserdenderer:: startstreaming**](cbaserenderer-startstreaming.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="04cc6-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="04cc6-112">Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="04cc6-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="04cc6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04cc6-113">Requirements</span></span>



| <span data-ttu-id="04cc6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04cc6-114">Requirement</span></span> | <span data-ttu-id="04cc6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="04cc6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04cc6-116">Header</span><span class="sxs-lookup"><span data-stu-id="04cc6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="04cc6-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04cc6-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04cc6-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04cc6-118">Library</span></span><br/> | <dl> <span data-ttu-id="04cc6-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04cc6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04cc6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04cc6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04cc6-121">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04cc6-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




