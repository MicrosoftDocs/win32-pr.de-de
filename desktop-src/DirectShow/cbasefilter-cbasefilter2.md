---
description: CBaseFilter.CBaseFilter(const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID) -Konstruktormethode.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: CBaseFilter.CBaseFilter(const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) -Konstruktor (Amfilter.h)
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
ms.openlocfilehash: b621bdb3f6a15ae950959a65eba8841bde399b81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099828"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="1468d-103">CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, \* CCritSec, REFCLSID) -Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1468d-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="1468d-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="1468d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1468d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1468d-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="1468d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1468d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1468d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1468d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1468d-108">Zeiger auf eine Zeichenfolge, die den Namen des Filters enthält, zu Debugzwecken.</span><span class="sxs-lookup"><span data-stu-id="1468d-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="1468d-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="1468d-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1468d-110">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="1468d-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="1468d-111">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="1468d-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="1468d-112">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="1468d-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1468d-113">*Plock*</span><span class="sxs-lookup"><span data-stu-id="1468d-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1468d-114">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1468d-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="1468d-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="1468d-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="1468d-116">Klassenbezeichner (CLSID) des Filters.</span><span class="sxs-lookup"><span data-stu-id="1468d-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1468d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1468d-117">Remarks</span></span>

<span data-ttu-id="1468d-118">Für das kritische Abschnittsobjekt würden Sie in der Regel einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1468d-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="1468d-119">Leiten Sie eine Klasse ab, die sowohl **CBaseFilter** als auch **CCritSec** erbt.</span><span class="sxs-lookup"><span data-stu-id="1468d-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="1468d-120">Übergeben Sie für *pLock* den `this` Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1468d-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="1468d-121">Leiten Sie eine Klasse ab, die **CBaseFilter** erbt und eine **CCritSec-Membervariable** enthält.</span><span class="sxs-lookup"><span data-stu-id="1468d-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="1468d-122">Übergeben Sie für *pLock* die Adresse dieser Variablen.</span><span class="sxs-lookup"><span data-stu-id="1468d-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1468d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1468d-123">Requirements</span></span>



| <span data-ttu-id="1468d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1468d-124">Requirement</span></span> | <span data-ttu-id="1468d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1468d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1468d-126">Header</span><span class="sxs-lookup"><span data-stu-id="1468d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1468d-127"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1468d-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1468d-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1468d-128">Library</span></span><br/> | <dl> <span data-ttu-id="1468d-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1468d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1468d-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1468d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1468d-131">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1468d-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




