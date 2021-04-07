---
title: So decodieren Sie Audiodaten in S/PDIF
description: So decodieren Sie Audiodaten in S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media-Format-SDK, Decodieren von Audiodaten in S/PDIF
- Windows Media-Format-SDK, digitales Microsoft/Philips Digital Interconnect-Format (S/PDIF)
- Advanced Systems Format (ASF), Decodierung von Audiodaten in S/PDIF
- ASF (Advanced Systems Format), Decodierung von Audiodaten in S/PDIF
- Advanced Systems Format (ASF), digitales, digitales Interconnect-Format (S/PDIF) von Sony/Philips
- ASF (Advanced Systems Format), digitales digitales Interconnect-Format (S/PDIF) von Sony/Philips
- Digitales Interconnect-Format (S/PDIF) für Sony/Philips, Decodierung von Audiodaten
- S/PDIF (Sony/Philips Digital Interconnect-Format), Decodierung von Audiodaten
- Decodieren von Audiodateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724102"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="1049e-112">So decodieren Sie Audiodaten in S/PDIF</span><span class="sxs-lookup"><span data-stu-id="1049e-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="1049e-113">Mit dem Windows Media Audio 9 Professional-Codec codierte Audiodaten können im Digital/Philips Digital Interconnect-Format (S/PDIF) decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="1049e-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="1049e-114">Führen Sie die folgenden Schritte aus, um die S/PDIF-Ausgabe zu generieren:</span><span class="sxs-lookup"><span data-stu-id="1049e-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="1049e-115">Öffnen Sie eine Datei, die einen Windows Media Audio 9 Professional-Stream enthält, indem Sie die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1049e-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="1049e-116">Identifizieren Sie die Ausgabe Nummer des Datenstroms, den Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="1049e-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="1049e-117">Weitere Informationen finden [Sie unter So identifizieren Sie Ausgabe Nummern](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="1049e-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="1049e-118">Aufrufen der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode, um die S/PDIF-Ausgabe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1049e-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="1049e-119">Verwenden Sie \_ für den Einstellungs Namen g wszene ablewmaprospdif Output.</span><span class="sxs-lookup"><span data-stu-id="1049e-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="1049e-120">Der Datentyp ist vom **WMT- \_ Typ \_ bool**. Legen Sie den Wert auf **true** fest, um die S/PDIF-Ausgabe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1049e-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="1049e-121">Rufen Sie die Schnittstelle der Ausgabe Eigenschaften ([**iwmoutputmediaproperties**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) des gewünschten Ausgabeformats ab, indem Sie die [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1049e-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="1049e-122">Weitere Informationen zum Aufzählen von Ausgabeformaten finden Sie unter [Zuweisen von Ausgabeformaten](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="1049e-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="1049e-123">Legen Sie das Ausgabeformat fest, indem Sie die [**iwmreader:: setoutputrequiemethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1049e-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="1049e-124">Übergeben Sie einen Zeiger auf die **iwmoutputmedia-** Oberfläche, die Sie in Schritt 4 abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="1049e-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="1049e-125">Nehmen Sie andere Konfigurationsänderungen vor, und starten Sie die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="1049e-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="1049e-126">Sie können die vorangehenden Schritte auf dem synchronen Reader ausführen, indem Sie die entsprechenden Methoden der [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="1049e-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="1049e-127">Der folgende Beispielcode veranschaulicht, wie Sie einen Audiostream festlegen, um Audiodaten als S/PDIF-Daten auszugeben.</span><span class="sxs-lookup"><span data-stu-id="1049e-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="1049e-128">Diese Funktion setzt voraus, dass eine Datei bereits in den Reader geladen wurde und dass die Ausgabe Nummer identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1049e-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="1049e-129">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1049e-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1049e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1049e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1049e-131">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="1049e-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="1049e-132">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="1049e-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="1049e-133">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1049e-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="1049e-134">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1049e-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="1049e-135">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1049e-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




