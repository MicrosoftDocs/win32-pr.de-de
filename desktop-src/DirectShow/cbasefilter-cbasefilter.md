---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) -Konstruktormethode.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT*) -Konstruktor (Amfilter.h)
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
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120108"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="32a1e-103">CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* ) -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="32a1e-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="32a1e-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="32a1e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32a1e-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="32a1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32a1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a1e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="32a1e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="32a1e-108">Zeiger auf eine Zeichenfolge, die den Namen des Filters enthält, zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="32a1e-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="32a1e-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="32a1e-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="32a1e-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="32a1e-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="32a1e-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="32a1e-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="32a1e-112">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="32a1e-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="32a1e-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="32a1e-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="32a1e-114">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32a1e-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="32a1e-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="32a1e-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="32a1e-116">Klassenbezeichner (CLSID) des Filters.</span><span class="sxs-lookup"><span data-stu-id="32a1e-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="32a1e-117">*Phr*</span><span class="sxs-lookup"><span data-stu-id="32a1e-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="32a1e-118">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="32a1e-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="32a1e-119">Der Konstruktor ignoriert diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="32a1e-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32a1e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32a1e-120">Remarks</span></span>

<span data-ttu-id="32a1e-121">Für das kritische Abschnittsobjekt würden Sie in der Regel einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="32a1e-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="32a1e-122">Leiten Sie eine Klasse ab, die sowohl **CBaseFilter** als auch **CCritSec** erbt.</span><span class="sxs-lookup"><span data-stu-id="32a1e-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="32a1e-123">Übergeben Sie für *pLock* den `this` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="32a1e-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="32a1e-124">Leiten Sie eine Klasse ab, die **CBaseFilter erbt** und eine **CCritSec-Membervariable** enthält.</span><span class="sxs-lookup"><span data-stu-id="32a1e-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="32a1e-125">Übergeben *Sie für pLock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="32a1e-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a1e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32a1e-126">Requirements</span></span>



| <span data-ttu-id="32a1e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32a1e-127">Requirement</span></span> | <span data-ttu-id="32a1e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="32a1e-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a1e-129">Header</span><span class="sxs-lookup"><span data-stu-id="32a1e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="32a1e-130"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="32a1e-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32a1e-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32a1e-131">Library</span></span><br/> | <dl> <span data-ttu-id="32a1e-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="32a1e-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a1e-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32a1e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a1e-134">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="32a1e-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




