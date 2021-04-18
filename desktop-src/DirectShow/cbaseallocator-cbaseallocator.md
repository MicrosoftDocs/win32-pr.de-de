---
description: Konstruktormethode.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Cbasezucator. cbasezucator-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358193"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="ab0a3-103">Cbasezucator. cbasezucator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ab0a3-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="ab0a3-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab0a3-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="ab0a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab0a3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ab0a3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ab0a3-108">Zeiger auf eine Zeichenfolge, die den debugnamen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="ab0a3-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ab0a3-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab0a3-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="ab0a3-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ab0a3-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="ab0a3-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ab0a3-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab0a3-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="ab0a3-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ab0a3-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ab0a3-116">Legen Sie \_ vor dem Erstellen des Objekts den Wert auf S OK fest.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ab0a3-117">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="ab0a3-118">*bevent*</span><span class="sxs-lookup"><span data-stu-id="ab0a3-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="ab0a3-119">Boolescher Wert, der angibt, ob ein Semaphor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="ab0a3-120">Wenn **true**, erstellt die Zuweisung ein Semaphor ([**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md)), das signalisiert wird, wenn ein Beispiel verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="ab0a3-121">Legen Sie den Wert auf **false** fest, wenn Sie eine abgeleitete Klasse implementieren, die keine Semaphore erfordert.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="ab0a3-122">*fenablereleasecallback*</span><span class="sxs-lookup"><span data-stu-id="ab0a3-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="ab0a3-123">Boolescher Wert, der angibt, ob der Release-Rückrufmechanismus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="ab0a3-124">Legen Sie den Wert auf **true** fest, wenn Sie eine Rückruf Schnittstelle angeben möchten, die aufgerufen wird, wenn Puffer freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="ab0a3-125">Geben Sie den Rückruf an, indem Sie die [**cbasezucator:: setnotify**](cbaseallocator-setnotify.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ab0a3-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab0a3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab0a3-126">Requirements</span></span>



| <span data-ttu-id="ab0a3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab0a3-127">Requirement</span></span> | <span data-ttu-id="ab0a3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ab0a3-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0a3-129">Header</span><span class="sxs-lookup"><span data-stu-id="ab0a3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ab0a3-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0a3-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab0a3-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab0a3-131">Library</span></span><br/> | <dl> <span data-ttu-id="ab0a3-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0a3-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab0a3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab0a3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0a3-134">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab0a3-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




