---
description: Konstruktormethode.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: CSource. CSource-Konstruktor (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 992775659d5f9838ef63b15c5395998f1faf6200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353817"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="2888f-103">CSource. CSource-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="2888f-103">CSource.CSource constructor</span></span>

<span data-ttu-id="2888f-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2888f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2888f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2888f-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="2888f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2888f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2888f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="2888f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="2888f-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="2888f-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="2888f-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="2888f-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="2888f-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="2888f-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="2888f-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="2888f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="2888f-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="2888f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="2888f-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2888f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2888f-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="2888f-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="2888f-115">Klassen Bezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="2888f-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2888f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2888f-116">Requirements</span></span>



| <span data-ttu-id="2888f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2888f-117">Requirement</span></span> | <span data-ttu-id="2888f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2888f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2888f-119">Header</span><span class="sxs-lookup"><span data-stu-id="2888f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2888f-120"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2888f-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2888f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2888f-121">Library</span></span><br/> | <dl> <span data-ttu-id="2888f-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2888f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2888f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2888f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2888f-124">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2888f-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




