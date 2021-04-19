---
description: Die Pause-Methode hält den Filter an. Diese Methode implementiert die imediafilter::P ause-Methode.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Cbasefilter. Pause-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366865"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="1273f-104">Cbasefilter. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="1273f-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="1273f-105">Die `Pause` Methode hält den Filter an.</span><span class="sxs-lookup"><span data-stu-id="1273f-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="1273f-106">Diese Methode implementiert die [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1273f-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1273f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1273f-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="1273f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1273f-108">Parameters</span></span>

<span data-ttu-id="1273f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1273f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1273f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1273f-110">Return value</span></span>

<span data-ttu-id="1273f-111">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="1273f-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1273f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1273f-112">Remarks</span></span>

<span data-ttu-id="1273f-113">Diese Methode ruft die [**cbasepin:: Active**](cbasepin-active.md) -Methode für jeden verbundenen Pins des Filters auf.</span><span class="sxs-lookup"><span data-stu-id="1273f-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="1273f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1273f-114">Requirements</span></span>



| <span data-ttu-id="1273f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1273f-115">Requirement</span></span> | <span data-ttu-id="1273f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1273f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1273f-117">Header</span><span class="sxs-lookup"><span data-stu-id="1273f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1273f-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1273f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1273f-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1273f-119">Library</span></span><br/> | <dl> <span data-ttu-id="1273f-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1273f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1273f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1273f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1273f-122">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1273f-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




