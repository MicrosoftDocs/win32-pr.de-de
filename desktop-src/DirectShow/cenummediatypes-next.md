---
description: 'Die Next-Methode ruft eine angegebene Anzahl von Medientypen ab. Diese Methode implementiert die ienummediatypes:: Next-Methode.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Cenum mediatypes. Next-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361568"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="62048-104">Cenum mediatypes. Next-Methode</span><span class="sxs-lookup"><span data-stu-id="62048-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="62048-105">Die- `Next` Methode ruft eine angegebene Anzahl von Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="62048-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="62048-106">Diese Methode implementiert die [**ienummediatypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) -Methode.</span><span class="sxs-lookup"><span data-stu-id="62048-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62048-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62048-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="62048-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62048-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62048-109">*cmediatypes*</span><span class="sxs-lookup"><span data-stu-id="62048-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="62048-110">Anzahl der abzurufenden Medientypen.</span><span class="sxs-lookup"><span data-stu-id="62048-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="62048-111">*ppmediatypes*</span><span class="sxs-lookup"><span data-stu-id="62048-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="62048-112">Array von Zeigern auf die [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Strukturen der Größe von *cpins*.</span><span class="sxs-lookup"><span data-stu-id="62048-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="62048-113">*pcfetch*</span><span class="sxs-lookup"><span data-stu-id="62048-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="62048-114">Ein Zeiger auf eine Variable, die die Anzahl der Medientypen empfängt, die von der Methode zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="62048-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="62048-115">Kann **null** sein, wenn *cmediatypes* den Wert 1 hat.</span><span class="sxs-lookup"><span data-stu-id="62048-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62048-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62048-116">Return value</span></span>

<span data-ttu-id="62048-117">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="62048-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="62048-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="62048-118">Return code</span></span>                                                                                                | <span data-ttu-id="62048-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62048-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62048-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="62048-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="62048-121">Es wurden nicht so viele Medientypen wie angefordert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="62048-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="62048-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="62048-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="62048-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="62048-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="62048-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="62048-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="62048-125">Ungültiges Argument.</span><span class="sxs-lookup"><span data-stu-id="62048-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="62048-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="62048-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="62048-127">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="62048-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="62048-128"><dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt></span><span class="sxs-lookup"><span data-stu-id="62048-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="62048-129">Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.</span><span class="sxs-lookup"><span data-stu-id="62048-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62048-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62048-130">Remarks</span></span>

<span data-ttu-id="62048-131">Wenn die Methode erfolgreich ausgeführt wird, enthält das von *ppmediatypes* angegebene Array Zeiger \_ auf \_ Medientyp Strukturen.</span><span class="sxs-lookup"><span data-stu-id="62048-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="62048-132">Die Anzahl der Strukturen ist gleich *\* pcfetch*.</span><span class="sxs-lookup"><span data-stu-id="62048-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="62048-133">Geben Sie jeden Medientyp frei, indem Sie die Funktion [**deletemediatype**](deletemediatype.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="62048-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="62048-134">Diese Methode ruft die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode der PIN auf, um die Medientypen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="62048-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="62048-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62048-135">Requirements</span></span>



| <span data-ttu-id="62048-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62048-136">Requirement</span></span> | <span data-ttu-id="62048-137">Wert</span><span class="sxs-lookup"><span data-stu-id="62048-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62048-138">Header</span><span class="sxs-lookup"><span data-stu-id="62048-138">Header</span></span><br/>  | <dl> <span data-ttu-id="62048-139"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62048-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="62048-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62048-140">Library</span></span><br/> | <dl> <span data-ttu-id="62048-141">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="62048-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62048-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62048-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62048-143">**Cenum mediatypes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="62048-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




