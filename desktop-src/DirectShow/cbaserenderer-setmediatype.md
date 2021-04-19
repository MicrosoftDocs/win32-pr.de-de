---
description: Die setmediatype-Methode wird aufgerufen, wenn der Medientyp der PIN festgelegt ist.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Cbaserderderer. setmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370909"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="28be4-103">Cbaserderderer. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="28be4-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="28be4-104">Die `SetMediaType` -Methode wird aufgerufen, wenn der Medientyp der PIN festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="28be4-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="28be4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28be4-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="28be4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28be4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28be4-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="28be4-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="28be4-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="28be4-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28be4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28be4-109">Return value</span></span>

<span data-ttu-id="28be4-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="28be4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="28be4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28be4-111">Remarks</span></span>

<span data-ttu-id="28be4-112">Die Eingabe-PIN ruft diese Methode von ihrer eigenen [**crendererinputpin:: setmediatype**](crendererinputpin-setmediatype.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="28be4-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="28be4-113">Diese Methode führt in der Basisklasse keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="28be4-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="28be4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28be4-114">Requirements</span></span>



| <span data-ttu-id="28be4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28be4-115">Requirement</span></span> | <span data-ttu-id="28be4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="28be4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28be4-117">Header</span><span class="sxs-lookup"><span data-stu-id="28be4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="28be4-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28be4-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28be4-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28be4-119">Library</span></span><br/> | <dl> <span data-ttu-id="28be4-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="28be4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28be4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28be4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28be4-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="28be4-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




