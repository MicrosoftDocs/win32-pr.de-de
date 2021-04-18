---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Cbasefilter. findpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360927"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="1efbc-104">Cbasefilter. findpin-Methode</span><span class="sxs-lookup"><span data-stu-id="1efbc-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="1efbc-105">Die- `FindPin` Methode ruft die PIN mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="1efbc-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="1efbc-106">Diese Methode implementiert die [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1efbc-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efbc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1efbc-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="1efbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1efbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efbc-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="1efbc-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="1efbc-110">Zeiger auf eine Konstante, mit NULL endender Unicode-Zeichenfolge, die die PIN identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1efbc-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="1efbc-111">*pppin*</span><span class="sxs-lookup"><span data-stu-id="1efbc-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="1efbc-112">Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN empfängt.</span><span class="sxs-lookup"><span data-stu-id="1efbc-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efbc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1efbc-113">Return value</span></span>

<span data-ttu-id="1efbc-114">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="1efbc-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="1efbc-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1efbc-115">Return code</span></span>                                                                                       | <span data-ttu-id="1efbc-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1efbc-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1efbc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1efbc-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="1efbc-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1efbc-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1efbc-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1efbc-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="1efbc-120">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="1efbc-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="1efbc-121"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="1efbc-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="1efbc-122">Es konnte keine passende Pin gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1efbc-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1efbc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1efbc-123">Remarks</span></span>

<span data-ttu-id="1efbc-124">Diese Methode ruft die [**cbasepin:: Name**](cbasepin-name.md) -Methode auf, um den Namen jeder PIN mit der durch den *ID* -Parameter angegebenen Zeichenfolge zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="1efbc-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="1efbc-125">Wenn die Methode erfolgreich ausgeführt wird, hat die **IPin** -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="1efbc-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="1efbc-126">Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="1efbc-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="1efbc-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1efbc-127">Requirements</span></span>



| <span data-ttu-id="1efbc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1efbc-128">Requirement</span></span> | <span data-ttu-id="1efbc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1efbc-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efbc-130">Header</span><span class="sxs-lookup"><span data-stu-id="1efbc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1efbc-131"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1efbc-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1efbc-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1efbc-132">Library</span></span><br/> | <dl> <span data-ttu-id="1efbc-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1efbc-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1efbc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efbc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efbc-135">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1efbc-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




