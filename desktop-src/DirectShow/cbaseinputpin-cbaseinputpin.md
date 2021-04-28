---
description: 'CBaseInputPin.CBaseInputPin-Konstruktor : Konstruktormethode.'
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: CBaseInputPin.CBaseInputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95a6dca29a9bdcaf978a54587035b34959d81719
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120048"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="b607d-103">CBaseInputPin.CBaseInputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="b607d-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="b607d-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="b607d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b607d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b607d-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="b607d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b607d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b607d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="b607d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="b607d-108">Eine Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="b607d-108">String containing the debug name of the object.</span></span> <span data-ttu-id="b607d-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="b607d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="b607d-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="b607d-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="b607d-111">Zeiger auf den Filter, der diesen Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="b607d-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="b607d-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="b607d-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="b607d-113">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b607d-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="b607d-114">Dies kann derselbe kritische Abschnitt wie die Filtersperre [**CBaseFilter::m \_ pLock sein.**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="b607d-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="b607d-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b607d-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b607d-116">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="b607d-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="b607d-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="b607d-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="b607d-118">Breitzeichenfolge mit dem Pinnamen (wird auch als Pinbezeichner verwendet).</span><span class="sxs-lookup"><span data-stu-id="b607d-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b607d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b607d-119">Remarks</span></span>

<span data-ttu-id="b607d-120">Alle Parameter werden direkt an den [**CBasePin-Konstruktor**](cbasepin-cbasepin.md) übergeben.</span><span class="sxs-lookup"><span data-stu-id="b607d-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b607d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b607d-121">Requirements</span></span>



| <span data-ttu-id="b607d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b607d-122">Requirement</span></span> | <span data-ttu-id="b607d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b607d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b607d-124">Header</span><span class="sxs-lookup"><span data-stu-id="b607d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b607d-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="b607d-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b607d-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b607d-126">Library</span></span><br/> | <dl> <span data-ttu-id="b607d-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b607d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b607d-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b607d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b607d-129">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b607d-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




