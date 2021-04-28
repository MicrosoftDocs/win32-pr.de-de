---
description: 'CBasePin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: CBasePin.EnumMediaTypes-Methode (Amfilter.h)
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
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099388"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="84f57-104">CBasePin.EnumMediaTypes-Methode</span><span class="sxs-lookup"><span data-stu-id="84f57-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="84f57-105">Die `EnumMediaTypes` -Methode aufzählt die bevorzugten Medientypen des Pins.</span><span class="sxs-lookup"><span data-stu-id="84f57-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="84f57-106">Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)</span><span class="sxs-lookup"><span data-stu-id="84f57-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f57-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f57-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="84f57-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="84f57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f57-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="84f57-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="84f57-110">Adresse einer Variablen, die einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="84f57-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f57-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84f57-111">Return value</span></span>

<span data-ttu-id="84f57-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="84f57-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="84f57-113">Mögliche Werte sind die werte in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="84f57-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="84f57-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="84f57-114">Return code</span></span>                                                                                   | <span data-ttu-id="84f57-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84f57-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="84f57-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="84f57-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="84f57-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="84f57-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="84f57-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="84f57-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="84f57-119">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="84f57-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="84f57-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="84f57-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="84f57-121"> NULL-Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="84f57-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84f57-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84f57-122">Remarks</span></span>

<span data-ttu-id="84f57-123">Eingabepins sind nicht erforderlich, um bevorzugte Typen aufzählen zu können.</span><span class="sxs-lookup"><span data-stu-id="84f57-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="84f57-124">Ausgabepins müssen mindestens einen bevorzugten Typ aufzählen.</span><span class="sxs-lookup"><span data-stu-id="84f57-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="84f57-125">Andernfalls könnten beide Stecknadeln keinen bevorzugten Typ haben, was eine Verbindung unmöglich macht.</span><span class="sxs-lookup"><span data-stu-id="84f57-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="84f57-126">Die **IEnumMediaTypes-Schnittstelle** funktioniert wie ein COM-Standardenumerator.</span><span class="sxs-lookup"><span data-stu-id="84f57-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="84f57-127">Weitere Informationen finden Sie unter [Aufzählen von Objekten in einem Filterdiagramm.](enumerating-objects-in-a-filter-graph.md)</span><span class="sxs-lookup"><span data-stu-id="84f57-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="84f57-128">Wenn die Methode erfolgreich ist, verfügt die **IEnumMediaTypes-Schnittstelle** über eine ausstehende Verweisanzahl.</span><span class="sxs-lookup"><span data-stu-id="84f57-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="84f57-129">Stellen Sie sicher, dass Sie sie veröffentlichen, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="84f57-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="84f57-130">Die [**CEnumMediaTypes-Basisklasse**](cenummediatypes.md) implementiert **IEnumMediaTypes.**</span><span class="sxs-lookup"><span data-stu-id="84f57-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="84f57-131">Sie ruft die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) des Pins auf, um die Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="84f57-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f57-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84f57-132">Requirements</span></span>



| <span data-ttu-id="84f57-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84f57-133">Requirement</span></span> | <span data-ttu-id="84f57-134">Wert</span><span class="sxs-lookup"><span data-stu-id="84f57-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f57-135">Header</span><span class="sxs-lookup"><span data-stu-id="84f57-135">Header</span></span><br/>  | <dl> <span data-ttu-id="84f57-136"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="84f57-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="84f57-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84f57-137">Library</span></span><br/> | <dl> <span data-ttu-id="84f57-138"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="84f57-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f57-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="84f57-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f57-140">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="84f57-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




