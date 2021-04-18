---
description: 'Die Methode umumpins listet die Pins für diesen Filter auf. Diese Methode implementiert die ibasefilter:: umumpins-Methode.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Cbasefilter. endumpins-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360928"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="0b805-104">Cbasefilter. endumpins-Methode</span><span class="sxs-lookup"><span data-stu-id="0b805-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="0b805-105">Die- `EnumPins` Methode listet die Pins für diesen Filter auf.</span><span class="sxs-lookup"><span data-stu-id="0b805-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="0b805-106">Diese Methode implementiert die [**ibasefilter:: umumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0b805-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b805-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b805-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="0b805-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b805-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b805-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="0b805-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="0b805-110">Adresse einer Variablen, die einen Zeiger auf die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="0b805-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b805-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b805-111">Return value</span></span>

<span data-ttu-id="0b805-112">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0b805-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="0b805-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0b805-113">Return code</span></span>                                                                                   | <span data-ttu-id="0b805-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b805-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="0b805-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b805-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b805-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="0b805-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="0b805-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b805-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b805-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="0b805-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="0b805-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0b805-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0b805-120">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="0b805-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b805-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b805-121">Remarks</span></span>

<span data-ttu-id="0b805-122">Diese Methode erstellt eine Instanz der [**cenumpins**](cenumpins.md) -Basisklasse und gibt einen Zeiger auf dieses Objekt vom Typ **ienumpins** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b805-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="0b805-123">Die **cenumpins** -Klasse ruft die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode des Filters auf, um die Pins für den Filter aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="0b805-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="0b805-124">Wenn diese Methode erfolgreich ausgeführt wird, hat die **ieinumpins** -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="0b805-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="0b805-125">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="0b805-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b805-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b805-126">Requirements</span></span>



| <span data-ttu-id="0b805-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b805-127">Requirement</span></span> | <span data-ttu-id="0b805-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0b805-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b805-129">Header</span><span class="sxs-lookup"><span data-stu-id="0b805-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0b805-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b805-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b805-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b805-131">Library</span></span><br/> | <dl> <span data-ttu-id="0b805-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0b805-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b805-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b805-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b805-134">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0b805-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




