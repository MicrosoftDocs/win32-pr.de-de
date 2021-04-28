---
description: 'CBaseMediaFilter.CBaseMediaFilter-Konstruktor : Konstruktormethode.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: CBaseMediaFilter.CBaseMediaFilter-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096318"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="47961-103">CBaseMediaFilter.CBaseMediaFilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="47961-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="47961-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="47961-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47961-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47961-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="47961-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47961-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="47961-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="47961-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="47961-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="47961-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="47961-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="47961-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="47961-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="47961-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="47961-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="47961-112">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="47961-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47961-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="47961-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="47961-114">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47961-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="47961-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="47961-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="47961-116">Klassenbezeichner des Objekts.</span><span class="sxs-lookup"><span data-stu-id="47961-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47961-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47961-117">Remarks</span></span>

<span data-ttu-id="47961-118">Wenn ein anderes Objekt das Objekt enthält oder aggregiert, kann `CBaseMediaFilter` die **CCritSec-Sperre** für das Objekt extern `CBaseMediaFilter` sein.</span><span class="sxs-lookup"><span data-stu-id="47961-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="47961-119">Übergeben Sie in diesem Fall einen Zeiger auf die Sperre in *pLock*.</span><span class="sxs-lookup"><span data-stu-id="47961-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="47961-120">Andernfalls können Sie:</span><span class="sxs-lookup"><span data-stu-id="47961-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="47961-121">Leiten Sie eine Klasse ab, die sowohl als auch `CBaseMediaFilter` **CCritSec erbt.**</span><span class="sxs-lookup"><span data-stu-id="47961-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="47961-122">Übergeben *Sie für pLock* den this-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="47961-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="47961-123">Leiten Sie eine Klasse ab, die eine `CBaseMediaFilter` **CCritSec-Membervariable erbt und** enthält.</span><span class="sxs-lookup"><span data-stu-id="47961-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="47961-124">Übergeben Sie für *pLock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="47961-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="47961-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47961-125">Requirements</span></span>



| <span data-ttu-id="47961-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47961-126">Requirement</span></span> | <span data-ttu-id="47961-127">Wert</span><span class="sxs-lookup"><span data-stu-id="47961-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47961-128">Header</span><span class="sxs-lookup"><span data-stu-id="47961-128">Header</span></span><br/>  | <dl> <span data-ttu-id="47961-129"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="47961-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="47961-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47961-130">Library</span></span><br/> | <dl> <span data-ttu-id="47961-131"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="47961-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47961-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47961-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47961-133">**CBaseMediaFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="47961-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




