---
description: 'Die Methode "beenden" beendet das-Objekt. Diese Methode implementiert die imediafilter:: stopmethode.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Cbasemediafilter. stoppt-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359244"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="5097f-104">Cbasemediafilter. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="5097f-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="5097f-105">Die- `Stop` Methode beendet das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5097f-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="5097f-106">Diese Methode implementiert die [**imediafilter:: stopmethode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="5097f-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5097f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5097f-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="5097f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5097f-108">Parameters</span></span>

<span data-ttu-id="5097f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5097f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5097f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5097f-110">Return value</span></span>

<span data-ttu-id="5097f-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5097f-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5097f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5097f-112">Remarks</span></span>

<span data-ttu-id="5097f-113">In der Basisklasse legt diese Methode die " [**cbasemediafilter:: m \_ State**](cbasemediafilter-m-state.md) Member"-Variable auf "beendet" fest, bewirkt \_ aber nichts anderes.</span><span class="sxs-lookup"><span data-stu-id="5097f-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="5097f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5097f-114">Requirements</span></span>



| <span data-ttu-id="5097f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5097f-115">Requirement</span></span> | <span data-ttu-id="5097f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5097f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5097f-117">Header</span><span class="sxs-lookup"><span data-stu-id="5097f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5097f-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5097f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5097f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5097f-119">Library</span></span><br/> | <dl> <span data-ttu-id="5097f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5097f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5097f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5097f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5097f-122">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5097f-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




