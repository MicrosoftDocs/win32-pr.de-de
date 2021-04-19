---
description: 'Die checktransform-Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist. Diese Methode überschreibt die ctransformfilter:: checktransform-Methode.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Ctransinplacefilter. checktransform-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367821"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="4964b-104">Ctransinplacefilter. checktransform-Methode</span><span class="sxs-lookup"><span data-stu-id="4964b-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="4964b-105">Die- `CheckTransform` Methode überprüft, ob ein Eingabe Medientyp mit einem Ausgabe Medientyp kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="4964b-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="4964b-106">Diese Methode überschreibt die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4964b-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4964b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4964b-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="4964b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4964b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4964b-109">*MTiN*</span><span class="sxs-lookup"><span data-stu-id="4964b-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="4964b-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Eingabetyp angibt.</span><span class="sxs-lookup"><span data-stu-id="4964b-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="4964b-111">*mtout*</span><span class="sxs-lookup"><span data-stu-id="4964b-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="4964b-112">Zeiger auf ein **cmediatype** -Objekt, das den Ausgabetyp angibt.</span><span class="sxs-lookup"><span data-stu-id="4964b-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4964b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4964b-113">Return value</span></span>

<span data-ttu-id="4964b-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4964b-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4964b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4964b-115">Remarks</span></span>

<span data-ttu-id="4964b-116">Der **ctransinplace** -Filter ruft niemals auf `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="4964b-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="4964b-117">Stattdessen verwenden alle Pin-Verbindungen [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) , um den Medientyp zu überprüfen. dabei wird davon ausgegangen, dass die Eingabe-und Ausgabetypen immer Stimmen.</span><span class="sxs-lookup"><span data-stu-id="4964b-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="4964b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4964b-118">Requirements</span></span>



| <span data-ttu-id="4964b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4964b-119">Requirement</span></span> | <span data-ttu-id="4964b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4964b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4964b-121">Header</span><span class="sxs-lookup"><span data-stu-id="4964b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4964b-122"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4964b-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4964b-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4964b-123">Library</span></span><br/> | <dl> <span data-ttu-id="4964b-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4964b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4964b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4964b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4964b-126">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4964b-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




