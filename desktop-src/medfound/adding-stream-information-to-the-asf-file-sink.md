---
description: Erfahren Sie mehr über das Hinzufügen von Streaminformationen zur ASF-Dateisenke, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Hinzufügen von Streaminformationen zur ASF-Dateisenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404357"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="443d7-103">Hinzufügen von Streaminformationen zur ASF-Dateisenke</span><span class="sxs-lookup"><span data-stu-id="443d7-103">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="443d7-104">Die ASF-Dateisenke ist eine Implementierung von [**DURCHFMediaSink Media Foundation**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="443d7-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="443d7-105">Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="443d7-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="443d7-106">Nach dem Instanziieren der Dateisenke muss sie vor dem Erstellen der Topologie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="443d7-106">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="443d7-107">Die Dateisenke muss die Datenströme in der Ausgabedatei, die Informationen zum Codierungsmodus und die Metadaten kennen.</span><span class="sxs-lookup"><span data-stu-id="443d7-107">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="443d7-108">In diesem Thema wird der Prozess zum Hinzufügen eines Streams in der Dateisenke beschrieben.</span><span class="sxs-lookup"><span data-stu-id="443d7-108">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="443d7-109">Hinzufügen von Streams in der ASF-Dateisenke</span><span class="sxs-lookup"><span data-stu-id="443d7-109">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="443d7-110">Aufzählen von Streamsenken</span><span class="sxs-lookup"><span data-stu-id="443d7-110">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="443d7-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="443d7-111">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="443d7-112">Hinzufügen von Streams in der ASF-Dateisenke</span><span class="sxs-lookup"><span data-stu-id="443d7-112">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="443d7-113">Die Dateisenke muss die Ausgabestreams und ihre Eigenschaften kennen, damit sie Ausgabebeispiele entsprechend generieren und der ASF-Ausgabedatei hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="443d7-113">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="443d7-114">Diese Einstellungen werden in das endgültige ASF-Headerobjekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="443d7-114">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="443d7-115">Um Streaminformationen festlegen zu können, müssen Sie über einen Verweis auf das ASF ContentInfo-Objekt der Dateisenke verfügen.</span><span class="sxs-lookup"><span data-stu-id="443d7-115">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="443d7-116">Weitere Informationen finden Sie unter [Erstellen der ASF-Dateisenke.](creating-the-asf-file-sink.md)</span><span class="sxs-lookup"><span data-stu-id="443d7-116">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="443d7-117">Im folgenden Verfahren werden die allgemeinen Schritte zum Konfigurieren des Streams mithilfe des ASF-Profilobjekts zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="443d7-117">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="443d7-118">**So konfigurieren Sie Streaminformationen in der ASF-Dateisenke**</span><span class="sxs-lookup"><span data-stu-id="443d7-118">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="443d7-119">Erstellen Sie ein ASF-Profilobjekt, indem [**Sie MFCreateASFProfile aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)</span><span class="sxs-lookup"><span data-stu-id="443d7-119">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="443d7-120">Erstellen Sie für jeden Stream in der Ausgabedatei einen Medientyp für den Zielstream, der der Dateisenke hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="443d7-120">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="443d7-121">Der Medientyp muss mit den Ausgabetypen kompatibel sein, die von den Windows Media Encodern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="443d7-121">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="443d7-122">Informationen zum Hinzufügen von Audiostreams zum Profil finden Sie unter Erstellen von Audiostreams für die ASF-Codierung.</span><span class="sxs-lookup"><span data-stu-id="443d7-122">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="443d7-123">Informationen zum Hinzufügen von Videostreams zum Profil finden Sie unter Erstellen von Videostreams für die ASF-Codierung.</span><span class="sxs-lookup"><span data-stu-id="443d7-123">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="443d7-124">Erstellen Sie Streams basierend auf den Medientypen, die in Schritt 2 erstellt wurden, indem [**Sie IMFASFProfile::CreateStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream)</span><span class="sxs-lookup"><span data-stu-id="443d7-124">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="443d7-125">Weisen Sie dem neu erstellten Stream eine Streamnummer zu, indem Sie den in Schritt 3 empfangenen [**IMFASFStreamConfig-Schnittstellenzeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="443d7-125">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="443d7-126">Konfigurieren Sie optional den Stream mit den folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="443d7-126">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="443d7-127">Leaky bucket parameters by setting the attributes: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="443d7-127">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="443d7-128">Nutzlasterweiterung, gegenseitiger Ausschluss durch Aufrufen von [**IMFASFStreamConfig-Methoden.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)</span><span class="sxs-lookup"><span data-stu-id="443d7-128">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="443d7-129">Legen Sie optional die Datenpaketgröße für das Profil fest, indem Sie die [**Attribute MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) und [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="443d7-129">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="443d7-130">Das ASF-Profil macht die [**BEFIAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) verfügbar, auf die eine Anwendung verweisen kann, indem **sie IMFASFProfile::QueryInterface aufruft.**</span><span class="sxs-lookup"><span data-stu-id="443d7-130">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="443d7-131">Legen Sie die Codierungsinformationen für den Stream in der Dateisenke fest.</span><span class="sxs-lookup"><span data-stu-id="443d7-131">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="443d7-132">Dies wird unter [Festlegen von Eigenschaften in der Dateisenke erläutert.](setting-properties-in-the-file-sink.md)</span><span class="sxs-lookup"><span data-stu-id="443d7-132">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="443d7-133">Fügen Sie den Stream dem Profil hinzu, indem Sie [**IMFASFProfile::SetStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)</span><span class="sxs-lookup"><span data-stu-id="443d7-133">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="443d7-134">Ordnen Sie das Profil dem ContentInfo-Objekt zu, indem [**Sie IMFASFContentInfo::SetProfile aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)</span><span class="sxs-lookup"><span data-stu-id="443d7-134">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="443d7-135">Um einen vorhandenen Stream zu ändern, kann die Anwendung einen Verweis auf die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) des Streams erhalten und gemäß den Anforderungen neu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="443d7-135">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="443d7-136">Zum Hinzufügen oder Entfernen von Streams muss die Anwendung [**IMFASFProfile::RemoveStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)</span><span class="sxs-lookup"><span data-stu-id="443d7-136">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="443d7-137">Um diese Änderungen zu übernehmen, Änderungen zu streamen oder zu entfernen, müssen Sie das Profil erneut im ContentInfo-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="443d7-137">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="443d7-138">Dadurch wird das vorhandene Profil überschrieben, das dem ContentInfo-Objekt bereits zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="443d7-138">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="443d7-139">Aufzählen von Streamsenken</span><span class="sxs-lookup"><span data-stu-id="443d7-139">Enumerating Stream Sinks</span></span>

<span data-ttu-id="443d7-140">Für jeden Stream im Profil, den das ContentInfo-Objekt kennt, erstellt die ASF-Dateisenke eine Streamsenke, die alle Eigenschaften des codierten Streams enthält, und fügt sie hinzu.</span><span class="sxs-lookup"><span data-stu-id="443d7-140">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="443d7-141">Die ASF-Dateisenke ist für feste Streams konzipiert.</span><span class="sxs-lookup"><span data-stu-id="443d7-141">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="443d7-142">Dies bedeutet, dass Sie keine Streams hinzufügen oder entfernen können, indem Sie [**DENKMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) oder [**DENKMediaSink::RemoveStreamSink aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)</span><span class="sxs-lookup"><span data-stu-id="443d7-142">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="443d7-143">Bei diesen Aufrufen für die Dateisenke tritt ein Fehler mit dem Fehlercode "MF \_ E \_ STREAMSINKS \_ FIXED" auf.</span><span class="sxs-lookup"><span data-stu-id="443d7-143">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="443d7-144">Beim Hinzufügen oder Entfernen von Streams im Profil werden die Streamsenken in der Dateisenke nicht automatisch hinzugefügt oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="443d7-144">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="443d7-145">Sie müssen die vorhandene Instanz der Datei verwerfen und mit neuen Datenstrominformationen neu erstellen, wenn sich Ihre Streams im Profil geändert haben.</span><span class="sxs-lookup"><span data-stu-id="443d7-145">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="443d7-146">Im folgenden Verfahren werden die allgemeinen Schritte zum Aufzählen von Streamsenken in der ASF-Dateisenke zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="443d7-146">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="443d7-147">**So enumerieren Sie Streamsenken**</span><span class="sxs-lookup"><span data-stu-id="443d7-147">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="443d7-148">Rufen [**Sie VORZEICHENMedienSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) auf, um die Gesamtzahl der Streamsenken in der ASF-Dateisenke zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="443d7-148">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="443d7-149">Eine Schleife durch die Streamsenken ang erhalten einen Verweis auf die [**GetStreamSinkByIndex-Schnittstelle**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) der Streamsenke.</span><span class="sxs-lookup"><span data-stu-id="443d7-149">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="443d7-150">Oder</span><span class="sxs-lookup"><span data-stu-id="443d7-150">-or-</span></span>

    <span data-ttu-id="443d7-151">Rufen [**Sie durch Angabe der Datenstromnummer DEN NAMEN DESINKMEDIASink::GetStreamSinkById-Werts**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) auf, um die Streamsenke zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="443d7-151">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="443d7-152">Jede Streamsenke wird mit der Streamnummer identifiziert, die Sie beim Erstellen des Streams im Profil festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="443d7-152">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="443d7-153">Wenn Sie eine Teiltopologie zum Codieren einer Mediendatei erstellen, müssen Sie der Topologie die Dateisenke als Ausgabetopologieknoten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="443d7-153">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="443d7-154">Dazu können Sie entweder jede Streamsenke in der Dateisenke angeben oder das Aktivierungsobjekt der Dateisenke und die Bezeichner der Streamsenke festlegen.</span><span class="sxs-lookup"><span data-stu-id="443d7-154">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="443d7-155">Weitere Informationen und Codebeispiele finden Sie unter [Erstellen von Ausgabeknoten.](creating-output-nodes.md)</span><span class="sxs-lookup"><span data-stu-id="443d7-155">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="443d7-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="443d7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="443d7-157">ASF-Mediensenken</span><span class="sxs-lookup"><span data-stu-id="443d7-157">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="443d7-158">ASF-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="443d7-158">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



