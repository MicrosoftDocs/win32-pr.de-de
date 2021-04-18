---
description: Konstruktormethode.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Csourceseeking. csourceseeking-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371466"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="3cc2b-103">Csourceseeking. csourceseeking-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3cc2b-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="3cc2b-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cc2b-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="3cc2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cc2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc2b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3cc2b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc2b-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="3cc2b-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3cc2b-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cc2b-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="3cc2b-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc2b-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3cc2b-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3cc2b-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3cc2b-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="3cc2b-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc2b-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="3cc2b-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3cc2b-117">*Plock*</span><span class="sxs-lookup"><span data-stu-id="3cc2b-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc2b-118">Zeiger auf ein [**ccritsec**](ccritsec.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="3cc2b-119">Deklarieren Sie in der abgeleiteten Klasse eine **ccritsec** -Member-Variable, und verwenden Sie die Adresse des Parameters für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="3cc2b-120">Die- `CSourceSeeking` Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start-und Endzeit-, Dauer-und Wiedergabe Rate zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="3cc2b-121">Wenn Sie auf diese Variablen in der abgeleiteten Klasse zugreifen, behalten Sie diese Sperre bei.</span><span class="sxs-lookup"><span data-stu-id="3cc2b-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cc2b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cc2b-122">Requirements</span></span>



| <span data-ttu-id="3cc2b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cc2b-123">Requirement</span></span> | <span data-ttu-id="3cc2b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3cc2b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc2b-125">Header</span><span class="sxs-lookup"><span data-stu-id="3cc2b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3cc2b-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cc2b-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cc2b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3cc2b-127">Library</span></span><br/> | <dl> <span data-ttu-id="3cc2b-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3cc2b-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc2b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cc2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc2b-130">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3cc2b-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




