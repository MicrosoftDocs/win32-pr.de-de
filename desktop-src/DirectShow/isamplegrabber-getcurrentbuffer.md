---
description: Die getcurrentbuffer-Methode ruft eine Kopie des Puffers ab, der mit dem letzten Beispiel verknüpft ist.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Isamplegrabber:: getcurrentbuffer-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369162"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="a7d17-103">Isamplegrabber:: getcurrentbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="a7d17-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="a7d17-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a7d17-104">\[Deprecated.</span></span> <span data-ttu-id="a7d17-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a7d17-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a7d17-106">Die **getcurrentbuffer** -Methode ruft eine Kopie des Puffers ab, der mit dem letzten Beispiel verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a7d17-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7d17-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a7d17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7d17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d17-109">*pbuffersize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a7d17-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d17-110">Ein Zeiger auf die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="a7d17-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="a7d17-111">Wenn *pbuffer* den Wert **null** hat, erhält dieser Parameter die erforderliche Puffergröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a7d17-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="a7d17-112">Wenn *pbuffer* nicht **null** ist, legen Sie diesen Parameter auf die Größe des Puffers (in Bytes) fest.</span><span class="sxs-lookup"><span data-stu-id="a7d17-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="a7d17-113">Bei der Ausgabe empfängt der-Parameter die Anzahl der Bytes, die in den Puffer kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a7d17-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="a7d17-114">Dieser Wert kann kleiner sein als die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="a7d17-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a7d17-115">*pbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7d17-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d17-116">Zeiger auf ein Bytearray mit der Größe *pbuffersize* oder **null**.</span><span class="sxs-lookup"><span data-stu-id="a7d17-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="a7d17-117">Wenn dieser Parameter nicht **null** ist, wird der aktuelle Puffer in das Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="a7d17-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="a7d17-118">Wenn dieser Parameter **null** ist, erhält der *pbuffersize* -Parameter die erforderliche Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="a7d17-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d17-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7d17-119">Return value</span></span>

<span data-ttu-id="a7d17-120">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d17-120">Returns one of the following values.</span></span>



| <span data-ttu-id="a7d17-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a7d17-121">Return code</span></span>                                                                                           | <span data-ttu-id="a7d17-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7d17-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7d17-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="a7d17-124">Die Stichproben werden nicht gepuffert.</span><span class="sxs-lookup"><span data-stu-id="a7d17-124">Samples are not being buffered.</span></span> <span data-ttu-id="a7d17-125">Aufrufen von [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="a7d17-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="a7d17-126"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="a7d17-127">Der angegebene Puffer ist nicht groß genug.</span><span class="sxs-lookup"><span data-stu-id="a7d17-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="a7d17-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="a7d17-129">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="a7d17-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="a7d17-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a7d17-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a7d17-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="a7d17-132"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a7d17-133">Der Filter ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="a7d17-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="a7d17-134"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="a7d17-135">Der Filter hat noch keine Stichproben empfangen.</span><span class="sxs-lookup"><span data-stu-id="a7d17-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="a7d17-136">Um ein Beispiel zu liefern, führen Sie das Diagramm aus oder halten es an.</span><span class="sxs-lookup"><span data-stu-id="a7d17-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="a7d17-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d17-137">Remarks</span></span>

<span data-ttu-id="a7d17-138">Um die Pufferung zu aktivieren, wenden Sie [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **true** an.</span><span class="sxs-lookup"><span data-stu-id="a7d17-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="a7d17-139">Ruft diese Methode zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="a7d17-139">Call this method twice.</span></span> <span data-ttu-id="a7d17-140">Legen Sie für den ersten-Befehl *pbuffer* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a7d17-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="a7d17-141">Die Größe des Puffers wird in " *pbuffersize*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7d17-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="a7d17-142">Weisen Sie dann ein Array zu, und nennen Sie die Methode erneut.</span><span class="sxs-lookup"><span data-stu-id="a7d17-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="a7d17-143">Übergeben Sie im zweiten-Befehl die Größe des Arrays in *pbuffersize*, und übergeben Sie die Adresse des Arrays in *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="a7d17-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="a7d17-144">Wenn das Array nicht groß genug ist, gibt die Methode "E \_ outo fmemory" zurück.</span><span class="sxs-lookup"><span data-stu-id="a7d17-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="a7d17-145">Der *pbuffer* -Parameter wird als **Long** -Zeiger eingegeben, aber der Inhalt des Puffers hängt vom Format der Daten ab.</span><span class="sxs-lookup"><span data-stu-id="a7d17-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="a7d17-146">Wenden Sie [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md) an, um den Medientyp des Formats zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7d17-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="a7d17-147">Diese Methode wird nicht aufgerufen, während das Filter Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7d17-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="a7d17-148">Während der Ausführung des Filter Diagramms wird der Inhalt des Puffers beim Empfang eines neuen Beispiels überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7d17-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="a7d17-149">Die beste Möglichkeit, diese Methode zu verwenden, ist die Verwendung des "One-Shot"-Modus, der das Diagramm nach dem Empfang des ersten Beispiels stoppt.</span><span class="sxs-lookup"><span data-stu-id="a7d17-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="a7d17-150">Um den One-Shot-Modus festzulegen, wenden Sie [**isamplegrabber:: setoneshot**](isamplegrabber-setoneshot.md)an.</span><span class="sxs-lookup"><span data-stu-id="a7d17-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="a7d17-151">Der Filter puffert keine vorab Beispiele oder Beispiele, in denen das **dwstreamid** -Element der " [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) "-Struktur etwas anderes als "am-Stream-Medien" ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a7d17-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="a7d17-152">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a7d17-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a7d17-153">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a7d17-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a7d17-154">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7d17-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7d17-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d17-155">Requirements</span></span>



| <span data-ttu-id="a7d17-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7d17-156">Requirement</span></span> | <span data-ttu-id="a7d17-157">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d17-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d17-158">Header</span><span class="sxs-lookup"><span data-stu-id="a7d17-158">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d17-159"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a7d17-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7d17-160">Library</span></span><br/> | <dl> <span data-ttu-id="a7d17-161"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a7d17-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d17-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7d17-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d17-163">Verwenden der Beispiel-Grabber</span><span class="sxs-lookup"><span data-stu-id="a7d17-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="a7d17-164">**Isamplegrabber-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a7d17-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




