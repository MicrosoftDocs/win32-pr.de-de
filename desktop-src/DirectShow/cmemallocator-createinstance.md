---
description: Die Methode "kreateinstance" erstellt eine neue Instanz der cmemzuordcator-Klasse.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Cmemzuzucator. kreatzustance-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368405"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="aef8f-103">Cmemzuzucator. kreatzustance-Methode</span><span class="sxs-lookup"><span data-stu-id="aef8f-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="aef8f-104">Die- `CreateInstance` Methode erstellt eine neue Instanz der **cmemzuordcator** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="aef8f-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aef8f-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="aef8f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aef8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef8f-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="aef8f-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="aef8f-108">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="aef8f-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="aef8f-109">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="aef8f-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="aef8f-110">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="aef8f-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aef8f-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="aef8f-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="aef8f-112">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="aef8f-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aef8f-113">Return value</span></span>

<span data-ttu-id="aef8f-114">Gibt einen Zeiger auf ein neues **cmemzuordcator** -Objekt zurück, das als **cunknown** -Objekt typisiert ist.</span><span class="sxs-lookup"><span data-stu-id="aef8f-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef8f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aef8f-115">Requirements</span></span>



| <span data-ttu-id="aef8f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aef8f-116">Requirement</span></span> | <span data-ttu-id="aef8f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aef8f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef8f-118">Header</span><span class="sxs-lookup"><span data-stu-id="aef8f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aef8f-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aef8f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aef8f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aef8f-120">Library</span></span><br/> | <dl> <span data-ttu-id="aef8f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aef8f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef8f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aef8f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef8f-123">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aef8f-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




