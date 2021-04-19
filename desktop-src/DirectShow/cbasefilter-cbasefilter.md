---
description: Konstruktormethode.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Cbasefilter. cbasefilter (Konst TCHAR *, LPUNKNOWN, ccritsec*, Ref CLSID, HRESULT *)-Konstruktor (amfilter. h)
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373756"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="ff5b7-103">Cbasefilter. cbasefilter-Konstruktor (Konst TCHAR \* , LPUNKNOWN, ccritsec \* , Ref CLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="ff5b7-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="ff5b7-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5b7-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ff5b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5b7-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ff5b7-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5b7-108">Zeiger auf eine Zeichenfolge, die den Namen des Filters für Debugzwecke enthält.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b7-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="ff5b7-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5b7-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="ff5b7-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ff5b7-112">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b7-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="ff5b7-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5b7-114">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b7-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="ff5b7-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5b7-116">Klassen Bezeichner (CLSID) des Filters.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b7-117">*PHR*</span><span class="sxs-lookup"><span data-stu-id="ff5b7-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5b7-118">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ff5b7-119">Der Konstruktor ignoriert diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff5b7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff5b7-120">Remarks</span></span>

<span data-ttu-id="ff5b7-121">Für das Objekt "kritischer Abschnitt" würden Sie in der Regel eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="ff5b7-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="ff5b7-122">Leiten Sie eine Klasse ab, die sowohl **cbasefilter** als auch **ccritsec** erbt.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="ff5b7-123">Übergeben Sie für *Plock* den- `this` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="ff5b7-124">Leiten Sie eine Klasse ab, die **cbasefilter** erbt und eine **ccritsec** -Element Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="ff5b7-125">Übergeben Sie für *Plock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5b7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5b7-126">Requirements</span></span>



| <span data-ttu-id="ff5b7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff5b7-127">Requirement</span></span> | <span data-ttu-id="ff5b7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ff5b7-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5b7-129">Header</span><span class="sxs-lookup"><span data-stu-id="ff5b7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5b7-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b7-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff5b7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff5b7-131">Library</span></span><br/> | <dl> <span data-ttu-id="ff5b7-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b7-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5b7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff5b7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5b7-134">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff5b7-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




