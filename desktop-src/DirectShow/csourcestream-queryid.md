---
description: Die QueryId-Methode ruft einen Bezeichner für die PIN ab.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Csourcestream. QueryId-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373890"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="73107-103">Csourcestream. QueryId-Methode</span><span class="sxs-lookup"><span data-stu-id="73107-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="73107-104">Die- `QueryId` Methode ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="73107-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="73107-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73107-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="73107-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73107-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73107-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="73107-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="73107-108">Ein Zeiger auf eine Variable, die eine Zeichenfolge mit dem PIN-Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="73107-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73107-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73107-109">Return value</span></span>

<span data-ttu-id="73107-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73107-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="73107-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="73107-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="73107-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="73107-112">Return code</span></span>                                                                                       | <span data-ttu-id="73107-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73107-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="73107-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="73107-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="73107-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="73107-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="73107-116"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="73107-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="73107-117">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="73107-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="73107-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="73107-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="73107-119">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="73107-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="73107-120"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="73107-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="73107-121">Die PIN wurde im Filter nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="73107-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73107-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73107-122">Remarks</span></span>

<span data-ttu-id="73107-123">Diese Methode implementiert die [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="73107-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="73107-124">Um eine Bezeichnerzeichenfolge zu erstellen, ruft die PIN die [**CSource:: findpinnumber**](csource-findpinnumber.md) -Methode mit sich selbst als Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="73107-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="73107-125">Die **findpinnumber** -Methode gibt die von 0 (null) indizierte PIN-Nummer zurück.</span><span class="sxs-lookup"><span data-stu-id="73107-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="73107-126">`QueryId` erhöht den Rückgabewert um 1 und konvertiert das Ergebnis in eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="73107-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="73107-127">Beispielsweise wird die erste Pin "1". die zweite PIN wird zu "2". und so weiter.</span><span class="sxs-lookup"><span data-stu-id="73107-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="73107-128">Wenn diese Methode "VFW \_ E \_ nicht gefunden" zurückgibt \_ , gibt Sie an, dass das Array von Pins des Filters ungültig ist, was vermutlich durch einen Fehler im Filter verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="73107-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="73107-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73107-129">Requirements</span></span>



| <span data-ttu-id="73107-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73107-130">Requirement</span></span> | <span data-ttu-id="73107-131">Wert</span><span class="sxs-lookup"><span data-stu-id="73107-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73107-132">Header</span><span class="sxs-lookup"><span data-stu-id="73107-132">Header</span></span><br/>  | <dl> <span data-ttu-id="73107-133"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73107-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="73107-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73107-134">Library</span></span><br/> | <dl> <span data-ttu-id="73107-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="73107-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73107-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73107-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73107-137">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="73107-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




