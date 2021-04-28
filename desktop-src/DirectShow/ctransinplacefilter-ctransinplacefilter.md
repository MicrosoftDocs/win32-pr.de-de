---
description: 'CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor : Konstruktormethode.'
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084778"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="da5a0-103">CTransInPlaceFilter.CTransInPlaceFilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="da5a0-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="da5a0-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="da5a0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da5a0-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="da5a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da5a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5a0-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="da5a0-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="da5a0-108">Eine Zeichenfolge, die den Debugnamen des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="da5a0-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="da5a0-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="da5a0-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="da5a0-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="da5a0-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="da5a0-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="da5a0-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="da5a0-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="da5a0-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="da5a0-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="da5a0-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da5a0-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="da5a0-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="da5a0-115">Klassenbezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="da5a0-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="da5a0-116">*Phr*</span><span class="sxs-lookup"><span data-stu-id="da5a0-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="da5a0-117">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="da5a0-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="da5a0-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="da5a0-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="da5a0-119">Boolescher Wert, der angibt, ob der Filter die Eingabedaten ändert.</span><span class="sxs-lookup"><span data-stu-id="da5a0-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="da5a0-120">True **gibt an,** dass der Filter die Daten ändert.</span><span class="sxs-lookup"><span data-stu-id="da5a0-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="da5a0-121">Andernfalls übergibt der Filter die Daten unverändert nachgelagert.</span><span class="sxs-lookup"><span data-stu-id="da5a0-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da5a0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da5a0-122">Requirements</span></span>



| <span data-ttu-id="da5a0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da5a0-123">Requirement</span></span> | <span data-ttu-id="da5a0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="da5a0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da5a0-125">Header</span><span class="sxs-lookup"><span data-stu-id="da5a0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="da5a0-126"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="da5a0-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da5a0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da5a0-127">Library</span></span><br/> | <dl> <span data-ttu-id="da5a0-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="da5a0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5a0-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da5a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5a0-130">**CTransInPlaceFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="da5a0-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




