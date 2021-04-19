---
description: Die ASF-Datei Senke ist eine Implementierung von imfmediasink, die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell der ASF-Medien senken und zur allgemeinen Verwendung finden Sie unter ASF-Medien senken.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Hinzufügen von streaminformationen zur ASF-Datei-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345051"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="2263a-104">Hinzufügen von streaminformationen zur ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="2263a-104">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="2263a-105">Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="2263a-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="2263a-106">Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="2263a-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="2263a-107">Nach dem Instanziieren der Datei Senke muss Sie vor dem Erstellen der Topologie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2263a-107">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="2263a-108">Die Datei Senke muss die Datenströme in der Ausgabedatei, die Codierungs Modus-Informationen und die Metadaten kennen.</span><span class="sxs-lookup"><span data-stu-id="2263a-108">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="2263a-109">In diesem Thema wird der Vorgang zum Hinzufügen von Datenströmen in der Datei Senke beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2263a-109">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="2263a-110">Hinzufügen von Streams in der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="2263a-110">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="2263a-111">Auflisten von streamsenken</span><span class="sxs-lookup"><span data-stu-id="2263a-111">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="2263a-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2263a-112">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="2263a-113">Hinzufügen von Streams in der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="2263a-113">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="2263a-114">Die Datei Senke muss die Ausgabestreams und ihre Eigenschaften kennen, damit Sie Ausgabe Beispiele entsprechend generieren und der Ausgabe-ASF-Datei hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="2263a-114">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="2263a-115">Diese Einstellungen werden in das endgültige Objekt des ASF-Headers geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2263a-115">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="2263a-116">Um streaminformationen festzulegen, müssen Sie über einen Verweis auf das ASF ContentInfo-Objekt der Datei Senke verfügen.</span><span class="sxs-lookup"><span data-stu-id="2263a-116">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="2263a-117">Weitere Informationen finden Sie unter [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="2263a-117">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="2263a-118">Im folgenden Verfahren werden die allgemeinen Schritte zum Konfigurieren des Streams mithilfe des ASF-Profil Objekts zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2263a-118">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="2263a-119">**So konfigurieren Sie streaminformationen in der ASF-Datei-Senke**</span><span class="sxs-lookup"><span data-stu-id="2263a-119">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="2263a-120">Erstellen Sie ein ASF-Profil Objekt, indem Sie [**mfcreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-120">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="2263a-121">Erstellen Sie für jeden Stream in der Ausgabedatei einen Medientyp für den Zielstream, der in der Datei Senke hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2263a-121">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="2263a-122">Der Medientyp muss mit den von den Windows Media Encoder unterstützten Ausgabetypen kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="2263a-122">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="2263a-123">Weitere Informationen zum Hinzufügen von Audiodatenströmen zum Profil finden Sie unter Creating Audiostreams for ASF Encoding.</span><span class="sxs-lookup"><span data-stu-id="2263a-123">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="2263a-124">Weitere Informationen zum Hinzufügen von Videostreams zum Profil finden Sie unter Erstellen von Videostreams für die ASF-Codierung.</span><span class="sxs-lookup"><span data-stu-id="2263a-124">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="2263a-125">Erstellen Sie Streams basierend auf den in Schritt 2 erstellten Medientypen durch Aufrufen von [**imfasfprofile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="2263a-125">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="2263a-126">Weisen Sie eine streamnummer für den neu erstellten Stream zu, indem Sie den in Schritt 3 empfangenen [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstellen Zeiger aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-126">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="2263a-127">Konfigurieren Sie den Stream optional mit den folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="2263a-127">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="2263a-128">Lecks von Bucket-Parametern durch Festlegen der Attribute: [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) oder [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="2263a-128">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="2263a-129">Nutz Last Erweiterung, gegenseitiger Ausschluss durch Aufrufen von [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="2263a-129">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="2263a-130">Legen Sie optional die Größe des Datenpakets für das Profil fest, indem Sie die Eigenschaften " [**MF \_ asfprofile \_ MinPacketSize**](mf-asfprofile-minpacketsize-attribute.md) " und " [**MF \_ asfprofile \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) " festlegen</span><span class="sxs-lookup"><span data-stu-id="2263a-130">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="2263a-131">Das ASF-Profil macht die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle verfügbar, auf die eine Anwendung durch Aufrufen von **imfasfprofile:: QueryInterface** verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="2263a-131">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="2263a-132">Legen Sie Codierungsinformationen für den Stream in der Datei Senke fest.</span><span class="sxs-lookup"><span data-stu-id="2263a-132">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="2263a-133">Erläutert unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="2263a-133">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="2263a-134">Fügen Sie den Stream zum Profil hinzu, indem Sie [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-134">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="2263a-135">Ordnen Sie das Profil dem ContentInfo-Objekt zu, indem Sie [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-135">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="2263a-136">Um einen vorhandenen Stream zu ändern, kann die Anwendung einen Verweis auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle des Streams erhalten und entsprechend den Anforderungen neu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2263a-136">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="2263a-137">Zum Hinzufügen oder Entfernen von Streams muss die Anwendung [**imfasfprofile:: removestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-137">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="2263a-138">Um diese Änderungen, streamänderungen oder Entfernungs Änderungen zu übernehmen, müssen Sie das Profil erneut im ContentInfo-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="2263a-138">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="2263a-139">Dies überschreibt das vorhandene Profil, das bereits mit dem ContentInfo-Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="2263a-139">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


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



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="2263a-140">Auflisten von streamsenken</span><span class="sxs-lookup"><span data-stu-id="2263a-140">Enumerating Stream Sinks</span></span>

<span data-ttu-id="2263a-141">Für jeden Datenstrom im Profil, den das ContentInfo-Objekt kennt, erstellt die ASF-Datei-Senke eine streamsenke, die alle Eigenschaften des codierten Streams enthält, und fügt Sie hinzu.</span><span class="sxs-lookup"><span data-stu-id="2263a-141">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="2263a-142">Die ASF-Datei-Senke enthält fixierte Datenströme.</span><span class="sxs-lookup"><span data-stu-id="2263a-142">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="2263a-143">Dies bedeutet, dass Sie Datenströme nicht hinzufügen oder entfernen können, indem Sie [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) oder [**imfmediasink:: removestreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2263a-143">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="2263a-144">Diese Aufrufe für die Datei-Senke schlagen mit dem \_ Fehlercode "MF E \_ streamsinks Fixed" fehl \_ .</span><span class="sxs-lookup"><span data-stu-id="2263a-144">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="2263a-145">Durch das Hinzufügen oder Entfernen von Streams im Profil werden die streamsenken in der Datei Senke nicht automatisch hinzugefügt oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="2263a-145">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="2263a-146">Wenn sich ihre Streams im Profil geändert haben, müssen Sie die vorhandene Instanz der Datei verwerfen und mit neuen Datenstrom Informationen neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2263a-146">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="2263a-147">Im folgenden Verfahren werden die allgemeinen Schritte zum Auflisten von streamsenken in der ASF-Datei-Senke zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2263a-147">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="2263a-148">**So zählen Sie streamsenken auf**</span><span class="sxs-lookup"><span data-stu-id="2263a-148">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="2263a-149">Aufrufen von [**imfmediasink:: getstreamsink count**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) zum Abrufen der Gesamtanzahl von streamsenken in der ASF-Datei-Senke.</span><span class="sxs-lookup"><span data-stu-id="2263a-149">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="2263a-150">Schleife durch die Stream-senken: erhalten Sie einen Verweis auf die [**getstreamsink byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) -Schnittstelle der Stream-Senke.</span><span class="sxs-lookup"><span data-stu-id="2263a-150">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="2263a-151">Oder</span><span class="sxs-lookup"><span data-stu-id="2263a-151">-or-</span></span>

    <span data-ttu-id="2263a-152">Aufrufen von [**imfmediasink:: getstreamsinkbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) zum Abrufen der streamsenke durch Angeben der streamnummer.</span><span class="sxs-lookup"><span data-stu-id="2263a-152">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="2263a-153">Jede streamsenke wird durch die Datenstrom Nummer identifiziert, die Sie beim Erstellen des Streams im Profil festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="2263a-153">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="2263a-154">Wenn Sie eine partielle Topologie zum Codieren einer Mediendatei entwickeln, müssen Sie die Datei Senke der Topologie als Knoten für die Ausgabe Topologie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2263a-154">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="2263a-155">Sie können dazu entweder jede streamsenke in der Datei Senke angeben oder das Datei-senkenaktivierungs-und die Datenstrom-senkenbezeichner festlegen.</span><span class="sxs-lookup"><span data-stu-id="2263a-155">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="2263a-156">Weitere Informationen und ein Codebeispiel finden Sie unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="2263a-156">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2263a-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2263a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2263a-158">ASF-Medien senken</span><span class="sxs-lookup"><span data-stu-id="2263a-158">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="2263a-159">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2263a-159">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



