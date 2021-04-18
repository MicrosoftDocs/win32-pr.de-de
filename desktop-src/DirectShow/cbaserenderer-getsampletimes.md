---
description: Die getsampletimes-Methode ruft die Zeitstempel aus einem Beispiel ab.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Cbaserderderer. getsampletimes-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364857"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="a84e0-103">Cbaserderderer. getsampletimes-Methode</span><span class="sxs-lookup"><span data-stu-id="a84e0-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="a84e0-104">Die- `GetSampleTimes` Methode ruft die Zeitstempel aus einem Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="a84e0-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84e0-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="a84e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a84e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84e0-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="a84e0-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a84e0-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="a84e0-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a84e0-109">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="a84e0-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a84e0-110">Ein Zeiger auf eine Variable, die die Startzeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="a84e0-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="a84e0-111">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="a84e0-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a84e0-112">Ein Zeiger auf eine Variable, die die Endzeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="a84e0-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a84e0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a84e0-113">Return value</span></span>

<span data-ttu-id="a84e0-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a84e0-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a84e0-115">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a84e0-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a84e0-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a84e0-116">Return code</span></span>                                                                                                    | <span data-ttu-id="a84e0-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a84e0-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a84e0-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="a84e0-119">Das Beispiel sollte sofort gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="a84e0-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="a84e0-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="a84e0-121">Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.</span><span class="sxs-lookup"><span data-stu-id="a84e0-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="a84e0-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="a84e0-123">Führen Sie dieses Beispiel nicht aus.</span><span class="sxs-lookup"><span data-stu-id="a84e0-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="a84e0-124"><dt>**VFW \_ E \_ \_ Startzeit \_ nach \_ Ende**</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="a84e0-125">Ungültiger Zeitstempel: die Endzeit liegt vor der Startzeit.</span><span class="sxs-lookup"><span data-stu-id="a84e0-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="a84e0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a84e0-126">Remarks</span></span>

<span data-ttu-id="a84e0-127">Der Filter ruft diese Methode auf, um zu bestimmen, wie eine Stichprobe behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a84e0-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="a84e0-128">Wenn der Rückgabewert S \_ OK ist, rendert der Filter das Beispiel sofort.</span><span class="sxs-lookup"><span data-stu-id="a84e0-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="a84e0-129">Wenn der Rückgabewert S \_ false ist, plant der Filter das Rendering basierend auf den Zeitstempeln für das Rendering.</span><span class="sxs-lookup"><span data-stu-id="a84e0-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="a84e0-130">Wenn der Rückgabewert ein Fehlercode ist, lehnt der Filter das Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="a84e0-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="a84e0-131">Diese Methode gibt "S OK" zurück \_ , wenn das Beispiel keine Zeitstempel aufweist, oder wenn der Filter keine Referenzuhr hat.</span><span class="sxs-lookup"><span data-stu-id="a84e0-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="a84e0-132">Andernfalls wird der Wert der [**cbaserenderer:: denddrawsamplenow**](cbaserenderer-shoulddrawsamplenow.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a84e0-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="a84e0-133">In der Basisklasse gibt " **schulddrawsamplenow** " immer "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="a84e0-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="a84e0-134">Die abgeleitete Klasse kann dieses Verhalten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a84e0-134">The derived class can override this behavior.</span></span> <span data-ttu-id="a84e0-135">Wenn die abgeleitete Klasse z. b. die Verwaltung von Qualitäts Teuerung implementiert, gibt Sie möglicherweise zurück, wenn \_ ein Beispiel nicht gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a84e0-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="a84e0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a84e0-136">Requirements</span></span>



| <span data-ttu-id="a84e0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a84e0-137">Requirement</span></span> | <span data-ttu-id="a84e0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a84e0-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a84e0-139">Header</span><span class="sxs-lookup"><span data-stu-id="a84e0-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a84e0-140"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a84e0-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a84e0-141">Library</span></span><br/> | <dl> <span data-ttu-id="a84e0-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a84e0-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a84e0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a84e0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84e0-144">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a84e0-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




