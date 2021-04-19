---
description: Konstruktormethode.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Crenderedinputpin. crenderedinputpin-Konstruktor (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366743"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="7f281-103">Crenderedinputpin. crenderedinputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="7f281-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="7f281-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="7f281-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f281-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f281-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="7f281-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f281-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="7f281-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="7f281-108">Zeichenfolge, die den debugnamen des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="7f281-108">String containing the debug name of the object.</span></span> <span data-ttu-id="7f281-109">Weitere Informationen finden Sie unter [**cbaseobject-Klasse**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="7f281-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f281-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="7f281-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="7f281-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="7f281-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="7f281-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="7f281-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="7f281-113">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f281-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="7f281-114">Dabei kann es sich um denselben kritischen Abschnitt handeln wie die Filter Sperre, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="7f281-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f281-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="7f281-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7f281-116">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="7f281-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="7f281-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="7f281-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7f281-118">Breit Zeichen-Zeichenfolge, die den Pin-Namen (auch als PIN-Bezeichner verwendet) enthält.</span><span class="sxs-lookup"><span data-stu-id="7f281-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f281-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f281-119">Requirements</span></span>



| <span data-ttu-id="7f281-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f281-120">Requirement</span></span> | <span data-ttu-id="7f281-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7f281-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f281-122">Header</span><span class="sxs-lookup"><span data-stu-id="7f281-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7f281-123"><dt>Amextra. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f281-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f281-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f281-124">Library</span></span><br/> | <dl> <span data-ttu-id="7f281-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f281-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f281-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f281-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f281-127">**Crenderedinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f281-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




