---
description: 'CBaseReferenceClock.CBaseReferenceClock-Konstruktor : Konstruktormethode.'
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: CBaseReferenceClock.CBaseReferenceClock-Konstruktor (Refclock.h)
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
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119938"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="f8292-103">CBaseReferenceClock.CBaseReferenceClock-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="f8292-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="f8292-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f8292-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8292-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8292-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="f8292-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8292-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f8292-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f8292-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="f8292-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="f8292-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f8292-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8292-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="f8292-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f8292-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8292-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f8292-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die IUnknown-Schnittstelle des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8292-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="f8292-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="f8292-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f8292-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="f8292-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f8292-115">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="f8292-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f8292-116">Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f8292-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="f8292-117">Legen Sie diesen Parameter nicht auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="f8292-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f8292-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="f8292-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="f8292-119">Zeiger auf ein [**WEBCAMSchedule-Objekt.**](camschedule.md)</span><span class="sxs-lookup"><span data-stu-id="f8292-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="f8292-120">Bei **NULL** erstellt diese Methode ein **neuesCAMSchedule-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="f8292-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8292-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8292-121">Requirements</span></span>



| <span data-ttu-id="f8292-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8292-122">Requirement</span></span> | <span data-ttu-id="f8292-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f8292-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8292-124">Header</span><span class="sxs-lookup"><span data-stu-id="f8292-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f8292-125"><dt>Refclock.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="f8292-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8292-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8292-126">Library</span></span><br/> | <dl> <span data-ttu-id="f8292-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f8292-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8292-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8292-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8292-129">**CBaseReferenceClock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8292-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




