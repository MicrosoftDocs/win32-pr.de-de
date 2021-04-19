---
description: 'Die Run-Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird. Diese Methode überschreibt die cbasepin:: Run-Methode.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Crenderedinputpin. Run-Methode (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354208"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="b5557-104">Crenderedinputpin. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="b5557-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="b5557-105">Die- `Run` Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5557-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="b5557-106">Diese Methode überschreibt die [**cbasepin:: Run**](cbasepin-run.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b5557-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5557-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5557-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="b5557-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5557-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5557-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="b5557-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b5557-110">Die Startzeit, die an die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode des Filters übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5557-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5557-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5557-111">Return value</span></span>

<span data-ttu-id="b5557-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b5557-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5557-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5557-113">Requirements</span></span>



| <span data-ttu-id="b5557-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5557-114">Requirement</span></span> | <span data-ttu-id="b5557-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b5557-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5557-116">Header</span><span class="sxs-lookup"><span data-stu-id="b5557-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b5557-117"><dt>Amextra. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5557-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5557-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5557-118">Library</span></span><br/> | <dl> <span data-ttu-id="b5557-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b5557-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5557-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5557-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5557-121">**Crenderedinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b5557-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




