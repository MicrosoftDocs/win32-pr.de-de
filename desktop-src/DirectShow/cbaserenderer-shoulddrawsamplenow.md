---
description: Die Methode "schulddrawsamplenow" bestimmt, wie ein Beispiel für das Rendering geplant wird.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Cbasererderderer. schulddrawsamplenow-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352136"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="9a563-103">Cbasererderer. schulddrawsamplenow-Methode</span><span class="sxs-lookup"><span data-stu-id="9a563-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="9a563-104">Die- `ShouldDrawSampleNow` Methode bestimmt, wie ein Beispiel für das Rendering geplant wird.</span><span class="sxs-lookup"><span data-stu-id="9a563-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a563-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a563-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="9a563-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a563-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="9a563-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9a563-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="9a563-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9a563-109">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="9a563-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="9a563-110">Ein Zeiger auf eine Variable, die die Startzeit des Beispiels enthält.</span><span class="sxs-lookup"><span data-stu-id="9a563-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="9a563-111">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="9a563-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="9a563-112">Ein Zeiger auf eine Variable, die die Endzeit des Beispiels enthält.</span><span class="sxs-lookup"><span data-stu-id="9a563-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a563-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a563-113">Return value</span></span>

<span data-ttu-id="9a563-114">Gibt " \_ false" zurück.</span><span class="sxs-lookup"><span data-stu-id="9a563-114">Returns S\_FALSE.</span></span> <span data-ttu-id="9a563-115">Wenn die abgeleitete Klasse diese Methode überschreibt, geben Sie einen der in der folgenden Tabelle aufgeführten Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9a563-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="9a563-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a563-116">Return code</span></span>                                                                               | <span data-ttu-id="9a563-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a563-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a563-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a563-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9a563-119">Das Beispiel sollte sofort gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="9a563-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="9a563-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9a563-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="9a563-121">Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.</span><span class="sxs-lookup"><span data-stu-id="9a563-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="9a563-122"><dt>**Fehlercode**</dt></span><span class="sxs-lookup"><span data-stu-id="9a563-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="9a563-123">Führen Sie dieses Beispiel nicht aus.</span><span class="sxs-lookup"><span data-stu-id="9a563-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="9a563-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a563-124">Remarks</span></span>

<span data-ttu-id="9a563-125">Die [**cbaserdenderer:: getsampletimes**](cbaserenderer-getsampletimes.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9a563-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="9a563-126">Standardmäßig werden Stichproben immer basierend auf Ihren Zeitstempeln für das Rendering geplant.</span><span class="sxs-lookup"><span data-stu-id="9a563-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="9a563-127">Diese Methode kann von der abgeleiteten Klasse überschrieben werden. So implementieren Sie z. b. die Qualitätskontrolle.</span><span class="sxs-lookup"><span data-stu-id="9a563-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a563-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a563-128">Requirements</span></span>



| <span data-ttu-id="9a563-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a563-129">Requirement</span></span> | <span data-ttu-id="9a563-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9a563-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a563-131">Header</span><span class="sxs-lookup"><span data-stu-id="9a563-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9a563-132"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a563-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a563-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a563-133">Library</span></span><br/> | <dl> <span data-ttu-id="9a563-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9a563-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a563-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a563-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a563-136">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a563-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




