---
description: Die agreemediatype-Methode sucht nach einem Medientyp, um eine PIN-Verbindung herzustellen.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Cbasepin. agreemediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370329"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="2bf90-103">Cbasepin. agreemediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="2bf90-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="2bf90-104">Die- `AgreeMediaType` Methode sucht nach einem Medientyp, um eine PIN-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bf90-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bf90-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2bf90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bf90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf90-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="2bf90-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="2bf90-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="2bf90-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2bf90-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="2bf90-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2bf90-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das einen Medientyp angibt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2bf90-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf90-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bf90-111">Return value</span></span>

<span data-ttu-id="2bf90-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2bf90-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2bf90-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="2bf90-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2bf90-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2bf90-114">Return code</span></span>                                                                                                  | <span data-ttu-id="2bf90-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bf90-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2bf90-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2bf90-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="2bf90-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2bf90-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="2bf90-118"><dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt></span><span class="sxs-lookup"><span data-stu-id="2bf90-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="2bf90-119">Es wurde kein zulässiger Medientyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="2bf90-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2bf90-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bf90-120">Remarks</span></span>

<span data-ttu-id="2bf90-121">Wenn der *PMT* -Parameter nicht **null** ist und einen Medientyp vollständig angibt, versucht diese Methode, mithilfe dieses Medientyps eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bf90-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="2bf90-122">Wenn der Versuch fehlschlägt, gibt die Methode einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2bf90-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="2bf90-123">Wenn der *PMT* -Parameter **null** ist oder einen partiellen Medientyp angibt, versucht diese Methode Medientypen in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="2bf90-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="2bf90-124">Die bevorzugten Medientypen der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="2bf90-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="2bf90-125">Die bevorzugten Medientypen dieser Pin.</span><span class="sxs-lookup"><span data-stu-id="2bf90-125">This pin's preferred media types.</span></span>

<span data-ttu-id="2bf90-126">Bevorzugte Medientypen werden mit der [**cbasepin:: enummediatypes**](cbasepin-enummediatypes.md) -Methode aufgezählt, und der resultierende Enumerator wird an die [**cbasepin:: trymediatypes**](cbasepin-trymediatypes.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="2bf90-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf90-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bf90-127">Requirements</span></span>



| <span data-ttu-id="2bf90-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bf90-128">Requirement</span></span> | <span data-ttu-id="2bf90-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2bf90-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf90-130">Header</span><span class="sxs-lookup"><span data-stu-id="2bf90-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2bf90-131"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf90-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2bf90-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2bf90-132">Library</span></span><br/> | <dl> <span data-ttu-id="2bf90-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf90-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf90-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bf90-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf90-135">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2bf90-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




