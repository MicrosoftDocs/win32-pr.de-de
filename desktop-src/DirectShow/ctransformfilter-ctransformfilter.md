---
description: 'CTransformFilter.CTransformFilter-Konstruktor : Konstruktormethode.'
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: CTransformFilter.CTransformFilter-Konstruktor (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098718"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="c06bc-103">CTransformFilter.CTransformFilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="c06bc-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="c06bc-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c06bc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c06bc-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="c06bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c06bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06bc-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="c06bc-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c06bc-108">Zeichenfolge, die den Debugnamen des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="c06bc-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="c06bc-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="c06bc-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="c06bc-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c06bc-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="c06bc-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="c06bc-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="c06bc-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c06bc-113">Legen Sie andernfalls diesen Parameter auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="c06bc-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c06bc-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="c06bc-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="c06bc-115">Klassenbezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="c06bc-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c06bc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c06bc-116">Remarks</span></span>

<span data-ttu-id="c06bc-117">Der Konstruktor erstellt keine Pins des Filters.</span><span class="sxs-lookup"><span data-stu-id="c06bc-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="c06bc-118">Dies geschieht beim ersten Aufruf der [**GetPin-Methode.**](ctransformfilter-getpin.md)</span><span class="sxs-lookup"><span data-stu-id="c06bc-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="c06bc-119">Der Konstruktor initialisiert die Membervariablen [**m \_ pInput**](ctransformfilter-m-pinput.md) und [**m \_ pOutput**](ctransformfilter-m-poutput.md) mit **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c06bc-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06bc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c06bc-120">Requirements</span></span>



| <span data-ttu-id="c06bc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c06bc-121">Requirement</span></span> | <span data-ttu-id="c06bc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c06bc-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06bc-123">Header</span><span class="sxs-lookup"><span data-stu-id="c06bc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c06bc-124"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c06bc-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c06bc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c06bc-125">Library</span></span><br/> | <dl> <span data-ttu-id="c06bc-126"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c06bc-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06bc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c06bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06bc-128">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c06bc-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




