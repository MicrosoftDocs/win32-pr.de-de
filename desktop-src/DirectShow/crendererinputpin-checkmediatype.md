---
description: 'Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert. Diese Methode überschreibt die cbasepin:: checkmediatype-Methode.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Crendererinputpin. checkmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372082"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="a5533-104">Crendererinputpin. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="a5533-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="a5533-105">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a5533-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="a5533-106">Diese Methode überschreibt die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a5533-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5533-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5533-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="a5533-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5533-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5533-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="a5533-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a5533-110">Zeiger auf ein Medientyp Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="a5533-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5533-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5533-111">Return value</span></span>

<span data-ttu-id="a5533-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5533-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5533-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5533-113">Requirements</span></span>



| <span data-ttu-id="a5533-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5533-114">Requirement</span></span> | <span data-ttu-id="a5533-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a5533-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5533-116">Header</span><span class="sxs-lookup"><span data-stu-id="a5533-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a5533-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5533-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5533-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5533-118">Library</span></span><br/> | <dl> <span data-ttu-id="a5533-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a5533-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5533-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5533-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5533-121">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a5533-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




