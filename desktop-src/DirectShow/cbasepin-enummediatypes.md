---
description: 'Die enummediatypes-Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die IPin:: enummediatypes-Methode.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Cbasepin. enummediatypes-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372427"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="a4d6f-104">Cbasepin. enummediatypes-Methode</span><span class="sxs-lookup"><span data-stu-id="a4d6f-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="a4d6f-105">Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="a4d6f-106">Diese Methode implementiert die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d6f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d6f-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a4d6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d6f-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="a4d6f-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="a4d6f-110">Adresse einer Variablen, die einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d6f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4d6f-111">Return value</span></span>

<span data-ttu-id="a4d6f-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a4d6f-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="a4d6f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4d6f-114">Return code</span></span>                                                                                   | <span data-ttu-id="a4d6f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4d6f-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a4d6f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4d6f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4d6f-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="a4d6f-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a4d6f-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4d6f-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="a4d6f-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a4d6f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a4d6f-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4d6f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4d6f-122">Remarks</span></span>

<span data-ttu-id="a4d6f-123">Eingabe Pins sind nicht erforderlich, um bevorzugte Typen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="a4d6f-124">Ausgabe Pins müssen mindestens einen bevorzugten Typ auflisten.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="a4d6f-125">Andernfalls könnten beide Pins einen bevorzugten Typ haben und eine Verbindung unmöglich machen.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="a4d6f-126">Die **ienummediatypes** -Schnittstelle funktioniert wie ein Standard-com-Enumerator.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="a4d6f-127">Weitere Informationen finden Sie unter Auflisten von [Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a4d6f-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="a4d6f-128">Wenn die Methode erfolgreich ausgeführt wird, hat die **ienummediatypes** -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="a4d6f-129">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="a4d6f-130">Die [**cenummediatypes**](cenummediatypes.md) -Basisklasse implementiert **ienummediatypes**.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="a4d6f-131">Sie ruft die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode der PIN auf, um die Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="a4d6f-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d6f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4d6f-132">Requirements</span></span>



| <span data-ttu-id="a4d6f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4d6f-133">Requirement</span></span> | <span data-ttu-id="a4d6f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a4d6f-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d6f-135">Header</span><span class="sxs-lookup"><span data-stu-id="a4d6f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a4d6f-136"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4d6f-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4d6f-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4d6f-137">Library</span></span><br/> | <dl> <span data-ttu-id="a4d6f-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a4d6f-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d6f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4d6f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d6f-140">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a4d6f-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




