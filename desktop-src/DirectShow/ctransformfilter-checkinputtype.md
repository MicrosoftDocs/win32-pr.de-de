---
description: Die checkinputtype-Methode überprüft, ob ein angegebener Medientyp für die Eingabe zulässig ist.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Ctransformfilter. checkinputtype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357573"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="6de67-103">Ctransformfilter. checkinputtype-Methode</span><span class="sxs-lookup"><span data-stu-id="6de67-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="6de67-104">Die- `CheckInputType` Methode überprüft, ob ein angegebener Medientyp für die Eingabe zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6de67-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6de67-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6de67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6de67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de67-107">*MTiN*</span><span class="sxs-lookup"><span data-stu-id="6de67-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="6de67-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="6de67-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de67-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6de67-109">Return value</span></span>

<span data-ttu-id="6de67-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6de67-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6de67-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6de67-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6de67-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6de67-112">Return code</span></span>                                                                                                | <span data-ttu-id="6de67-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6de67-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="6de67-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6de67-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="6de67-115">Der Medientyp ist akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="6de67-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="6de67-116"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="6de67-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="6de67-117">Der Medientyp ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6de67-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6de67-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6de67-118">Remarks</span></span>

<span data-ttu-id="6de67-119">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6de67-119">The derived class must implement this method.</span></span> <span data-ttu-id="6de67-120">Gibt S \_ OK zurück, wenn das vorgeschlagene Eingabeformat zulässig ist, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6de67-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="6de67-121">Diese Methode muss nicht überprüfen, ob das Eingabeformat mit dem Ausgabeformat (sofern vorhanden) kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="6de67-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="6de67-122">Die Eingabe-PIN überprüft dies durch Aufrufen der [**checktransform**](ctransformfilter-checktransform.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6de67-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de67-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de67-123">Requirements</span></span>



| <span data-ttu-id="6de67-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de67-124">Requirement</span></span> | <span data-ttu-id="6de67-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6de67-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de67-126">Header</span><span class="sxs-lookup"><span data-stu-id="6de67-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6de67-127"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6de67-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6de67-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6de67-128">Library</span></span><br/> | <dl> <span data-ttu-id="6de67-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6de67-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de67-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6de67-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de67-131">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6de67-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




