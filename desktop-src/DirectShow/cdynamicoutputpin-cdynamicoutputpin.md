---
description: CDynamicOutputPin.CDynamicOutputPin-Konstruktor – Konstruktormethode.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: CDynamicOutputPin.CDynamicOutputPin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099308"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="5c408-103">CDynamicOutputPin.CDynamicOutputPin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="5c408-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="5c408-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="5c408-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c408-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c408-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="5c408-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c408-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="5c408-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="5c408-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="5c408-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="5c408-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5c408-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c408-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="5c408-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="5c408-111">Zeiger auf den Filter, der diesen Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="5c408-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="5c408-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="5c408-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="5c408-113">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c408-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="5c408-114">Verwenden Sie den gleichen kritischen Abschnitt wie die Filtersperre [ **CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="5c408-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="5c408-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="5c408-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5c408-116">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="5c408-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="5c408-117">Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c408-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="5c408-118">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5c408-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="5c408-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="5c408-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5c408-120">Zeiger auf eine Breitzeichenzeichenfolge, die den Pinbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="5c408-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="5c408-121">Weitere Informationen finden Sie unter [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="5c408-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c408-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c408-122">Requirements</span></span>



| <span data-ttu-id="5c408-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c408-123">Requirement</span></span> | <span data-ttu-id="5c408-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5c408-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c408-125">Header</span><span class="sxs-lookup"><span data-stu-id="5c408-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5c408-126"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="5c408-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c408-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c408-127">Library</span></span><br/> | <dl> <span data-ttu-id="5c408-128"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5c408-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c408-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c408-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c408-130">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5c408-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




