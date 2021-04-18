---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Ctransformoutputpin. getmediatype-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365557"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="d9493-103">Ctransformoutputpin. getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="d9493-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="d9493-104">Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp nach Indexwert ab.</span><span class="sxs-lookup"><span data-stu-id="d9493-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9493-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9493-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d9493-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9493-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9493-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="d9493-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="d9493-108">NULL basierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="d9493-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="d9493-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="d9493-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d9493-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="d9493-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9493-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9493-111">Return value</span></span>

<span data-ttu-id="d9493-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d9493-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d9493-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9493-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d9493-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d9493-114">Return code</span></span>                                                                                            | <span data-ttu-id="d9493-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9493-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="d9493-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d9493-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="d9493-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d9493-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="d9493-118"><dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="d9493-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="d9493-119">Index außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="d9493-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9493-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9493-120">Remarks</span></span>

<span data-ttu-id="d9493-121">Diese Methode überschreibt die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d9493-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="d9493-122">Wenn die Eingabe-PIN des Filters nicht verbunden ist, gibt die Methode VFW \_ s \_ keine \_ weiteren \_ Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="d9493-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="d9493-123">Andernfalls wird die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode des Filters aufgerufen, um den Medientyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9493-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="d9493-124">Die **ctransformfilter:: getmediatype** -Methode ist rein virtuell. die von der abgeleitete Klasse des Filters muss Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d9493-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9493-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9493-125">Requirements</span></span>



| <span data-ttu-id="d9493-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9493-126">Requirement</span></span> | <span data-ttu-id="d9493-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d9493-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9493-128">Header</span><span class="sxs-lookup"><span data-stu-id="d9493-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d9493-129"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9493-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9493-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9493-130">Library</span></span><br/> | <dl> <span data-ttu-id="d9493-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d9493-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




