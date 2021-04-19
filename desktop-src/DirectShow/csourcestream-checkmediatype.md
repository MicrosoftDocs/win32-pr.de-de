---
description: 'Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. Diese Methode implementiert die rein virtuelle cbasepin:: checkmediatype-Methode.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Csourcestream. checkmediatype-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355924"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="a0b6e-104">Csourcestream. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="a0b6e-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="a0b6e-105">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="a0b6e-106">Diese Methode implementiert die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b6e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b6e-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="a0b6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b6e-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="a0b6e-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="a0b6e-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b6e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0b6e-111">Return value</span></span>

<span data-ttu-id="a0b6e-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a0b6e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a0b6e-113">Return code</span></span>                                                                            | <span data-ttu-id="a0b6e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0b6e-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a0b6e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b6e-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a0b6e-116">Diese PIN unterstützt diesen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="a0b6e-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b6e-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a0b6e-118">Dieser Medientyp wird von der PIN nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0b6e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0b6e-119">Remarks</span></span>

<span data-ttu-id="a0b6e-120">Standardmäßig unterstützt die PIN einen einzelnen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="a0b6e-121">Diese Methode ruft den unterstützten Typ durch Aufrufen der Einzel Parameter Version der [**csourcestream:: getmediatype**](csourcestream-getmediatype.md) -Methode ab und vergleicht sie mit dem vorgeschlagenen Typ.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="a0b6e-122">Wenn Ihre PIN mehr als einen Medientyp unterstützt, überschreiben Sie diese Methode.</span><span class="sxs-lookup"><span data-stu-id="a0b6e-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b6e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0b6e-123">Requirements</span></span>



| <span data-ttu-id="a0b6e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0b6e-124">Requirement</span></span> | <span data-ttu-id="a0b6e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a0b6e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b6e-126">Header</span><span class="sxs-lookup"><span data-stu-id="a0b6e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a0b6e-127"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b6e-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a0b6e-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0b6e-128">Library</span></span><br/> | <dl> <span data-ttu-id="a0b6e-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b6e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b6e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0b6e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b6e-131">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a0b6e-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




