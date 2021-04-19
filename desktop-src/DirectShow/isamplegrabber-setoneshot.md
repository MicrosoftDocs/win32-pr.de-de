---
description: Die Methode "-Methode" gibt an, ob der Sample Grabber-Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Isamplegrabber:: setoneshot-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360419"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="beafe-103">Isamplegrabber:: setoneshot-Methode</span><span class="sxs-lookup"><span data-stu-id="beafe-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="beafe-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="beafe-104">\[Deprecated.</span></span> <span data-ttu-id="beafe-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="beafe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="beafe-106">Die **Methode "** -Methode" gibt an, ob der [**Sample Grabber**](sample-grabber-filter.md) -Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="beafe-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="beafe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="beafe-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="beafe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="beafe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beafe-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="beafe-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="beafe-110">Ein boolescher Wert, der angibt, ob der Sample-Grabber Filter nach dem Empfang eines Beispiels angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="beafe-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="beafe-111">Wert</span><span class="sxs-lookup"><span data-stu-id="beafe-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="beafe-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="beafe-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="beafe-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="beafe-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="beafe-114">Der Beispiel Grabber wird nach dem ersten Beispiel angehalten.</span><span class="sxs-lookup"><span data-stu-id="beafe-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="beafe-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="beafe-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="beafe-116">Nach dem ersten Beispiel verarbeitet der Beispiel Grabber weiterhin Beispiele.</span><span class="sxs-lookup"><span data-stu-id="beafe-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="beafe-117">Dies ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="beafe-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beafe-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="beafe-118">Return value</span></span>

<span data-ttu-id="beafe-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="beafe-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="beafe-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="beafe-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="beafe-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beafe-121">Remarks</span></span>

<span data-ttu-id="beafe-122">Verwenden Sie diese Methode, um ein einzelnes Beispiel aus dem Datenstrom zu erhalten, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="beafe-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="beafe-123">Nennen **Sie** "\*" mit dem Wert " **true**".</span><span class="sxs-lookup"><span data-stu-id="beafe-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="beafe-124">Optional können Sie die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle verwenden, um eine Position im Stream zu suchen.</span><span class="sxs-lookup"><span data-stu-id="beafe-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="beafe-125">Nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , um das Filter Diagramm auszuführen.</span><span class="sxs-lookup"><span data-stu-id="beafe-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="beafe-126">Nennen Sie [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) , um zu warten, bis das Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="beafe-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="beafe-127">Rufen Sie alternativ [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) auf, um Diagramm Ereignisse abzurufen, bis Sie das Ereignis " [**EC \_ Complete**](ec-complete.md) " erhalten.</span><span class="sxs-lookup"><span data-stu-id="beafe-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="beafe-128">Nachdem die Stichprobenentnahme angehalten wurde, befindet sich das Filter Diagramm weiterhin in einem laufenden Zustand.</span><span class="sxs-lookup"><span data-stu-id="beafe-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="beafe-129">Sie können das Diagramm suchen oder anhalten, um ein weiteres Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="beafe-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="beafe-130">Eine frühere Version der Dokumentation hat besagt, dass das Filter Diagramm beendet wird, nachdem das Beispiel empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="beafe-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="beafe-131">Das ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="beafe-131">That is not accurate.</span></span> <span data-ttu-id="beafe-132">Der Stream wird beendet, der Graph verbleibt jedoch im Zustand "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="beafe-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="beafe-133">Der Beispiel-Grabber implementiert den One-Shot-Modus durch Aufrufen von [**IPin:: EndOfStream für den downstreamfilter**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) und das Zurückgeben von " \_ false" aus der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.</span><span class="sxs-lookup"><span data-stu-id="beafe-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="beafe-134">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="beafe-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="beafe-135">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="beafe-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="beafe-136">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="beafe-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="beafe-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beafe-137">Requirements</span></span>



| <span data-ttu-id="beafe-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beafe-138">Requirement</span></span> | <span data-ttu-id="beafe-139">Wert</span><span class="sxs-lookup"><span data-stu-id="beafe-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beafe-140">Header</span><span class="sxs-lookup"><span data-stu-id="beafe-140">Header</span></span><br/>  | <dl> <span data-ttu-id="beafe-141"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="beafe-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="beafe-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="beafe-142">Library</span></span><br/> | <dl> <span data-ttu-id="beafe-143"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="beafe-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beafe-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beafe-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beafe-145">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="beafe-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="beafe-146">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="beafe-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




