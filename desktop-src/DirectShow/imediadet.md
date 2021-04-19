---
description: Die imediadet-Schnittstelle ruft Informationen über eine Mediendatei ab, wie z. b. die Anzahl der Streams sowie den Medientyp, die Dauer und die Framerate der einzelnen Datenströme.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Imediadet-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369415"
---
# <a name="imediadet-interface"></a><span data-ttu-id="e1a42-103">Imediadet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e1a42-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="e1a42-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e1a42-104">\[Deprecated.</span></span> <span data-ttu-id="e1a42-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e1a42-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1a42-106">Die `IMediaDet` -Schnittstelle ruft Informationen zu einer Mediendatei ab, z. b. die Anzahl der Streams und den Medientyp, die Dauer und die Framerate der einzelnen Datenströme.</span><span class="sxs-lookup"><span data-stu-id="e1a42-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="e1a42-107">Sie enthält auch Methoden zum Abrufen einzelner Frames aus einem Videostream.</span><span class="sxs-lookup"><span data-stu-id="e1a42-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="e1a42-108">Das [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) macht diese Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1a42-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="e1a42-109">Führen Sie die folgenden Schritte aus, um Informationen zu einer Datei zu erhalten, die diese Schnittstelle verwendet:</span><span class="sxs-lookup"><span data-stu-id="e1a42-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="e1a42-110">Erstellen Sie eine Instanz des mediadet-Objekts durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e1a42-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="e1a42-111">Die Klassen-ID ist CLSID \_ mediadet.</span><span class="sxs-lookup"><span data-stu-id="e1a42-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="e1a42-112">Nennen Sie [**imediadet::p UT \_ filename**](imediadet-put-filename.md) , um den Namen der Quelldatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e1a42-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="e1a42-113">Rufen Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) auf, um die Anzahl der Ausgabedaten Ströme in der Quelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e1a42-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="e1a42-114">Nennen Sie [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md) , um einen bestimmten Stream anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e1a42-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="e1a42-115">Wenden Sie eine der folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="e1a42-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="e1a42-116">**Imediadet:: get \_ Framerate**</span><span class="sxs-lookup"><span data-stu-id="e1a42-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="e1a42-117">**Imediadet:: get \_ streamlength**</span><span class="sxs-lookup"><span data-stu-id="e1a42-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="e1a42-118">**Imediadet:: get \_ streammediatype**</span><span class="sxs-lookup"><span data-stu-id="e1a42-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="e1a42-119">**Imediadet:: get \_ Streamtype**</span><span class="sxs-lookup"><span data-stu-id="e1a42-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="e1a42-120">Um einen Videorahmen abzurufen, rufen Sie [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) oder [**imediadet:: Write-Bitmapbits**](imediadet-writebitmapbits.md)auf.</span><span class="sxs-lookup"><span data-stu-id="e1a42-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="e1a42-121">Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.</span><span class="sxs-lookup"><span data-stu-id="e1a42-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="e1a42-122">Verwenden Sie nicht dasselbe mediadet-Objekt mit mehreren Dateien.</span><span class="sxs-lookup"><span data-stu-id="e1a42-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="e1a42-123">Um Informationen oder Video Frames aus mehr als einer Datei zu erhalten, verwenden Sie separate mediadet-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e1a42-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="e1a42-124">Die **imediadet** -Schnittstelle unterstützt keine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate, sodass Sie diese Schnittstelle nicht verwenden können, um Zeilen Sprung Felder oder Informationen über das Durchschneiden zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1a42-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="e1a42-125">Auch wenn der upstreamdecoder nur **VIDEOINFOHEADER2** unterstützt, können Sie nicht verwenden `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="e1a42-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="e1a42-126">Dies kann beispielsweise bei einem MPEG-2-Decoder der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="e1a42-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="e1a42-127">Außerdem ignoriert die- `IMediaDet` Schnittstelle alle Streams in der Datei, die keine Video-oder Audiodaten sind.</span><span class="sxs-lookup"><span data-stu-id="e1a42-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="e1a42-128">Wenn die Datei z. b. einen Audiostream, einen Datenstrom und einen Videostream enthält, meldet die **get \_ outputstreams** -Methode nur zwei Streams (Audiodaten und Videos).</span><span class="sxs-lookup"><span data-stu-id="e1a42-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="e1a42-129">Member</span><span class="sxs-lookup"><span data-stu-id="e1a42-129">Members</span></span>

<span data-ttu-id="e1a42-130">Die **imediadet** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e1a42-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1a42-131">**Imediadet** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1a42-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="e1a42-132">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1a42-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1a42-133">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1a42-133">Methods</span></span>

<span data-ttu-id="e1a42-134">Die **imediadet** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e1a42-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="e1a42-135">Methode</span><span class="sxs-lookup"><span data-stu-id="e1a42-135">Method</span></span>                                                        | <span data-ttu-id="e1a42-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1a42-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1a42-137">**Enterbitmapgrabmode**</span><span class="sxs-lookup"><span data-stu-id="e1a42-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="e1a42-138">Schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="e1a42-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="e1a42-139">**\_currentstream erhalten**</span><span class="sxs-lookup"><span data-stu-id="e1a42-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="e1a42-140">Ruft die streamnummer ab, die derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1a42-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="e1a42-141">**\_Dateiname erhalten**</span><span class="sxs-lookup"><span data-stu-id="e1a42-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="e1a42-142">Ruft den Namen der Quelldatei ab, die derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1a42-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="e1a42-143">**\_Filter erhalten**</span><span class="sxs-lookup"><span data-stu-id="e1a42-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="e1a42-144">Ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1a42-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="e1a42-145">**\_Framerate erhalten**</span><span class="sxs-lookup"><span data-stu-id="e1a42-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="e1a42-146">Ruft die Framerate des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="e1a42-147">**get \_ outputstreams**</span><span class="sxs-lookup"><span data-stu-id="e1a42-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="e1a42-148">Ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten und Videostreams ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="e1a42-149">**\_streamlength erhalten**</span><span class="sxs-lookup"><span data-stu-id="e1a42-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="e1a42-150">Ruft die Dauer des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="e1a42-151">**get \_ streammediatype**</span><span class="sxs-lookup"><span data-stu-id="e1a42-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="e1a42-152">Ruft den Medientyp des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="e1a42-153">**\_Streamtype aufrufen**</span><span class="sxs-lookup"><span data-stu-id="e1a42-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="e1a42-154">Ruft den Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="e1a42-155">**\_streamtypeb aufrufen**</span><span class="sxs-lookup"><span data-stu-id="e1a42-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="e1a42-156">Ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1a42-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="e1a42-157">**Getbitmapbits**</span><span class="sxs-lookup"><span data-stu-id="e1a42-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="e1a42-158">Ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="e1a42-159">**Getsamplegrabber**</span><span class="sxs-lookup"><span data-stu-id="e1a42-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="e1a42-160">Ruft einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e1a42-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="e1a42-161">**\_currentstream platzieren**</span><span class="sxs-lookup"><span data-stu-id="e1a42-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="e1a42-162">Gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1a42-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="e1a42-163">**\_Dateiname einfügen**</span><span class="sxs-lookup"><span data-stu-id="e1a42-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="e1a42-164">Gibt den Namen der Quelldatei an, die vom Medien Detektor verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1a42-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="e1a42-165">**\_Filter platzieren**</span><span class="sxs-lookup"><span data-stu-id="e1a42-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="e1a42-166">Gibt einen Quell Filter für das zu verwendende Medien Erkennungs Modul an.</span><span class="sxs-lookup"><span data-stu-id="e1a42-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="e1a42-167">**"Beschreib tebitmapbits"**</span><span class="sxs-lookup"><span data-stu-id="e1a42-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="e1a42-168">Ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="e1a42-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e1a42-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1a42-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e1a42-170">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e1a42-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1a42-171">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e1a42-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e1a42-172">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1a42-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1a42-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1a42-173">Requirements</span></span>



| <span data-ttu-id="e1a42-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1a42-174">Requirement</span></span> | <span data-ttu-id="e1a42-175">Wert</span><span class="sxs-lookup"><span data-stu-id="e1a42-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a42-176">Header</span><span class="sxs-lookup"><span data-stu-id="e1a42-176">Header</span></span><br/>  | <dl> <span data-ttu-id="e1a42-177"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e1a42-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e1a42-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1a42-178">Library</span></span><br/> | <dl> <span data-ttu-id="e1a42-179"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e1a42-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
