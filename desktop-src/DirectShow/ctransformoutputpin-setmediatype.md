---
description: Die setmediatype-Methode legt den Medientyp für die Verbindung fest.
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Ctransformoutputpin. setmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45bd16f0c0e5ea9cd1e719518fab15180177fd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369263"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="43d40-103">Ctransformoutputpin. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="43d40-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="43d40-104">Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="43d40-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d40-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d40-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="43d40-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d40-107">*UV*</span><span class="sxs-lookup"><span data-stu-id="43d40-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="43d40-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="43d40-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d40-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43d40-109">Return value</span></span>

<span data-ttu-id="43d40-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43d40-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d40-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43d40-111">Remarks</span></span>

<span data-ttu-id="43d40-112">Diese Methode überschreibt die [**cbasepin:: setmediatype**](cbasepin-setmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="43d40-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="43d40-113">Die [**ctransformfilter:: setmediatype**](ctransformfilter-setmediatype.md) -Methode des Filters wird aufgerufen, um den Filter zu informieren.</span><span class="sxs-lookup"><span data-stu-id="43d40-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="43d40-114">Die PIN muss überprüfen, ob der Medientyp zulässig ist, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="43d40-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d40-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43d40-115">Requirements</span></span>



| <span data-ttu-id="43d40-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43d40-116">Requirement</span></span> | <span data-ttu-id="43d40-117">Wert</span><span class="sxs-lookup"><span data-stu-id="43d40-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d40-118">Header</span><span class="sxs-lookup"><span data-stu-id="43d40-118">Header</span></span><br/>  | <dl> <span data-ttu-id="43d40-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43d40-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43d40-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43d40-120">Library</span></span><br/> | <dl> <span data-ttu-id="43d40-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="43d40-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




