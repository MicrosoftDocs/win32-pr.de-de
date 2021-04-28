---
description: CRenderedInputPin.CRenderedInputPin-Konstruktor – Konstruktormethode.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: CRenderedInputPin.CRenderedInputPin-Konstruktor (Amextra.h)
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
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085398"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="1a61e-103">CRenderedInputPin.CRenderedInputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="1a61e-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="1a61e-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="1a61e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a61e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a61e-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="1a61e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a61e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a61e-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="1a61e-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="1a61e-108">Eine Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="1a61e-108">String containing the debug name of the object.</span></span> <span data-ttu-id="1a61e-109">Weitere Informationen finden Sie unter [**CBaseObject-Klasse**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1a61e-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a61e-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="1a61e-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="1a61e-111">Zeiger auf den Filter, der diesen Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="1a61e-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="1a61e-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="1a61e-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1a61e-113">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a61e-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="1a61e-114">Dies kann derselbe kritische Abschnitt wie die Filtersperre [**CBaseFilter::m \_ pLock sein.**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="1a61e-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a61e-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1a61e-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1a61e-116">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="1a61e-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="1a61e-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="1a61e-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1a61e-118">Breitzeichenfolge mit dem Pinnamen (wird auch als Pinbezeichner verwendet).</span><span class="sxs-lookup"><span data-stu-id="1a61e-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a61e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a61e-119">Requirements</span></span>



| <span data-ttu-id="1a61e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a61e-120">Requirement</span></span> | <span data-ttu-id="1a61e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1a61e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a61e-122">Header</span><span class="sxs-lookup"><span data-stu-id="1a61e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1a61e-123"><dt>Amextra.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a61e-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a61e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a61e-124">Library</span></span><br/> | <dl> <span data-ttu-id="1a61e-125"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a61e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a61e-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a61e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a61e-127">**CRenderedInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a61e-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




