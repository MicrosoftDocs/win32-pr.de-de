---
description: Konstruktormethode.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Cbasefilter. cbasefilter (Konst TCHAR *, LPUNKNOWN, ccritsec*, Ref-sid) Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358249"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="4ff80-103">Cbasefilter. cbasefilter-Konstruktor (Konst TCHAR \* , LPUNKNOWN, ccritsec \* , Ref CLSID)</span><span class="sxs-lookup"><span data-stu-id="4ff80-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="4ff80-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4ff80-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ff80-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="4ff80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ff80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff80-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4ff80-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff80-108">Zeiger auf eine Zeichenfolge, die den Namen des Filters für Debugzwecke enthält.</span><span class="sxs-lookup"><span data-stu-id="4ff80-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="4ff80-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="4ff80-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff80-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ff80-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="4ff80-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ff80-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4ff80-112">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="4ff80-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ff80-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="4ff80-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff80-114">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ff80-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="4ff80-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="4ff80-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff80-116">Klassen Bezeichner (CLSID) des Filters.</span><span class="sxs-lookup"><span data-stu-id="4ff80-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ff80-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ff80-117">Remarks</span></span>

<span data-ttu-id="4ff80-118">Für das Objekt "kritischer Abschnitt" würden Sie in der Regel eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="4ff80-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="4ff80-119">Leiten Sie eine Klasse ab, die sowohl **cbasefilter** als auch **ccritsec** erbt.</span><span class="sxs-lookup"><span data-stu-id="4ff80-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="4ff80-120">Übergeben Sie für *Plock* den- `this` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4ff80-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="4ff80-121">Leiten Sie eine Klasse ab, die **cbasefilter** erbt und eine **ccritsec** -Element Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="4ff80-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="4ff80-122">Übergeben Sie für *Plock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ff80-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff80-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ff80-123">Requirements</span></span>



| <span data-ttu-id="4ff80-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ff80-124">Requirement</span></span> | <span data-ttu-id="4ff80-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4ff80-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff80-126">Header</span><span class="sxs-lookup"><span data-stu-id="4ff80-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4ff80-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ff80-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ff80-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ff80-128">Library</span></span><br/> | <dl> <span data-ttu-id="4ff80-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4ff80-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ff80-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ff80-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff80-131">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4ff80-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




