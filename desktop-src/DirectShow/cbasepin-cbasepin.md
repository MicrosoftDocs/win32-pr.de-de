---
description: 'CBasePin.CBasePin-Konstruktor : Konstruktormethode.'
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: CBasePin.CBasePin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099428"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="81eef-103">CBasePin.CBasePin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="81eef-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="81eef-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="81eef-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81eef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81eef-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="81eef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81eef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81eef-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="81eef-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-108">Zeichenfolge, die den Debugnamen für das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="81eef-108">String containing the debug name for the object.</span></span> <span data-ttu-id="81eef-109">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="81eef-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="81eef-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="81eef-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-111">Zeiger auf den Filter, der diese Stecknadel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="81eef-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="81eef-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="81eef-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-113">Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81eef-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="81eef-114">Kann derselbe kritische Abschnitt wie die Filtersperre sein, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="81eef-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="81eef-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="81eef-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-116">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="81eef-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="81eef-117">Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81eef-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="81eef-118">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="81eef-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="81eef-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="81eef-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-120">Breitzeichenzeichenfolge, die den Namen der Stecknadel enthält.</span><span class="sxs-lookup"><span data-stu-id="81eef-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="81eef-121">Weitere Informationen finden Sie unter [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="81eef-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="81eef-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="81eef-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="81eef-123">Member der [**PIN \_ DIRECTION-Enumeration,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der die Richtung des Pins angibt.</span><span class="sxs-lookup"><span data-stu-id="81eef-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81eef-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81eef-124">Remarks</span></span>

<span data-ttu-id="81eef-125">Der von *pLock* angegebene kritische Abschnitt serialisiert den Zustand des Pins, einschließlich des Verbindungsstatus, der Auswahl der Zuweisung, des Medientyps und des Status von Leerungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="81eef-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="81eef-126">Verwenden Sie diesen kritischen Abschnitt nicht zum Serialisieren von Streamingvorgängen.</span><span class="sxs-lookup"><span data-stu-id="81eef-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="81eef-127">Weitere Informationen finden Sie unter [Datenfluss im Filterdiagramm](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="81eef-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="81eef-128">Ein Filter erstellt möglicherweise Pins in seiner Konstruktormethode, sodass der *pFilter-Zeiger* an diesem Punkt möglicherweise nicht auf ein gültiges Objekt verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="81eef-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="81eef-129">Speichern Sie den Zeiger, dereferenzieren Sie ihn jedoch nicht im Konstruktor des Pins.</span><span class="sxs-lookup"><span data-stu-id="81eef-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="81eef-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81eef-130">Requirements</span></span>



| <span data-ttu-id="81eef-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81eef-131">Requirement</span></span> | <span data-ttu-id="81eef-132">Wert</span><span class="sxs-lookup"><span data-stu-id="81eef-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81eef-133">Header</span><span class="sxs-lookup"><span data-stu-id="81eef-133">Header</span></span><br/>  | <dl> <span data-ttu-id="81eef-134"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="81eef-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81eef-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81eef-135">Library</span></span><br/> | <dl> <span data-ttu-id="81eef-136"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="81eef-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81eef-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81eef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81eef-138">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="81eef-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




