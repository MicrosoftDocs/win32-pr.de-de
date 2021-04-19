---
description: Die checkmediatype-Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Cbaserderderer. checkmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351373"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="a394f-103">Cbaserderderer. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="a394f-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="a394f-104">Die- `CheckMediaType` Methode bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a394f-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a394f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a394f-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a394f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a394f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a394f-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="a394f-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a394f-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="a394f-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a394f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a394f-109">Return value</span></span>

<span data-ttu-id="a394f-110">Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a394f-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="a394f-111">Andernfalls gibt S \_ false oder einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="a394f-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a394f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a394f-112">Remarks</span></span>

<span data-ttu-id="a394f-113">Die Eingabe-PIN ruft diese Methode aus ihrer eigenen [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a394f-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="a394f-114">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a394f-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a394f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a394f-115">Requirements</span></span>



| <span data-ttu-id="a394f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a394f-116">Requirement</span></span> | <span data-ttu-id="a394f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a394f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a394f-118">Header</span><span class="sxs-lookup"><span data-stu-id="a394f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a394f-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a394f-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a394f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a394f-120">Library</span></span><br/> | <dl> <span data-ttu-id="a394f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a394f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a394f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a394f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a394f-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a394f-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




