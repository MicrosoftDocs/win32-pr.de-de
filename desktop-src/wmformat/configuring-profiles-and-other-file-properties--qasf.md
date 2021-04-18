---
title: Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)
description: Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media-Format-SDK, Konfigurieren von Profilen (qasf)
- Windows Media-Format-SDK, Konfigurieren von Dateieigenschaften (qasf)
- Windows Media-Format-SDK, Metadaten (qasf)
- Advanced Systems Format (ASF), Konfigurieren von Profilen (qasf)
- ASF (Advanced Systems Format), Konfigurieren von Profilen (qasf)
- Advanced Systems Format (ASF), Konfigurieren von Dateieigenschaften (qasf)
- ASF (Advanced Systems Format), Konfigurieren von Dateieigenschaften (qasf)
- Advanced Systems Format (ASF), Metadaten (qasf)
- ASF (Advanced Systems Format), Metadaten (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- Metadaten, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473740"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="d3eda-116">Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="d3eda-117">In den folgenden Artikeln wird beschrieben, wie verschiedene Aufgaben im Zusammenhang mit der Erstellung von ASF-Dateien durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3eda-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="d3eda-118">Erstellen eines Profils (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="d3eda-119">Um ein benutzerdefiniertes Profil zu erstellen, verwenden Sie das Windows Media SDK-SDK direkt, um ein Profil-Manager-Objekt mithilfe der [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="d3eda-120">Erstellen Sie als nächstes das Profil, und übergeben Sie es mithilfe der [**iconfigasfwriter:: konfigurifisingprofile**](iconfigasfwriter-configurefilterusingprofile.md) -Methode an den [WM-ASF-Writer](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d3eda-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="d3eda-121">Dies ist die einzige Möglichkeit, den Filter mit einem Profil zu konfigurieren, das die Codecs Windows Media Audio und der Video 9-Serie verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3eda-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="d3eda-122">System Profile für frühere Versionen dieser Codecs können mithilfe der [**iconfigasfwriter:: Konfigurations refilterusingprofileguid**](iconfigasfwriter-configurefilterusingprofileguid.md) -Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d3eda-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="d3eda-123">Hinzufügen von Metadaten (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="d3eda-124">Rufen Sie zum Hinzufügen von Metadaten zu einer Datei **QueryInterface** von der **ibasefilter** -Schnittstelle auf dem [WM-ASF-Writer](wm-asf-writer-filter.md) auf, um die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="d3eda-125">Nachdem dem Filter ein Profil zugewiesen wurde, verwenden Sie die **iwmheaderinfo** -Schnittstellen Methoden, um die Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d3eda-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="d3eda-126">Indizieren einer Datei (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="d3eda-127">Der WM-ASF-Writer erstellt standardmäßig Temporale indizierte Dateien.</span><span class="sxs-lookup"><span data-stu-id="d3eda-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="d3eda-128">Verwenden Sie zum Erstellen einer Frame indizierten Datei die [**iconfigasfwriter:: setindexmode**](iconfigasfwriter-setindexmode.md) -Methode, um die gesamte Indizierung zu deaktivieren, und erstellen Sie dann die Datei.</span><span class="sxs-lookup"><span data-stu-id="d3eda-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="d3eda-129">Verwenden Sie nach Abschluss des Vorgangs das SDK für den Windows Media-Format, um einen Frame basierten Index für die Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="d3eda-130">Ausführen Two-Pass Codierung (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="d3eda-131">Die zwei-Pass-Codierung wird nur auf Windows Media-Codecs der Version 8 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3eda-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="d3eda-132">Versetzen Sie den WM-ASF-Writer in den Vorverarbeitungs-Modus, indem Sie [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) aufrufen und am \_ configasfwriter \_ param \_ Multipass im *dwparam* -Parameter und **true** im *dwParam1* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d3eda-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="d3eda-133">Führen Sie dann das Filter Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="d3eda-133">Then run the filter graph.</span></span> <span data-ttu-id="d3eda-134">Wenn alle Vorverarbeitungs Durchläufen abgeschlossen sind (in der Regel wird nur ein Vorverarbeitungs Durchlauf ausgeführt), empfängt die Anwendung ein Ereignis vom Typ " **\_ Preprocess \_ Complete** " vom Filter.</span><span class="sxs-lookup"><span data-stu-id="d3eda-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="d3eda-135">Wenn dieses Ereignis empfangen wird, verwenden Sie **imediaseeking:: setpositions** , um den Streamzeiger auf den Anfang zurückzusetzen, und führen Sie das Filter Diagramm erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d3eda-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="d3eda-136">Nach dem letzten Durchlauf (in der Regel der zweite Durchlauf) empfängt die Anwendung ein **EC \_ Complete** -Ereignis, um anzugeben, dass der Codierungsprozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d3eda-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="d3eda-137">Wenn ein Vorverarbeitungs Durchlauf abgebrochen wird, bevor das Ereignis für das Ereignis " **EC \_ Preprocess \_ Complete** " empfangen wird, rufen Sie [**IConfigAsfWriter2:: resetmultipassstate**](iconfigasfwriter2-resetmultipassstate.md) auf, um den Filter vor dem Versuch einer anderen Vorverarbeitungs Ausführung zurückzusetzen</span><span class="sxs-lookup"><span data-stu-id="d3eda-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="d3eda-138">Es ist nur erforderlich, **iconfigasfwriter:: SetParam**(am \_ configasfwriter \_ param \_ Multipass, **false**) aufzurufen, wenn Sie den Filter vollständig aus dem Vorverarbeitungs Modus setzen möchten.</span><span class="sxs-lookup"><span data-stu-id="d3eda-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3eda-139">Die Anwendung ist dafür verantwortlich, den Vorverarbeitungs Modus basierend auf dem Profil zu aktivieren, das für die Codierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3eda-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="d3eda-140">Für einige Profile ist die zwei-Pass-Codierung erforderlich. Wenn Sie versuchen, eine Datei mit einem solchen Profil zu codieren, und am \_ configasfwriter \_ param \_ Multipass nicht auf **true** festgelegt ist, führt dies zu einem Fehler vom Typ " \_ userabort".</span><span class="sxs-lookup"><span data-stu-id="d3eda-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="d3eda-141">Weitere Informationen dazu, wie Sie bestimmen können, ob für ein bestimmtes Profil zwei-Pass-Codierungen erforderlich sind, finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bitrate Streams](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="d3eda-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="d3eda-142">Erhalten und Festlegen von Puffer Eigenschaften zur Laufzeit (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="d3eda-143">In einigen Szenarien, z. b. Wenn Sie die Tastenkombination beim Schreiben einer Datei erzwingen möchten, muss eine Anwendung möglicherweise Informationen zu einem Windows-Medien Puffer zur Laufzeit erhalten oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="d3eda-144">Die Filter " [WM ASF Reader](wm-asf-reader-filter.md) " und " [WM ASF Writer](wm-asf-writer-filter.md) " unterstützen beide einen Rückrufmechanismus, mit dem eine Anwendung beim Lesen oder Schreiben von Dateien auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle auf jedem einzelnen Medien Puffer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="d3eda-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="d3eda-145">Anwendungen können diese Schnittstelle verwenden, um bestimmte Beispiele als Keyframes oder [*cleanpoints*](wmformat-glossary.md)festzulegen, um SMPTE-Zeit Codes festzulegen, damit-Einstellungen anzugeben oder einen beliebigen Typ privater Daten einem Stream hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="d3eda-146">Verwenden Sie die [**iamwmbufferpass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) -Schnittstelle, um Rückrufe von der PIN zu registrieren, die den Videostream verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d3eda-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="d3eda-147">Wenn die PIN die [**iamwmbufferpasscallback:: notify**](iamwmbufferpasscallback-notify.md) -Methode aufruft, untersuchen Sie die Zeitstempel des Puffers, und rufen Sie ggf. [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) auf, um die " **WM \_ sampleextensionguid \_ outputcleanpoint** "-Eigenschaft für den Puffer auf " **true**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="d3eda-148">Unterstützung von nicht quadratischen Pixeln (qasf)</span><span class="sxs-lookup"><span data-stu-id="d3eda-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="d3eda-149">Der WM-ASF-Writer stellt eine Verbindung mit einem upstreamfilter her, z. b. dem DV-Decoder, der Informationen zum Pixel Seitenverhältnis ausgibt</span><span class="sxs-lookup"><span data-stu-id="d3eda-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="d3eda-150">Der WM-ASF-Writer schreibt diese Informationen als Dateneinheiten Erweiterungen für jedes Beispiel in der Datei.</span><span class="sxs-lookup"><span data-stu-id="d3eda-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="d3eda-151">Wenn der WM-ASF-Reader die Pixel-Seitenverhältnis Informationen im Dateiheader oder in den Dateneinheiten Erweiterungen für die Beispiele findet, bietet er einen **VIDEOINFOHEADER2** -Medientyp als erste Wahl in der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="d3eda-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="d3eda-152">Die Member **dwpictaspectratiox** und **dwpictaspectratioy** der Struktur, die das Seitenverhältnis des Video Rechtecks beschreiben, werden richtig angepasst, um das Pixel Seitenverhältnis zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="d3eda-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="d3eda-153">Beibehalten des interschnür Formats</span><span class="sxs-lookup"><span data-stu-id="d3eda-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="d3eda-154">Wenn Sie in einem Fernsehgerät oder einer DV-Kamera Zeilen Sprung Video aufzeichnen, sollten Sie das Originalvideo als unabhängige Felder aufbewahren, wenn Sie davon ausgehen, dass die codierte Datei in einem Fernsehgerät oder einem anderen Zeilen Sprung Gerät wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3eda-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="d3eda-155">(Computer Monitore sind progressiv-Scangeräte.) Wenn Sie ein Video deinstalften und dann für die Wiedergabe in einem Fernsehgerät wiederherstellen, entstehen Datenverluste.</span><span class="sxs-lookup"><span data-stu-id="d3eda-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="d3eda-156">In einer ASF-Datei werden Zeilen Sprung-Informationen als Dateneinheiten Erweiterungen gespeichert, die die Anwendung auf die einzelnen Beispiele anwendet, indem die zuvor beschriebene **iamwmbufferpasscallback** -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3eda-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="d3eda-157">Führen Sie die folgenden Schritte aus, um eine Datei zu codieren, die die ursprünglichen damit-Einstellungen beibehält:</span><span class="sxs-lookup"><span data-stu-id="d3eda-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="d3eda-158">Implementieren Sie eine Klasse, die **iamwmbufferpasscallback** unterstützt, und schreiben Sie eine Benachrichtigungsfunktion, die die damit-Flags für die einzelnen Stichproben festlegt.</span><span class="sxs-lookup"><span data-stu-id="d3eda-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="d3eda-159">Diese Funktion wird vom WM-ASF-Writer aufgerufen, bevor die einzelnen Beispiele verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d3eda-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="d3eda-160">Legen Sie die dateneinheits Erweiterungen für das Profil fest, bevor Sie das Profil an den Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d3eda-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="d3eda-161">Nachdem Sie den Filter mit dem Profil konfiguriert haben, rufen Sie die **IWMWriterAdvanced2** -Schnittstelle vom WM-ASF-Writer ab, und rufen Sie **die Methode "** die Methode".</span><span class="sxs-lookup"><span data-stu-id="d3eda-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
CComPtr<IServiceProvider> pProvider;
  CComPtr<IWMWriterAdvanced2> pWMWA2;
  hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                         (void**)&pProvider);
  if (SUCCEEDED(hr))
  {
      hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
                    IID_IWMWriterAdvanced2,
                    (void**)&pWMWA2);
  }
  BOOL pValue = TRUE;
 // Set the first parameter to your actual input number.
 hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
              WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
            
```



 

 