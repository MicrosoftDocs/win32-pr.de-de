---
description: Konfigurieren von Profilen und anderen ASF-Dateieigenschaften
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Konfigurieren von Profilen und anderen ASF-Dateieigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392729"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="08d5c-103">Konfigurieren von Profilen und anderen ASF-Dateieigenschaften</span><span class="sxs-lookup"><span data-stu-id="08d5c-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="08d5c-104">In den folgenden Artikeln wird beschrieben, wie verschiedene Aufgaben im Zusammenhang mit der Erstellung von ASF-Dateien durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08d5c-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="08d5c-105">Einige der in diesem Thema erwähnten Schnittstellen sind in der Dokumentation zum Windows Media-Format SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="08d5c-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="08d5c-106">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="08d5c-106">Creating a Profile</span></span>

<span data-ttu-id="08d5c-107">ASF-Profile werden im Windows Media-Format SDK ausführlich erläutert. im wesentlichen beschreiben Sie Attribute einer Windows Media-Format Datei, z. b. Bitrate, Anzahl und Typ von Streams und Komprimierungs Qualität.</span><span class="sxs-lookup"><span data-stu-id="08d5c-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="08d5c-108">Der Filter verwendet das Profil, um zu bestimmen, welche Art von Windows Media-Format Datei geschrieben werden soll, wie viele Eingabe Pins Sie einrichten muss und welche Medientypen akzeptiert werden können.</span><span class="sxs-lookup"><span data-stu-id="08d5c-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="08d5c-109">Um ein benutzerdefiniertes Profil zu erstellen, verwenden Sie das Windows Media SDK-SDK direkt, um ein Profil-Manager-Objekt mithilfe der **wmkreateprofilemanager** -Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="08d5c-110">Erstellen Sie als nächstes das Profil, und übergeben Sie es mithilfe der [**iconfigasfwriter:: konfigurifisingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) -Methode an den [WM-ASF-Writer](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="08d5c-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="08d5c-111">Dies ist die einzige Möglichkeit, den Filter mit einem Profil zu konfigurieren, das die Codecs Windows Media Audio und der Video 9-Serie verwendet.</span><span class="sxs-lookup"><span data-stu-id="08d5c-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="08d5c-112">System Profile für frühere Versionen dieser Codecs können mithilfe der [**iconfigasfwriter:: Konfigurations refilterusingprofileguid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) -Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="08d5c-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="08d5c-113">Sie können das Profil zurücksetzen, während die Eingabe Pins des Filters verbunden sind, solange das neue Profil keine zusätzlichen Eingabe Pins erfordert.</span><span class="sxs-lookup"><span data-stu-id="08d5c-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="08d5c-114">Wenn Sie z. b. das Profil aus einem reinen reinen Audioprofil in ein zweidimensionales Audio-und Video Profil ändern, wird nur die audiopin wieder hergestellt, und es wird keine neue PIN für den Videostream erstellt.</span><span class="sxs-lookup"><span data-stu-id="08d5c-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="08d5c-115">Hinzufügen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="08d5c-115">Adding Metadata</span></span>

<span data-ttu-id="08d5c-116">Fragen Sie zum Hinzufügen von Metadaten zu einer Datei den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter für die **iwmheaderinfo** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="08d5c-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="08d5c-117">Nachdem dem Filter ein Profil zugewiesen wurde, verwenden Sie die **iwmheaderinfo** -Schnittstellen Methoden, um die Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="08d5c-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="08d5c-118">Indizieren einer Datei</span><span class="sxs-lookup"><span data-stu-id="08d5c-118">Indexing a File</span></span>

<span data-ttu-id="08d5c-119">Der WM-ASF-Writer erstellt standardmäßig Temporale indizierte Dateien.</span><span class="sxs-lookup"><span data-stu-id="08d5c-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="08d5c-120">Verwenden Sie zum Erstellen einer Frame indizierten Datei die [**iconfigasfwriter:: setindexmode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) -Methode, um die gesamte Indizierung zu deaktivieren, und erstellen Sie dann die Datei.</span><span class="sxs-lookup"><span data-stu-id="08d5c-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="08d5c-121">Verwenden Sie nach Abschluss des Vorgangs das SDK für den Windows Media-Format, um einen Frame basierten Index für die Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="08d5c-122">Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="08d5c-122">Two-Pass Encoding</span></span>

<span data-ttu-id="08d5c-123">Die zwei-Pass-Codierung wird nur auf Windows Media-Codecs der Version 8 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08d5c-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="08d5c-124">Versetzen Sie den WM-ASF-Writer in den Vorverarbeitungs-Modus, indem Sie [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) aufrufen und am \_ configasfwriter \_ param \_ Multipass im *dwparam* -Parameter und **true** im *dwParam1* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="08d5c-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="08d5c-125">Führen Sie dann das Filter Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="08d5c-125">Then run the filter graph.</span></span> <span data-ttu-id="08d5c-126">Wenn alle Vorverarbeitungs Durchläufen abgeschlossen sind (in der Regel wird nur ein Vorverarbeitungs Durchlauf ausgeführt), empfängt die Anwendung ein Ereignis vom Typ " [**\_ Preprocess \_ Complete**](ec-preprocess-complete.md) " vom Filter.</span><span class="sxs-lookup"><span data-stu-id="08d5c-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="08d5c-127">Wenn dieses Ereignis empfangen wird, verwenden Sie [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , um den Streamzeiger auf den Anfang zurückzusetzen, und führen Sie das Filter Diagramm erneut aus.</span><span class="sxs-lookup"><span data-stu-id="08d5c-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="08d5c-128">Nach dem letzten Durchlauf (in der Regel der zweite Durchlauf) empfängt die Anwendung ein [**EC \_ Complete**](ec-complete.md) -Ereignis, um anzugeben, dass der Codierungsprozess abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="08d5c-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="08d5c-129">Wenn ein Vorverarbeitungs Durchlauf abgebrochen wird, bevor das Ereignis für das Ereignis " **EC \_ Preprocess \_ Complete** " empfangen wird, rufen Sie [**IConfigAsfWriter2:: resetmultipassstate**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) auf, um den Filter vor dem Versuch einer anderen Vorverarbeitungs Ausführung zurückzusetzen</span><span class="sxs-lookup"><span data-stu-id="08d5c-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="08d5c-130">Es ist nur erforderlich, den Parameter "am \_ configasfwriter \_ param Multipass" auf "false" festzulegen \_ , wenn Sie den Filter vollständig aus dem Vorverarbeitungs Modus setzen möchten. </span><span class="sxs-lookup"><span data-stu-id="08d5c-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08d5c-131">Es ist Aufgabe der Anwendung, den Vorverarbeitungs Modus basierend auf dem Profil zu aktivieren, das für die Codierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08d5c-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="08d5c-132">Für einige Profile ist die zwei-Pass-Codierung erforderlich. Wenn Sie versuchen, eine Datei mit einem solchen Profil zu codieren, und am \_ configasfwriter \_ param \_ Multipass nicht auf **true** festgelegt ist, führt dies zu einem Fehler vom Typ " [**\_ userabort**](ec-userabort.md) ".</span><span class="sxs-lookup"><span data-stu-id="08d5c-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="08d5c-133">Weitere Informationen finden Sie in der Dokumentation zum Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="08d5c-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="08d5c-134">Erhalten und Festlegen von Puffer Eigenschaften zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="08d5c-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="08d5c-135">In einigen Szenarien, z. b. Wenn Sie die Tastenkombination beim Schreiben einer Datei erzwingen möchten, muss eine Anwendung möglicherweise Informationen zu einem Windows-Medien Puffer zur Laufzeit erhalten oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="08d5c-136">Die Filter " [WM ASF Reader](wm-asf-reader-filter.md) " und " [WM ASF Writer](wm-asf-writer-filter.md) " unterstützen beide einen Rückrufmechanismus, mit dem eine Anwendung beim Lesen oder Schreiben von Dateien auf die **INSSBuffer3** -Schnittstelle auf jedem einzelnen Medien Puffer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="08d5c-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="08d5c-137">Anwendungen können diese Schnittstelle verwenden, um bestimmte Beispiele als Keyframes festzulegen, SMPTE-Zeit Codes festzulegen, damit-Einstellungen anzugeben oder einen beliebigen Typ privater Daten einem Stream hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="08d5c-138">Verwenden Sie die [**iamwmbufferpass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) -Schnittstelle, um Rückrufe von der PIN zu registrieren, die den Videostream verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="08d5c-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="08d5c-139">Mit der PIN wird die [**iamwmbufferpasscallback:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) -Methode für jeden Puffer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="08d5c-140">Nicht quadratische Pixel</span><span class="sxs-lookup"><span data-stu-id="08d5c-140">Non-Square Pixels</span></span>

<span data-ttu-id="08d5c-141">Der WM-ASF-Writer stellt eine Verbindung mit einem upstreamfilter her, z. b. dem DV-Decoder, der Informationen zum Pixel Seitenverhältnis ausgibt</span><span class="sxs-lookup"><span data-stu-id="08d5c-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="08d5c-142">Der WM-ASF-Writer schreibt diese Informationen als Dateneinheiten Erweiterungen für jedes Beispiel in der Datei.</span><span class="sxs-lookup"><span data-stu-id="08d5c-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="08d5c-143">Wenn der WM-ASF-Reader Pixel-Seitenverhältnis Informationen im Dateiheader oder in Dateneinheiten Erweiterungen für die Beispiele findet, bietet er ein [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format als erste Wahl in der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="08d5c-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="08d5c-144">Die Member **dwpictaspectratiox** und **dwpictaspectratioy** der Struktur, die das Seitenverhältnis des Video Rechtecks beschreiben, werden richtig angepasst, um das Pixel Seitenverhältnis zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="08d5c-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="08d5c-145">Beibehalten des interschnür Formats</span><span class="sxs-lookup"><span data-stu-id="08d5c-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="08d5c-146">Wenn Sie in einem Fernsehgerät oder einer DV-Kamera Zeilen Sprung Video aufzeichnen, sollten Sie das Originalvideo als unabhängige Felder aufbewahren, wenn Sie davon ausgehen, dass die codierte Datei in einem Fernsehgerät oder einem anderen Zeilen Sprung Gerät wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="08d5c-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="08d5c-147">(Computer Monitore sind progressiv-Scangeräte.) Wenn Sie ein Video deinstalften und dann für die Wiedergabe in einem Fernsehgerät wiederherstellen, entstehen Datenverluste.</span><span class="sxs-lookup"><span data-stu-id="08d5c-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="08d5c-148">In einer ASF-Datei werden Zeilen Sprung-Informationen als Dateneinheiten Erweiterungen gespeichert, die die Anwendung auf die einzelnen Beispiele anwendet, indem die zuvor beschriebene [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08d5c-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="08d5c-149">Führen Sie die folgenden Schritte aus, um eine Datei zu codieren, die die ursprünglichen damit-Einstellungen beibehält:</span><span class="sxs-lookup"><span data-stu-id="08d5c-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="08d5c-150">Implementieren Sie eine Klasse, die **iamwmbufferpasscallback** unterstützt, und schreiben Sie eine Benachrichtigungsfunktion, die die damit-Flags für die einzelnen Stichproben festlegt.</span><span class="sxs-lookup"><span data-stu-id="08d5c-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="08d5c-151">Diese Funktion wird vom WM-ASF-Writer aufgerufen, bevor die einzelnen Beispiele verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="08d5c-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="08d5c-152">Legen Sie die dateneinheits Erweiterungen für das Profil fest, bevor Sie das Profil an den Filter übergeben.</span><span class="sxs-lookup"><span data-stu-id="08d5c-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="08d5c-153">Nachdem Sie den Filter mit dem Profil konfiguriert haben, rufen Sie die **IWMWriterAdvanced2** -Schnittstelle vom WM-ASF-Writer ab, und rufen Sie **die Methode "** die Methode".</span><span class="sxs-lookup"><span data-stu-id="08d5c-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
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

    

## <a name="related-topics"></a><span data-ttu-id="08d5c-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08d5c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d5c-155">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="08d5c-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



