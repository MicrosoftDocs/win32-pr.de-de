---
description: 'Beendet den Filter. Diese Methode implementiert die imediafilter:: stopmethode.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: Ctransformfilter. stoppt-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356017"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="0ddd9-104">Ctransformfilter. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="0ddd9-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="0ddd9-105">Beendet den Filter.</span><span class="sxs-lookup"><span data-stu-id="0ddd9-105">Stops the filter.</span></span> <span data-ttu-id="0ddd9-106">Diese Methode implementiert die [**imediafilter:: stopmethode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="0ddd9-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddd9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ddd9-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="0ddd9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ddd9-108">Parameters</span></span>

<span data-ttu-id="0ddd9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ddd9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ddd9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ddd9-110">Return value</span></span>

<span data-ttu-id="0ddd9-111">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ddd9-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ddd9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ddd9-112">Remarks</span></span>

<span data-ttu-id="0ddd9-113">Nachdem diese Methode beide Zuweisungen decommittet hat, ruft Sie die [**stopstreaming**](ctransformfilter-stopstreaming.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0ddd9-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="0ddd9-114">Die **stopstreaming** -Methode führt in der Basisklasse keine Aktion aus, die abgeleitete Klasse kann Sie jedoch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0ddd9-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddd9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ddd9-115">Requirements</span></span>



| <span data-ttu-id="0ddd9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ddd9-116">Requirement</span></span> | <span data-ttu-id="0ddd9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0ddd9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddd9-118">Header</span><span class="sxs-lookup"><span data-stu-id="0ddd9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0ddd9-119"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd9-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ddd9-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ddd9-120">Library</span></span><br/> | <dl> <span data-ttu-id="0ddd9-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0ddd9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddd9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ddd9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddd9-123">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0ddd9-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




