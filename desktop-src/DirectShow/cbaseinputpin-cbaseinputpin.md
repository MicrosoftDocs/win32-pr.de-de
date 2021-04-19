---
description: Konstruktormethode.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Cbasinput PIN. cbasinput Pin-Konstruktor (amfilter. h)
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
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366847"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="02352-103">Cbasinput PIN. cbasinput Pin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="02352-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="02352-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="02352-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02352-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02352-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="02352-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02352-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="02352-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="02352-108">Zeichenfolge, die den debugnamen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="02352-108">String containing the debug name of the object.</span></span> <span data-ttu-id="02352-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="02352-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="02352-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="02352-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="02352-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="02352-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="02352-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="02352-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="02352-113">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="02352-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="02352-114">Dabei kann es sich um denselben kritischen Abschnitt handeln wie die Filter Sperre, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="02352-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="02352-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="02352-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="02352-116">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="02352-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="02352-117">*ppinname*</span><span class="sxs-lookup"><span data-stu-id="02352-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="02352-118">Breit Zeichen-Zeichenfolge, die den Pin-Namen (auch als PIN-Bezeichner verwendet) enthält.</span><span class="sxs-lookup"><span data-stu-id="02352-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02352-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02352-119">Remarks</span></span>

<span data-ttu-id="02352-120">Alle Parameter werden direkt an den [**cbasepin**](cbasepin-cbasepin.md) -Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="02352-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="02352-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02352-121">Requirements</span></span>



| <span data-ttu-id="02352-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02352-122">Requirement</span></span> | <span data-ttu-id="02352-123">Wert</span><span class="sxs-lookup"><span data-stu-id="02352-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02352-124">Header</span><span class="sxs-lookup"><span data-stu-id="02352-124">Header</span></span><br/>  | <dl> <span data-ttu-id="02352-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02352-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02352-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02352-126">Library</span></span><br/> | <dl> <span data-ttu-id="02352-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="02352-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02352-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02352-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02352-129">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="02352-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




