---
description: Konstruktormethode.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Cbaseoutputpin. cbaseoutputpin-Konstruktor (amfilter. h)
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
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371502"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="723e9-103">Cbaseoutputpin. cbaseoutputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="723e9-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="723e9-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="723e9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="723e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="723e9-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="723e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="723e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723e9-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="723e9-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="723e9-108">Zeichenfolge, die den debugnamen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="723e9-108">String containing the debug name of the object.</span></span> <span data-ttu-id="723e9-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="723e9-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="723e9-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="723e9-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="723e9-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="723e9-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="723e9-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="723e9-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="723e9-113">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="723e9-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="723e9-114">Dabei kann es sich um denselben kritischen Abschnitt handeln wie die Filter Sperre, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="723e9-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="723e9-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="723e9-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="723e9-116">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="723e9-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="723e9-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="723e9-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="723e9-118">Breit Zeichen-Zeichenfolge, die den Pin-Namen (auch als PIN-Bezeichner verwendet) enthält.</span><span class="sxs-lookup"><span data-stu-id="723e9-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="723e9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="723e9-119">Remarks</span></span>

<span data-ttu-id="723e9-120">Alle Parameter werden direkt an den [**cbasepin**](cbasepin.md) -Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="723e9-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="723e9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="723e9-121">Requirements</span></span>



| <span data-ttu-id="723e9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="723e9-122">Requirement</span></span> | <span data-ttu-id="723e9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="723e9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723e9-124">Header</span><span class="sxs-lookup"><span data-stu-id="723e9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="723e9-125"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="723e9-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="723e9-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="723e9-126">Library</span></span><br/> | <dl> <span data-ttu-id="723e9-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="723e9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723e9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="723e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723e9-129">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="723e9-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




