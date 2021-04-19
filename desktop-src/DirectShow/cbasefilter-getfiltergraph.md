---
description: Die getfiltergraph-Methode ruft einen Zeiger auf den Filter Diagramm-Manager ab.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Cbasefilter. getfiltergraph-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370153"
---
# <a name="cbasefiltergetfiltergraph-method"></a><span data-ttu-id="e8691-103">Cbasefilter. getfiltergraph-Methode</span><span class="sxs-lookup"><span data-stu-id="e8691-103">CBaseFilter.GetFilterGraph method</span></span>

<span data-ttu-id="e8691-104">Die- `GetFilterGraph` Methode ruft einen Zeiger auf den Filter Diagramm-Manager ab.</span><span class="sxs-lookup"><span data-stu-id="e8691-104">The `GetFilterGraph` method retrieves a pointer to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8691-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8691-105">Syntax</span></span>


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a><span data-ttu-id="e8691-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8691-106">Parameters</span></span>

<span data-ttu-id="e8691-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e8691-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8691-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8691-108">Return value</span></span>

<span data-ttu-id="e8691-109">Gibt den Wert von [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="e8691-109">Returns the value of [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8691-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8691-110">Requirements</span></span>



| <span data-ttu-id="e8691-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8691-111">Requirement</span></span> | <span data-ttu-id="e8691-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e8691-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8691-113">Header</span><span class="sxs-lookup"><span data-stu-id="e8691-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e8691-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8691-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8691-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8691-115">Library</span></span><br/> | <dl> <span data-ttu-id="e8691-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e8691-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8691-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8691-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8691-118">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e8691-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




