---
description: Hält das-Objekt an. Implementiert die imediafilter::P ause-Methode.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Cbasemediafilter. Pause-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360302"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="eb436-104">Cbasemediafilter. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="eb436-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="eb436-105">Hält das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eb436-105">Pauses the object.</span></span> <span data-ttu-id="eb436-106">Implementiert die [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) -Methode.</span><span class="sxs-lookup"><span data-stu-id="eb436-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb436-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb436-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="eb436-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb436-108">Parameters</span></span>

<span data-ttu-id="eb436-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="eb436-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb436-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb436-110">Return value</span></span>

<span data-ttu-id="eb436-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="eb436-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb436-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb436-112">Remarks</span></span>

<span data-ttu-id="eb436-113">In der Basisklasse legt diese Methode die " [**cbasemediafilter:: m \_ State**](cbasemediafilter-m-state.md) Member"-Variable auf "angehalten" fest, bewirkt \_ aber nichts anderes.</span><span class="sxs-lookup"><span data-stu-id="eb436-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb436-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb436-114">Requirements</span></span>



| <span data-ttu-id="eb436-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb436-115">Requirement</span></span> | <span data-ttu-id="eb436-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eb436-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb436-117">Header</span><span class="sxs-lookup"><span data-stu-id="eb436-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eb436-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb436-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb436-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb436-119">Library</span></span><br/> | <dl> <span data-ttu-id="eb436-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb436-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb436-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb436-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb436-122">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb436-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




