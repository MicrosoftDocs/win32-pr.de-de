---
description: Die setmediatype-Methode wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Ctransformfilter. setmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361623"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="ffcf0-103">Ctransformfilter. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="ffcf0-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="ffcf0-104">Die `SetMediaType` -Methode wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ffcf0-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffcf0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffcf0-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ffcf0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffcf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffcf0-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="ffcf0-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="ffcf0-108">Member der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerierten Typs, der eine PIN für den Filter angibt (Eingabe oder Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="ffcf0-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="ffcf0-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="ffcf0-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ffcf0-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="ffcf0-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffcf0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffcf0-111">Return value</span></span>

<span data-ttu-id="ffcf0-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ffcf0-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffcf0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffcf0-113">Remarks</span></span>

<span data-ttu-id="ffcf0-114">Die [**ctransforminputpin:: setmediatype**](ctransforminputpin-setmediatype.md) -Methode und die [**ctransformoutputpin:: setmediatype**](ctransformoutputpin-setmediatype.md) -Methode aufrufen diese Methode, wenn der Medientyp einer PIN festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ffcf0-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="ffcf0-115">Diese Methode führt keine Aktion in der Basisklasse durch, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ffcf0-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffcf0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffcf0-116">Requirements</span></span>



| <span data-ttu-id="ffcf0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffcf0-117">Requirement</span></span> | <span data-ttu-id="ffcf0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ffcf0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcf0-119">Header</span><span class="sxs-lookup"><span data-stu-id="ffcf0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ffcf0-120"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffcf0-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ffcf0-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffcf0-121">Library</span></span><br/> | <dl> <span data-ttu-id="ffcf0-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ffcf0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffcf0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffcf0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffcf0-124">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ffcf0-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




