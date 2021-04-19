---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode überschreibt die cbasepin:: EndOf Stream-Methode.'
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Crendererinputpin. EndOf Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372742"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="062a5-104">Crendererinputpin. EndOf Stream-Methode</span><span class="sxs-lookup"><span data-stu-id="062a5-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="062a5-105">Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="062a5-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="062a5-106">Diese Methode überschreibt die [**cbasepin:: EndOf Stream**](cbasepin-endofstream.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="062a5-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="062a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="062a5-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="062a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="062a5-108">Parameters</span></span>

<span data-ttu-id="062a5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="062a5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="062a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="062a5-110">Return value</span></span>

<span data-ttu-id="062a5-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="062a5-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="062a5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="062a5-112">Requirements</span></span>



| <span data-ttu-id="062a5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="062a5-113">Requirement</span></span> | <span data-ttu-id="062a5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="062a5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062a5-115">Header</span><span class="sxs-lookup"><span data-stu-id="062a5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="062a5-116"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="062a5-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="062a5-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="062a5-117">Library</span></span><br/> | <dl> <span data-ttu-id="062a5-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="062a5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="062a5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="062a5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062a5-120">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="062a5-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




