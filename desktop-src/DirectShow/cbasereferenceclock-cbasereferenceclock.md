---
description: Konstruktormethode.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Cbasereferenceclock. cbasereferenceclock-Konstruktor (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373865"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="96c96-103">Cbasereferenceclock. cbasereferenceclock-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="96c96-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="96c96-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="96c96-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c96-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="96c96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96c96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c96-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="96c96-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="96c96-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="96c96-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="96c96-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="96c96-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c96-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="96c96-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="96c96-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="96c96-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="96c96-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die IUnknown-Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="96c96-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="96c96-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="96c96-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96c96-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="96c96-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="96c96-115">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="96c96-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="96c96-116">Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="96c96-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="96c96-117">Legen Sie diesen Parameter nicht auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="96c96-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96c96-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="96c96-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="96c96-119">Zeiger auf ein " [**camschedule**](camschedule.md) "-Objekt.</span><span class="sxs-lookup"><span data-stu-id="96c96-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="96c96-120">Wenn der Wert **null** ist, erstellt diese Methode ein neues " **camschedule** "-Objekt.</span><span class="sxs-lookup"><span data-stu-id="96c96-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96c96-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96c96-121">Requirements</span></span>



| <span data-ttu-id="96c96-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96c96-122">Requirement</span></span> | <span data-ttu-id="96c96-123">Wert</span><span class="sxs-lookup"><span data-stu-id="96c96-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c96-124">Header</span><span class="sxs-lookup"><span data-stu-id="96c96-124">Header</span></span><br/>  | <dl> <span data-ttu-id="96c96-125"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96c96-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="96c96-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96c96-126">Library</span></span><br/> | <dl> <span data-ttu-id="96c96-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="96c96-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c96-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96c96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c96-129">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="96c96-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




