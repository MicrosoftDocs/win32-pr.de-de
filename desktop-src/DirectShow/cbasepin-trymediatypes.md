---
description: Bei einer Liste von Medientypen wird von der trymediatypes-Methode versucht, eine Verbindung mit einem dieser Typen abzuschließen.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Cbasepin. trymediatypes-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351294"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="e2284-103">Cbasepin. trymediatypes-Methode</span><span class="sxs-lookup"><span data-stu-id="e2284-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="e2284-104">Bei einer Liste von Medientypen versucht die- `TryMediaTypes` Methode, eine Verbindung mit einem dieser Typen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e2284-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2284-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2284-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e2284-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2284-107">*preceivepin*</span><span class="sxs-lookup"><span data-stu-id="e2284-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="e2284-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der empfangenden PIN.</span><span class="sxs-lookup"><span data-stu-id="e2284-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e2284-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e2284-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e2284-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das die möglichen Medientypen einschränkt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e2284-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e2284-111">*"-ID"*</span><span class="sxs-lookup"><span data-stu-id="e2284-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="e2284-112">Zeiger auf eine [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle, die verwendet wird, um die Liste der Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="e2284-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2284-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2284-113">Return value</span></span>

<span data-ttu-id="e2284-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2284-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e2284-115">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="e2284-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e2284-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e2284-116">Return code</span></span>                                                                                                  | <span data-ttu-id="e2284-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2284-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="e2284-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2284-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e2284-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e2284-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="e2284-120"><dt>**VFW \_ E \_ keine \_ akzeptablen \_ Typen**</dt></span><span class="sxs-lookup"><span data-stu-id="e2284-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="e2284-121">Es wurde kein akzeptabler Medientyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="e2284-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2284-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2284-122">Remarks</span></span>

<span data-ttu-id="e2284-123">Für jeden Medientyp, der von der **ienummediatypes** -Schnittstelle zurückgegeben wird, versucht diese Methode, eine Verbindung durch Aufrufen der [**cbasepin::-Verbindungs**](cbasepin-attemptconnection.md) Methode herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2284-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="e2284-124">Wenn der *PMT* -Parameter nicht **null** ist, überspringt die PIN Medientypen, die nicht diesem Typ entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e2284-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="e2284-125">Der *PMT* -Parameter kann einen partiellen Medientyp angeben.</span><span class="sxs-lookup"><span data-stu-id="e2284-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="e2284-126">Ein partieller Medientyp weist den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder das Format auf.</span><span class="sxs-lookup"><span data-stu-id="e2284-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="e2284-127">Der GUID- \_ NULL-Wert stimmt mit einem beliebigen Typ überein, ähnlich dem Wert "Platzhalter".</span><span class="sxs-lookup"><span data-stu-id="e2284-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2284-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2284-128">Requirements</span></span>



| <span data-ttu-id="e2284-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2284-129">Requirement</span></span> | <span data-ttu-id="e2284-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e2284-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2284-131">Header</span><span class="sxs-lookup"><span data-stu-id="e2284-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e2284-132"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2284-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2284-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2284-133">Library</span></span><br/> | <dl> <span data-ttu-id="e2284-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e2284-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2284-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2284-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2284-136">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e2284-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




