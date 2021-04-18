---
description: Die endflush-Methode beendet einen Löschvorgang.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Cbaserderderer. endflush-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361312"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="a49c2-103">Cbaserderderer. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="a49c2-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="a49c2-104">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="a49c2-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a49c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a49c2-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="a49c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a49c2-106">Parameters</span></span>

<span data-ttu-id="a49c2-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a49c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a49c2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a49c2-108">Return value</span></span>

<span data-ttu-id="a49c2-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a49c2-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a49c2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a49c2-110">Remarks</span></span>

<span data-ttu-id="a49c2-111">Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie einen Aufruf an die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode empfängt.</span><span class="sxs-lookup"><span data-stu-id="a49c2-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a49c2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a49c2-112">Requirements</span></span>



| <span data-ttu-id="a49c2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a49c2-113">Requirement</span></span> | <span data-ttu-id="a49c2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a49c2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49c2-115">Header</span><span class="sxs-lookup"><span data-stu-id="a49c2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a49c2-116"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a49c2-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a49c2-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a49c2-117">Library</span></span><br/> | <dl> <span data-ttu-id="a49c2-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a49c2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a49c2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a49c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49c2-120">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a49c2-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




