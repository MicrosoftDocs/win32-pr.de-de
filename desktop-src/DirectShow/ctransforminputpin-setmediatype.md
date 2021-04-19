---
description: Die setmediatype-Methode legt den Medientyp für die Verbindung fest.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Ctransforminputpin. setmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358792"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="fde9e-103">Ctransforminputpin. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="fde9e-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="fde9e-104">Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="fde9e-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fde9e-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="fde9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fde9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde9e-107">*UV*</span><span class="sxs-lookup"><span data-stu-id="fde9e-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="fde9e-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="fde9e-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde9e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fde9e-109">Return value</span></span>

<span data-ttu-id="fde9e-110">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fde9e-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde9e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fde9e-111">Remarks</span></span>

<span data-ttu-id="fde9e-112">Diese Methode überschreibt die [**cbasepin:: setmediatype**](cbasepin-setmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fde9e-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="fde9e-113">Die [**ctransformfilter:: setmediatype**](ctransformfilter-setmediatype.md) -Methode des Filters wird aufgerufen, um den Filter zu informieren.</span><span class="sxs-lookup"><span data-stu-id="fde9e-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="fde9e-114">Die PIN muss überprüfen, ob der Medientyp zulässig ist, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fde9e-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde9e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fde9e-115">Requirements</span></span>



| <span data-ttu-id="fde9e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fde9e-116">Requirement</span></span> | <span data-ttu-id="fde9e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fde9e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde9e-118">Header</span><span class="sxs-lookup"><span data-stu-id="fde9e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fde9e-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fde9e-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fde9e-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fde9e-120">Library</span></span><br/> | <dl> <span data-ttu-id="fde9e-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fde9e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




