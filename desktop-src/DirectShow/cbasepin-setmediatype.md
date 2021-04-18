---
description: Die setmediatype-Methode legt den Medientyp für die Verbindung fest.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Cbasepin. setmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371223"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="69573-103">Cbasepin. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="69573-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="69573-104">Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="69573-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69573-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69573-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="69573-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69573-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69573-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="69573-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="69573-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="69573-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69573-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69573-109">Return value</span></span>

<span data-ttu-id="69573-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="69573-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="69573-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69573-111">Remarks</span></span>

<span data-ttu-id="69573-112">Mit dieser Methode wird das Format für eine PIN-Verbindung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69573-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="69573-113">Vor dem Aufrufen dieser Methode ruft die PIN die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu bestimmen, ob der Medientyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="69573-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="69573-114">Daher wird davon ausgegangen, dass der *PMT* -Parameter ein akzeptabler Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="69573-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="69573-115">In der Basisklasse legt diese Methode die Member-Variable [**cbasepin:: m \_ MT**](cbasepin-m-mt.md) fest und gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="69573-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="69573-116">Eine abgeleitete Klasse kann diese Methode überschreiben, wenn Sie eine Benachrichtigung erfordert, wenn der Medientyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="69573-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="69573-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69573-117">Requirements</span></span>



| <span data-ttu-id="69573-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69573-118">Requirement</span></span> | <span data-ttu-id="69573-119">Wert</span><span class="sxs-lookup"><span data-stu-id="69573-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69573-120">Header</span><span class="sxs-lookup"><span data-stu-id="69573-120">Header</span></span><br/>  | <dl> <span data-ttu-id="69573-121"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69573-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69573-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69573-122">Library</span></span><br/> | <dl> <span data-ttu-id="69573-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="69573-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69573-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69573-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69573-125">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="69573-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




