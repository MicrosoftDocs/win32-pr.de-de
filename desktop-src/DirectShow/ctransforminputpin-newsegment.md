---
description: 'Die newsegment-Methode benachrichtigt die PIN, dass Medien Beispiele, die nach diesem-aufrufempfang empfangen werden, als Segment gruppiert werden. Diese Methode implementiert die IPin:: newsegment-Methode.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Ctransforminputpin. newsegment-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360908"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="29106-104">Ctransforminputpin. newsegment-Methode</span><span class="sxs-lookup"><span data-stu-id="29106-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="29106-105">Die- `NewSegment` Methode benachrichtigt die PIN, dass nach diesem-aufrufempfang empfangene Medien Beispiele als Segment gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="29106-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="29106-106">Diese Methode implementiert die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode.</span><span class="sxs-lookup"><span data-stu-id="29106-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29106-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="29106-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="29106-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="29106-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29106-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="29106-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="29106-110">Die Startzeit des Segments.</span><span class="sxs-lookup"><span data-stu-id="29106-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="29106-111">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="29106-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="29106-112">Die Endzeit des Segments.</span><span class="sxs-lookup"><span data-stu-id="29106-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="29106-113">*drate*</span><span class="sxs-lookup"><span data-stu-id="29106-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="29106-114">Rate des Segments.</span><span class="sxs-lookup"><span data-stu-id="29106-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29106-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29106-115">Return value</span></span>

<span data-ttu-id="29106-116">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29106-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29106-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29106-117">Remarks</span></span>

<span data-ttu-id="29106-118">Diese Methode überschreibt die [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="29106-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="29106-119">Die [**ctransformfilter:: newsegment**](ctransformfilter-newsegment.md) -Methode des Filters wird aufgerufen, um den Aufruf Downstream zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="29106-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="29106-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29106-120">Requirements</span></span>



| <span data-ttu-id="29106-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29106-121">Requirement</span></span> | <span data-ttu-id="29106-122">Wert</span><span class="sxs-lookup"><span data-stu-id="29106-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29106-123">Header</span><span class="sxs-lookup"><span data-stu-id="29106-123">Header</span></span><br/>  | <dl> <span data-ttu-id="29106-124"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29106-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="29106-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29106-125">Library</span></span><br/> | <dl> <span data-ttu-id="29106-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="29106-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




