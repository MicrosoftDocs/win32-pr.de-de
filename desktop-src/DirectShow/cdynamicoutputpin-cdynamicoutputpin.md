---
description: Konstruktormethode.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Cdynamicoutputpin. cdynamicoutputpin-Konstruktor (amfilter. h)
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
ms.openlocfilehash: 7f45a2fee25796f39c7d8b358b1ac83e4a5b1daa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367202"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="466f6-103">Cdynamicoutputpin. cdynamicoutputpin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="466f6-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="466f6-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="466f6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="466f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="466f6-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="466f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="466f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="466f6-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="466f6-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="466f6-108">Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="466f6-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="466f6-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="466f6-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="466f6-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="466f6-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="466f6-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="466f6-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="466f6-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="466f6-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="466f6-113">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="466f6-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="466f6-114">Verwenden Sie den gleichen kritischen Abschnitt wie die Filter Sperre [ **cbasefilter:: m \_ Plock** .](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="466f6-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="466f6-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="466f6-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="466f6-116">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="466f6-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="466f6-117">Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK.</span><span class="sxs-lookup"><span data-stu-id="466f6-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="466f6-118">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="466f6-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="466f6-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="466f6-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="466f6-120">Zeiger auf eine breit Zeichen-Zeichenfolge, die den PIN-Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="466f6-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="466f6-121">Weitere Informationen finden Sie unter [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="466f6-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="466f6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="466f6-122">Requirements</span></span>



| <span data-ttu-id="466f6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="466f6-123">Requirement</span></span> | <span data-ttu-id="466f6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="466f6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="466f6-125">Header</span><span class="sxs-lookup"><span data-stu-id="466f6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="466f6-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="466f6-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="466f6-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="466f6-127">Library</span></span><br/> | <dl> <span data-ttu-id="466f6-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="466f6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="466f6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="466f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="466f6-130">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="466f6-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




