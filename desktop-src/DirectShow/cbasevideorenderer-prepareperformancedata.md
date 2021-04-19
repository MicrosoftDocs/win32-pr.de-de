---
description: Die prepareperformancedata-Methode legt die m \_ trlate-und m \_ trframe-Werte des aktuellen Frames fest.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Cbasevideorenderer. prepareperformancedata-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369967"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="cfe47-103">Cbasevideorenderer. prepareperformancedata-Methode</span><span class="sxs-lookup"><span data-stu-id="cfe47-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="cfe47-104">Die `PreparePerformanceData` -Methode legt die **m \_ trlate** -und **m \_ trframe** -Werte des aktuellen Frames fest.</span><span class="sxs-lookup"><span data-stu-id="cfe47-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfe47-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="cfe47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfe47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe47-107">*trlate*</span><span class="sxs-lookup"><span data-stu-id="cfe47-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe47-108">Der Wert, der angibt, wie spät das Beispiel in Bezugszeit Einheiten über die Fälligkeits Zeit hinausging.</span><span class="sxs-lookup"><span data-stu-id="cfe47-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="cfe47-109">*trframe*</span><span class="sxs-lookup"><span data-stu-id="cfe47-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe47-110">Interframe-Zeit in Bezugszeit Einheiten.</span><span class="sxs-lookup"><span data-stu-id="cfe47-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe47-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfe47-111">Return value</span></span>

<span data-ttu-id="cfe47-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cfe47-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe47-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfe47-113">Remarks</span></span>

<span data-ttu-id="cfe47-114">Diese Member-Funktion **legt \_ m trlate** auf den Wert von *trlate* und **m \_ trframe** auf den Wert von *trframe* fest.</span><span class="sxs-lookup"><span data-stu-id="cfe47-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="cfe47-115">Wenn die Member-Funktion [**cbasevideorenderer:: recordframellichkeit**](cbasevideorenderer-recordframelateness.md) von [**cbasevideorenderer:: onrenderstart**](cbasevideorenderer-onrenderstart.md) oder [**cbasevideorenderer:: ondirectrender**](cbasevideorenderer-ondirectrender.md)aufgerufen wird, werden die Werte von **m \_ trlate** und **m \_ trframe** übergeben, um die Statistiken zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfe47-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="cfe47-116">`PreparePerformanceData` wird von [**cbasevideorenderer:: onwaitend**](cbasevideorenderer-onwaitend.md) aufgerufen, um diese Datenmember-Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cfe47-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe47-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfe47-117">Requirements</span></span>



| <span data-ttu-id="cfe47-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfe47-118">Requirement</span></span> | <span data-ttu-id="cfe47-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cfe47-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe47-120">Header</span><span class="sxs-lookup"><span data-stu-id="cfe47-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cfe47-121"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfe47-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cfe47-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfe47-122">Library</span></span><br/> | <dl> <span data-ttu-id="cfe47-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cfe47-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe47-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfe47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe47-125">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cfe47-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




