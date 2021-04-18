---
description: Konstruktormethode.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Cbasepin. cbasepin-Konstruktor (amfilter. h)
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372475"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="97132-103">Cbasepin. cbasepin-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="97132-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="97132-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="97132-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="97132-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97132-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="97132-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97132-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="97132-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-108">Zeichenfolge, die den debugnamen für das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="97132-108">String containing the debug name for the object.</span></span> <span data-ttu-id="97132-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="97132-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="97132-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="97132-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-111">Zeiger auf den Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="97132-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="97132-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="97132-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-113">Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="97132-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="97132-114">Kann derselbe kritische Abschnitt wie die Filter Sperre sein, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="97132-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="97132-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="97132-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-116">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="97132-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="97132-117">Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK.</span><span class="sxs-lookup"><span data-stu-id="97132-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="97132-118">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="97132-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="97132-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="97132-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-120">Zeichenfolge mit breit Zeichen, die den Namen der PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="97132-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="97132-121">Weitere Informationen finden Sie unter [**cbasepin:: querypininfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="97132-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="97132-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="97132-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="97132-123">Member der [**Pin- \_ Richtungs**](/windows/win32/api/strmif/ne-strmif-pin_direction) Enumeration, die die Richtung der PIN angibt.</span><span class="sxs-lookup"><span data-stu-id="97132-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97132-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97132-124">Remarks</span></span>

<span data-ttu-id="97132-125">Der von *Plock* angegebene kritische Abschnitt serialisiert den Zustand der PIN, einschließlich des Verbindungsstatus, der Auswahl der Zuweisung, des Medientyps und des Status von Leerungs Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="97132-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="97132-126">Verwenden Sie diesen kritischen Abschnitt nicht zum Serialisieren von Streamingvorgängen.</span><span class="sxs-lookup"><span data-stu-id="97132-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="97132-127">Weitere Informationen finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="97132-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="97132-128">Ein Filter kann Pins in seiner Konstruktormethode erstellen. daher verweist der *pFilter* -Zeiger an diesem Punkt möglicherweise nicht auf ein gültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="97132-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="97132-129">Speichern Sie den Zeiger, aber heben Sie ihn nicht im Konstruktor der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="97132-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="97132-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97132-130">Requirements</span></span>



| <span data-ttu-id="97132-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97132-131">Requirement</span></span> | <span data-ttu-id="97132-132">Wert</span><span class="sxs-lookup"><span data-stu-id="97132-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97132-133">Header</span><span class="sxs-lookup"><span data-stu-id="97132-133">Header</span></span><br/>  | <dl> <span data-ttu-id="97132-134"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97132-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97132-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97132-135">Library</span></span><br/> | <dl> <span data-ttu-id="97132-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="97132-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97132-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97132-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97132-138">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="97132-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




