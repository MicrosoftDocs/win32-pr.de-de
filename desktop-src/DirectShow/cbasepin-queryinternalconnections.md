---
description: 'Die QueryInternalConnections-Methode ruft die Pins ab, die intern mit dieser Pin (innerhalb des Filters) verbunden sind. Diese Methode implementiert die IPin:: QueryInternalConnections-Methode.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Cbasepin. QueryInternalConnections-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356490"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="90710-104">Cbasepin. QueryInternalConnections-Methode</span><span class="sxs-lookup"><span data-stu-id="90710-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="90710-105">Die- `QueryInternalConnections` Methode ruft die Pins ab, die intern mit dieser Pin (innerhalb des Filters) verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="90710-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="90710-106">Diese Methode implementiert die [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) -Methode.</span><span class="sxs-lookup"><span data-stu-id="90710-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="90710-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="90710-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="90710-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90710-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90710-109">*Appin*</span><span class="sxs-lookup"><span data-stu-id="90710-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="90710-110">Adresse eines Arrays von [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeigern.</span><span class="sxs-lookup"><span data-stu-id="90710-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="90710-111">*npin*</span><span class="sxs-lookup"><span data-stu-id="90710-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="90710-112">Gibt bei Eingabe die Größe des Arrays an.</span><span class="sxs-lookup"><span data-stu-id="90710-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="90710-113">Wenn die Methode zurückgibt, wird der Wert auf die Anzahl der im Array zurückgegebenen Zeiger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90710-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90710-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90710-114">Return value</span></span>

<span data-ttu-id="90710-115">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="90710-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="90710-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="90710-116">Return code</span></span>                                                                               | <span data-ttu-id="90710-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90710-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="90710-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="90710-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="90710-119">Unzureichende Array Größe.</span><span class="sxs-lookup"><span data-stu-id="90710-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="90710-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90710-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="90710-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="90710-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="90710-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="90710-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="90710-123">Fehler.</span><span class="sxs-lookup"><span data-stu-id="90710-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="90710-124"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="90710-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="90710-125">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="90710-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="90710-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90710-126">Remarks</span></span>

<span data-ttu-id="90710-127">Bei manchen Filtern entsprechen Eingabe Pins bestimmten Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="90710-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="90710-128">Für jede Pin füllt diese Methode ein Array mit Zeigern auf die entsprechenden Pins.</span><span class="sxs-lookup"><span data-stu-id="90710-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="90710-129">Wenn jede Eingabe-PIN Daten für jede Ausgabe-PIN bereitstellt, wird E \_ notimpl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90710-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="90710-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90710-130">Requirements</span></span>



| <span data-ttu-id="90710-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90710-131">Requirement</span></span> | <span data-ttu-id="90710-132">Wert</span><span class="sxs-lookup"><span data-stu-id="90710-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90710-133">Header</span><span class="sxs-lookup"><span data-stu-id="90710-133">Header</span></span><br/>  | <dl> <span data-ttu-id="90710-134"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90710-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="90710-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90710-135">Library</span></span><br/> | <dl> <span data-ttu-id="90710-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="90710-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90710-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90710-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90710-138">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="90710-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




