---
description: CBaseOutputPin.CBaseOutputPin-Konstruktor – Konstruktormethode.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: CBaseOutputPin.CBaseOutputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9901591be32d431ebe53a2098456446a0126d26b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099568"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="27824-103">CBaseOutputPin.CBaseOutputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="27824-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="27824-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="27824-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27824-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27824-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="27824-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="27824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27824-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="27824-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="27824-108">Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="27824-108">String containing the debug name of the object.</span></span> <span data-ttu-id="27824-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="27824-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="27824-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="27824-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="27824-111">Zeiger auf den Filter, der diese Stecknadel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="27824-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="27824-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="27824-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="27824-113">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27824-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="27824-114">Dies kann derselbe kritische Abschnitt wie die Filtersperre [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md)sein.</span><span class="sxs-lookup"><span data-stu-id="27824-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="27824-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="27824-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="27824-116">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="27824-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="27824-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="27824-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="27824-118">Breitzeichenzeichenfolge, die den Pinnamen enthält (wird auch als Stecknadelbezeichner verwendet).</span><span class="sxs-lookup"><span data-stu-id="27824-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27824-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27824-119">Remarks</span></span>

<span data-ttu-id="27824-120">Alle Parameter werden direkt an den [**CBasePin-Konstruktor**](cbasepin.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="27824-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="27824-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27824-121">Requirements</span></span>



| <span data-ttu-id="27824-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27824-122">Requirement</span></span> | <span data-ttu-id="27824-123">Wert</span><span class="sxs-lookup"><span data-stu-id="27824-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27824-124">Header</span><span class="sxs-lookup"><span data-stu-id="27824-124">Header</span></span><br/>  | <dl> <span data-ttu-id="27824-125"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="27824-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="27824-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27824-126">Library</span></span><br/> | <dl> <span data-ttu-id="27824-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="27824-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27824-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27824-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27824-129">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="27824-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




