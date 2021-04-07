---
title: Übertragungen von ASF-Daten
description: Übertragungen von ASF-Daten
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media-Format-SDK, Senden von ASF-Daten
- Advanced Systems Format (ASF), Broadcast von Daten
- ASF (Advanced Systems Format), Broadcasting Data
- Windows Media-Format-SDK, Senden von ASF-Daten
- Advanced Systems Format (ASF), Senden von Daten
- ASF (Advanced Systems Format), Senden von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104038665"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="37725-109">Übertragungen von ASF-Daten</span><span class="sxs-lookup"><span data-stu-id="37725-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="37725-110">In diesem Thema wird beschrieben, wie Sie mit dem HTTP-Protokoll ASF-Daten über ein Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="37725-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="37725-111">Zum Senden von Dateien über ein Netzwerk ist die Verwendung des Writer-Objekts erforderlich. Daher sollten Sie vor dem Lesen dieses Themas über ein allgemeines Verständnis dieses Objekts verfügen.</span><span class="sxs-lookup"><span data-stu-id="37725-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="37725-112">Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="37725-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="37725-113">Wenn Sie mit nicht komprimierten Daten beginnen, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="37725-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="37725-114">Erstellen Sie das Writer-Objekt, indem Sie die [**wmcreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37725-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="37725-115">Diese Funktion gibt einen **iwmwriter** -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="37725-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="37725-116">Erstellen Sie das netzwerksink-Objekt, indem Sie die [**wmcreateschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) -Funktion aufrufen, die einen **iwmschreiternetworksink** -Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="37725-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="37725-117">Nennen Sie [**iwmschreiternetworksink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) in der Netzwerk Senke, und geben Sie die Portnummer an, die geöffnet werden soll. Beispiel: 8080.</span><span class="sxs-lookup"><span data-stu-id="37725-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="37725-118">Zum Abrufen der URL des Hosts können Sie optional [**iwmschreiternetworksink:: gethosturl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37725-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="37725-119">Clients greifen über diese URL auf den Inhalt zu.</span><span class="sxs-lookup"><span data-stu-id="37725-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="37725-120">Sie können auch [**iwmschreiternetworksink:: setmaximumclients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) aufrufen, um die Anzahl der Clients einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="37725-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="37725-121">Fügen Sie die Netzwerk Senke an den Writer an, indem Sie [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) für den Writer aufrufen, mit einem Zeiger auf die **iwmschreiternetworksink** -Schnittstelle der Netzwerk Senke.</span><span class="sxs-lookup"><span data-stu-id="37725-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="37725-122">Legen Sie das ASF-Profil fest, indem Sie die [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) -Methode für das Writer-Objekt mit einem [**iwmprofile**](iwmprofile.md) -Zeiger aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37725-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="37725-123">Weitere Informationen zum Erstellen eines Profils finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="37725-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="37725-124">Optional können Sie Metadaten mithilfe der [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle für den Writer angeben.</span><span class="sxs-lookup"><span data-stu-id="37725-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="37725-125">Nennen Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) für den Writer.</span><span class="sxs-lookup"><span data-stu-id="37725-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="37725-126">Für jedes Beispiel wird die [**iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="37725-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="37725-127">Geben Sie die Datenstrom Nummer, die Präsentationszeit, die Dauer der Stichprobe und einen Zeiger auf den Beispiel Puffer an.</span><span class="sxs-lookup"><span data-stu-id="37725-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="37725-128">Die Methode " **Write tesample** " komprimiert die Beispiele.</span><span class="sxs-lookup"><span data-stu-id="37725-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="37725-129">Wenn Sie den Vorgang abgeschlossen haben, nennen Sie [**iwmwriter:: endwriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) für den Writer.</span><span class="sxs-lookup"><span data-stu-id="37725-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="37725-130">Nennen Sie [**iwmschreiteradvanced:: removesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) auf dem Writer, um das netzwerksink-Objekt zu trennen.</span><span class="sxs-lookup"><span data-stu-id="37725-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="37725-131">Nennen Sie [**iwmschreiternetworksink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) in der Netzwerk Senke, um den Port freizugeben.</span><span class="sxs-lookup"><span data-stu-id="37725-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="37725-132">Eine weitere Möglichkeit zum Streamen von ASF-Inhalten über ein Netzwerk besteht darin, Sie aus einer vorhandenen ASF-Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="37725-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="37725-133">Das im SDK bereitgestellte wmvnetwrite-Beispiel veranschaulicht diese Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="37725-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="37725-134">Führen Sie zusätzlich zu den zuvor aufgeführten Schritten folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="37725-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="37725-135">Erstellen Sie ein Reader-Objekt, und rufen Sie die **Open** -Methode mit dem Namen der Datei auf.</span><span class="sxs-lookup"><span data-stu-id="37725-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="37725-136">Aufrufen von [**iwmreaderadvanced:: setmanualstreamselection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) für das Reader-Objekt mit dem Wert " **true**".</span><span class="sxs-lookup"><span data-stu-id="37725-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="37725-137">Dadurch kann die Anwendung jeden Stream in der Datei lesen, einschließlich Streams mit gegenseitigem Ausschluss.</span><span class="sxs-lookup"><span data-stu-id="37725-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="37725-138">Fragen Sie den Reader nach der [**iwmprofile**](iwmprofile.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="37725-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="37725-139">Verwenden Sie diesen Zeiger, wenn Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) für das Writer-Objekt aufrufen (Schritt 5 in der vorherigen Prozedur).</span><span class="sxs-lookup"><span data-stu-id="37725-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="37725-140">Für jeden Stream, der im Profil definiert ist, können Sie [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) aufrufen, um die streamnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37725-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="37725-141">Übergeben Sie diese streamnummer an die [**iwmreaderadvanced:: setreceivestreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) -Methode des Readers.</span><span class="sxs-lookup"><span data-stu-id="37725-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="37725-142">Diese Methode teilt dem Reader mit, komprimierte Beispiele zu liefern, anstatt Sie zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="37725-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="37725-143">Die Beispiele werden mithilfe der [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) -Rückruf Methode der Anwendung an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="37725-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="37725-144">Sie müssen die Codec-Informationen für jeden Datenstrom abrufen, den Sie unkomprimiert gelesen haben, und ihn vor der Übertragung dem Header hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37725-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="37725-145">Rufen Sie zum Abrufen der Codec-Informationen [**IWMHeaderInfo2:: getcodecinfocount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2:: getcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="37725-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="37725-146">Wählen Sie die Codec-Informationen aus, die der Datenstrom Konfiguration entsprechen.</span><span class="sxs-lookup"><span data-stu-id="37725-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="37725-147">Legen Sie dann die Codec-Informationen im Writer durch Aufrufen von [**IWMHeaderInfo3:: addcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)fest, und übergeben Sie dabei die Informationen, die vom Reader abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37725-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="37725-148">Nachdem Sie das Profil für den Writer festgelegt haben, können Sie [**iwmwriter:: getinputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) für den Writer aufrufen, um die Anzahl der Eingaben zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="37725-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="37725-149">Geben Sie für jede Eingabe den Wert " [**iwmwriter::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) " mit dem Wert **null** an.</span><span class="sxs-lookup"><span data-stu-id="37725-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="37725-150">Dadurch wird dem Writer-Objekt angezeigt, dass die Anwendung komprimierte Beispiele bereitstellt, sodass der Writer keine Codecs zum Komprimieren der Daten verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="37725-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="37725-151">Stellen Sie sicher, dass Sie vor dem Aufrufen von **beginwriting**"" vor **dem Aufruf von** "</span><span class="sxs-lookup"><span data-stu-id="37725-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="37725-152">Kopieren Sie optional die Metadatenattribute vom Reader in den Writer.</span><span class="sxs-lookup"><span data-stu-id="37725-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="37725-153">Da die Beispiele des Readers bereits komprimiert sind, verwenden Sie die Methode [**iwmschreiteradvanced:: schreitestreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) , um die Beispiele anstelle der **beschreitesample** -Methode zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="37725-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="37725-154">Die " **Write-streamsample** "-Methode umgeht die üblichen Komprimierungs Prozeduren des Writer-Objekts.</span><span class="sxs-lookup"><span data-stu-id="37725-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="37725-155">Wenn der Reader das Ende der Datei erreicht, sendet er eine WMT- \_ Benachrichtigungs Benachrichtigung an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="37725-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="37725-156">Außerdem sollte die Anwendung die Uhr auf dem Reader-Objekt steuern, damit der Reader so schnell wie möglich Daten aus der Datei abruft.</span><span class="sxs-lookup"><span data-stu-id="37725-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="37725-157">Rufen Sie hierzu die [**iwmreaderadvanced:: setuserprovidedclock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) -Methode für den Reader mit dem Wert " **true**" auf.</span><span class="sxs-lookup"><span data-stu-id="37725-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="37725-158">Nachdem der Reader die WMT \_ Started-Benachrichtigung gesendet hat, rufen Sie [**iwmreaderadvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) auf, und geben Sie das Zeitintervall an, das der Reader übermitteln soll.</span><span class="sxs-lookup"><span data-stu-id="37725-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="37725-159">Nachdem der Reader das Zeitintervall gelesen hat, ruft er die [**iwmreadercallbackadvanced:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) -Rückruf Methode der Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="37725-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="37725-160">Die Anwendung sollte **delivertime** erneut abrufen, um das nächste Zeitintervall zu lesen.</span><span class="sxs-lookup"><span data-stu-id="37725-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="37725-161">So können Sie z. b. in Intervallen von einer Sekunde aus der Datei lesen:</span><span class="sxs-lookup"><span data-stu-id="37725-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="37725-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37725-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37725-163">**Senden von ASF-Daten über ein Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="37725-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="37725-164">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="37725-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




