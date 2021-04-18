---
description: Die passnotify-Methode übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Cbasonputpin. passnotify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358019"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="33f68-103">Cbasonputpin. passnotify-Methode</span><span class="sxs-lookup"><span data-stu-id="33f68-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="33f68-104">Die `PassNotify` -Methode übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.</span><span class="sxs-lookup"><span data-stu-id="33f68-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33f68-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="33f68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33f68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f68-107">*Q1*</span><span class="sxs-lookup"><span data-stu-id="33f68-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="33f68-108">[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="33f68-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f68-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33f68-109">Return value</span></span>

<span data-ttu-id="33f68-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="33f68-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33f68-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="33f68-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="33f68-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="33f68-112">Return code</span></span>                                                                                       | <span data-ttu-id="33f68-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33f68-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="33f68-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33f68-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="33f68-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="33f68-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="33f68-116"><dt>**VFW \_ E \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="33f68-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="33f68-117">Es konnte kein Objekt gefunden werden, um die Nachricht zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="33f68-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33f68-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33f68-118">Remarks</span></span>

<span data-ttu-id="33f68-119">Ruft diese Methode auf, wenn der Filter keine Qualitäts Steuerungs Meldungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="33f68-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="33f68-120">Diese Methode übergibt die Nachricht in der angegebenen Reihenfolge an eines der folgenden Objekte:</span><span class="sxs-lookup"><span data-stu-id="33f68-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="33f68-121">Ein externer Qualitäts Steuerungs Manager, wenn die [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="33f68-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="33f68-122">Die upstreamausgabepin.</span><span class="sxs-lookup"><span data-stu-id="33f68-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f68-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33f68-123">Requirements</span></span>



| <span data-ttu-id="33f68-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33f68-124">Requirement</span></span> | <span data-ttu-id="33f68-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33f68-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f68-126">Header</span><span class="sxs-lookup"><span data-stu-id="33f68-126">Header</span></span><br/>  | <dl> <span data-ttu-id="33f68-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33f68-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33f68-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33f68-128">Library</span></span><br/> | <dl> <span data-ttu-id="33f68-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33f68-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f68-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33f68-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f68-131">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33f68-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="33f68-132">Qualitäts Steuerungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="33f68-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




