---
description: Konstruktormethode.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Cbasemediafilter. cbasemediafilter-Konstruktor (amfilter. h)
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
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351220"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="ef69a-103">Cbasemediafilter. cbasemediafilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ef69a-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="ef69a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ef69a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef69a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef69a-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="ef69a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef69a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef69a-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ef69a-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ef69a-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ef69a-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ef69a-109">*Kro*</span><span class="sxs-lookup"><span data-stu-id="ef69a-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ef69a-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef69a-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="ef69a-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef69a-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ef69a-112">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ef69a-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef69a-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="ef69a-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ef69a-114">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef69a-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="ef69a-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="ef69a-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="ef69a-116">Klassen Bezeichner des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef69a-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef69a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef69a-117">Remarks</span></span>

<span data-ttu-id="ef69a-118">Wenn ein anderes Objekt das Objekt enthält oder aggregiert `CBaseMediaFilter` , kann die **ccritsec** -Sperre für das Objekt extern sein `CBaseMediaFilter` .</span><span class="sxs-lookup"><span data-stu-id="ef69a-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="ef69a-119">Übergeben Sie in diesem Fall einen Zeiger auf die Sperre in *Plock*.</span><span class="sxs-lookup"><span data-stu-id="ef69a-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="ef69a-120">Andernfalls können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="ef69a-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="ef69a-121">Leiten Sie eine Klasse ab, die sowohl `CBaseMediaFilter` als auch **ccritsec** erbt.</span><span class="sxs-lookup"><span data-stu-id="ef69a-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="ef69a-122">Übergeben Sie für *Plock* den this-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ef69a-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="ef69a-123">Leiten Sie eine Klasse ab, die erbt `CBaseMediaFilter` und eine **ccritsec** -Element Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="ef69a-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="ef69a-124">Übergeben Sie für *Plock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef69a-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef69a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef69a-125">Requirements</span></span>



| <span data-ttu-id="ef69a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef69a-126">Requirement</span></span> | <span data-ttu-id="ef69a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ef69a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef69a-128">Header</span><span class="sxs-lookup"><span data-stu-id="ef69a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ef69a-129"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef69a-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef69a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef69a-130">Library</span></span><br/> | <dl> <span data-ttu-id="ef69a-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ef69a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef69a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef69a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef69a-133">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ef69a-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




