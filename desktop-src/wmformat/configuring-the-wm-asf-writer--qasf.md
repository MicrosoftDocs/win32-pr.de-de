---
title: Konfigurieren von WM ASF Writer (qasf)
description: Konfigurieren von WM ASF Writer (qasf)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media-Format-SDK, Konfigurieren von WM-ASF-Writer (qasf)
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, WM-ASF-Writer
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), Konfigurieren von WM ASF Writer (qasf)
- ASF (Advanced Systems Format), Konfigurieren von WM ASF Writer (qasf)
- Advanced Systems Format (ASF), WM-ASF-Writer
- ASF (Advanced Systems Format), WM-ASF-Writer
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, Konfigurieren von WM-ASF-Writer (qasf)
- DirectShow, WM-ASF-Writer
- DirectShow, qasf
- WM-ASF-Writer, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102147"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="a7563-119">Konfigurieren von WM ASF Writer (qasf)</span><span class="sxs-lookup"><span data-stu-id="a7563-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="a7563-120">Wenn der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter erstellt wird, wird er automatisch mit dem wmprofile \_ V80 256- \_ Video Profil als Standard konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a7563-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="a7563-121">Da für dieses Profil die Codecs Windows Media Audio und Windows Media Video Version 8 verwendet werden, empfiehlt es sich, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und dann seinen [**iwmprofile**](iwmprofile.md) -Zeiger mithilfe der [**iconfigasfwriter::**](iconfigasfwriter-configurefilterusingprofile.md) Configuration Report profile-Methode an den Filter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a7563-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="a7563-122">Der Filter muss dem Diagramm hinzugefügt werden, bevor der Filter konfiguriert werden kann, und er muss konfiguriert werden, bevor er mit upstreamfiltern verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7563-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="a7563-123">Der Filter verwendet das Profil, um zu bestimmen, welche Art von Windows Media-Format Datei geschrieben werden soll, wie viele Eingabe Pins eingerichtet werden und welche Medientypen von den Pins akzeptiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a7563-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="a7563-124">Der Filter ermöglicht das Zurücksetzen von Profilen, während die Eingabe Pins verbunden sind, solange das neue Profil keine zusätzlichen Eingabe Pins erfordert.</span><span class="sxs-lookup"><span data-stu-id="a7563-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="a7563-125">Wenn Sie z. b. das Profil aus einem reinen Audioprofil in ein zweidimensionales Audio-und Video Profil ändern, muss nur die audiopin mit einem Zeitstempel versehen werden, und alle Eingabe Pins müssen verbunden sein, bevor der Filter ausgeführt oder angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7563-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="a7563-126">Dies bedeutet Folgendes: Wenn Sie den Filter mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter eine Audioeingabe-PIN und eine Videoeingabe-PIN. beide Pins müssen miteinander verbunden sein, bevor der Filter ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7563-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="a7563-127">Hinzufügen von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a7563-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="a7563-128">Sie können einen profilstream für dateneinheits Erweiterungen konfigurieren, wie z. b. SMPTE-Zeit Codes, entweder vor oder nach dem Verbinden des Filters, solange Sie dieser Reihenfolge von Vorgängen folgen:</span><span class="sxs-lookup"><span data-stu-id="a7563-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="a7563-129">Fügen Sie dem Stream mithilfe von [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)eine oder mehrere Dateneinheiten Erweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7563-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="a7563-130">[**Wmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) zum Aktualisieren des Profils aufruft.</span><span class="sxs-lookup"><span data-stu-id="a7563-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="a7563-131">Nennen Sie [**iconfigasfwriter:: konfigurierfilterusingprofile**](iconfigasfwriter-configurefilterusingprofile.md) mit dem aktualisierten Profil Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7563-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="a7563-132">Suchen Sie die Videoeingabe-PIN, und wenden Sie Ihre [**iamwmbufferpass:: setnotify**](iamwmbufferpass-setnotify.md) -Methode an, um Ihre Anwendungs definierte [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="a7563-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="a7563-133">Wenn das Diagramm ausgeführt wird, wird die [**iamwmbufferpasscallback:: notify**](iamwmbufferpasscallback-notify.md) -Methode für jeden Frame aufgerufen, und Sie können Eigenschaften für das Beispiel mithilfe der [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstellen Methoden erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="a7563-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="a7563-134">In einigen Prozessor intensiven Szenarien wie z. b. Inverse Telecine benötigt der WM-ASF-Writer möglicherweise mehr Ausgabepuffer, als von einigen downstreamfiltern unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7563-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="a7563-135">Der DV-Decoder nimmt z. b. für die Ausgabepin nicht mehr als einen Puffer an, und dasselbe gilt für den AVI-Dekompressor unter bestimmten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="a7563-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="a7563-136">Wenn beim Versuch, eine Verbindung mit diesen Filtern herzustellen, oder möglicherweise beim Ausführen des Diagramms Probleme auftreten, kann es erforderlich sein, einen Vermittler Filter zu schreiben, der eine beliebige Anzahl von Puffern in der Ausgabe-PIN akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a7563-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 