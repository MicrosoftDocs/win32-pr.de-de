---
description: 'CBaseAllocator.CBaseAllocator-Konstruktor : Konstruktormethode.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: CBaseAllocator.CBaseAllocator-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: dfda2b03d1ddb3f4a8ad5f4446dbee997da4e790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096359"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="9a025-103">CBaseAllocator.CBaseAllocator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="9a025-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="9a025-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="9a025-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a025-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a025-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="9a025-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a025-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9a025-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9a025-108">Zeiger auf eine Zeichenfolge, die den Debugnamen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="9a025-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="9a025-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9a025-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a025-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="9a025-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9a025-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a025-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9a025-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a025-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9a025-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="9a025-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9a025-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="9a025-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9a025-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="9a025-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="9a025-116">Legen Sie den Wert auf S \_ OK fest, bevor Sie das -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a025-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="9a025-117">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9a025-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="9a025-118">*bEvent*</span><span class="sxs-lookup"><span data-stu-id="9a025-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="9a025-119">Boolescher Wert, der angibt, ob ein Semaphor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a025-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="9a025-120">True **gibt an,** dass die Zuweisung ein Semaphor ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)) erstellt, das signalisiert wird, wenn ein Beispiel verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="9a025-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="9a025-121">Legen Sie den Wert auf **FALSE** fest, wenn Sie eine abgeleitete Klasse implementieren, die kein Semaphor erfordert.</span><span class="sxs-lookup"><span data-stu-id="9a025-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="9a025-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="9a025-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="9a025-123">Boolescher Wert, der angibt, ob der Releaserückrufmechanismus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a025-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="9a025-124">Legen Sie den Wert auf **TRUE** fest, wenn Sie eine Rückrufschnittstelle bereitstellen möchten, die aufgerufen wird, wenn Puffer freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a025-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="9a025-125">Geben Sie den Rückruf an, indem Sie die [**CBaseAllocator::SetNotify-Methode**](cbaseallocator-setnotify.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a025-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a025-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a025-126">Requirements</span></span>



| <span data-ttu-id="9a025-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a025-127">Requirement</span></span> | <span data-ttu-id="9a025-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9a025-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a025-129">Header</span><span class="sxs-lookup"><span data-stu-id="9a025-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9a025-130"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9a025-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9a025-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a025-131">Library</span></span><br/> | <dl> <span data-ttu-id="9a025-132"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9a025-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a025-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a025-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a025-134">**CBaseAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a025-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




