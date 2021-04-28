---
description: 'CSourceSeeking.CSourceSeeking-Konstruktor : Konstruktormethode.'
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: CSourceSeeking.CSourceSeeking-Konstruktor (Ctlutil.h)
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
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098818"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="1cf22-103">CSourceSeeking.CSourceSeeking-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1cf22-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="1cf22-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="1cf22-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cf22-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="1cf22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cf22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf22-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1cf22-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf22-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="1cf22-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="1cf22-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1cf22-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf22-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="1cf22-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf22-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="1cf22-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="1cf22-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="1cf22-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="1cf22-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="1cf22-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cf22-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1cf22-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf22-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="1cf22-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="1cf22-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1cf22-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1cf22-117">*Plock*</span><span class="sxs-lookup"><span data-stu-id="1cf22-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf22-118">Zeiger auf ein [**CCritSec-Objekt.**](ccritsec.md)</span><span class="sxs-lookup"><span data-stu-id="1cf22-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="1cf22-119">Deklarieren Sie in der abgeleiteten Klasse eine **CCritSec-Membervariable,** und verwenden Sie die Adresse für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="1cf22-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="1cf22-120">Die -Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start- und `CSourceSeeking` Stoppzeiten, die Dauer und die Wiedergaberate zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1cf22-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="1cf22-121">Halten Sie diese Sperre bei jedem Zugriff auf diese Variablen in Ihrer abgeleiteten Klasse bei.</span><span class="sxs-lookup"><span data-stu-id="1cf22-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cf22-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cf22-122">Requirements</span></span>



| <span data-ttu-id="1cf22-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cf22-123">Requirement</span></span> | <span data-ttu-id="1cf22-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1cf22-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf22-125">Header</span><span class="sxs-lookup"><span data-stu-id="1cf22-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1cf22-126"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cf22-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1cf22-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cf22-127">Library</span></span><br/> | <dl> <span data-ttu-id="1cf22-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1cf22-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf22-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1cf22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf22-130">**CSourceSeeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1cf22-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




