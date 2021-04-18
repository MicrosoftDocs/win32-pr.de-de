---
description: 'Die Next-Methode ruft eine angegebene Anzahl von Pins in der enumerationssequenz ab. Diese Methode implementiert die iumumpins:: Next-Methode.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Cenumpins. Next-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365663"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="a448c-104">Cenumpins. Next-Methode</span><span class="sxs-lookup"><span data-stu-id="a448c-104">CEnumPins.Next method</span></span>

<span data-ttu-id="a448c-105">Die Next-Methode ruft eine angegebene Anzahl von Pins in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="a448c-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="a448c-106">Diese Methode implementiert die [**iumumpins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a448c-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a448c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a448c-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="a448c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a448c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a448c-109">*cpins*</span><span class="sxs-lookup"><span data-stu-id="a448c-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="a448c-110">Anzahl der abzurufenden Pins.</span><span class="sxs-lookup"><span data-stu-id="a448c-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a448c-111">*pppins*</span><span class="sxs-lookup"><span data-stu-id="a448c-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="a448c-112">Ein Array von Größen- *cpins* , das mit [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeigern gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="a448c-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="a448c-113">*pcfetch*</span><span class="sxs-lookup"><span data-stu-id="a448c-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="a448c-114">Ein Zeiger auf eine Variable, die die Anzahl der abgerufenen Pins empfängt.</span><span class="sxs-lookup"><span data-stu-id="a448c-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="a448c-115">Kann **null** sein, wenn *cpins* den Wert 1 hat.</span><span class="sxs-lookup"><span data-stu-id="a448c-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a448c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a448c-116">Return value</span></span>

<span data-ttu-id="a448c-117">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a448c-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a448c-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a448c-118">Return code</span></span>                                                                                                | <span data-ttu-id="a448c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a448c-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a448c-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="a448c-121">Es wurden nicht so viele Pins wie angefordert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a448c-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a448c-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a448c-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a448c-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="a448c-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="a448c-125">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="a448c-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a448c-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="a448c-127">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="a448c-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a448c-128"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="a448c-129">Der Zustand des Filters wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="a448c-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a448c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a448c-130">Remarks</span></span>

<span data-ttu-id="a448c-131">Diese Methode ruft Zeiger auf die angegebene Anzahl von Pins ab, beginnend an der aktuellen Position in der Enumeration und platziert Sie im angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="a448c-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="a448c-132">Diese Methode ruft die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode des Filters auf, um die Pins abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a448c-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="a448c-133">Wenn die Methode erfolgreich ausgeführt wird, weisen die **IPin** -Zeiger alle ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="a448c-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="a448c-134">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="a448c-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a448c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a448c-135">Requirements</span></span>



| <span data-ttu-id="a448c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a448c-136">Requirement</span></span> | <span data-ttu-id="a448c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a448c-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a448c-138">Header</span><span class="sxs-lookup"><span data-stu-id="a448c-138">Header</span></span><br/>  | <dl> <span data-ttu-id="a448c-139"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a448c-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a448c-140">Library</span></span><br/> | <dl> <span data-ttu-id="a448c-141">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a448c-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a448c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a448c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a448c-143">**Cenumpins-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a448c-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




