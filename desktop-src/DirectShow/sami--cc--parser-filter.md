---
description: Sami (CC)-Parserfilter
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Sami (CC)-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522040"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="ed22a-103">Sami (CC)-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="ed22a-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="ed22a-104">Analysiert Untertitel Daten aus synchronisierten, zugänglichen Medienaustausch Dateien (Sami).</span><span class="sxs-lookup"><span data-stu-id="ed22a-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="ed22a-105">Sami ist ein Textformat, das HTML ähnelt, und wird zum Codieren zeitbasierter Beschriftungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed22a-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="ed22a-106">Dieser Filter konvertiert Sami-Daten in einen Textstream.</span><span class="sxs-lookup"><span data-stu-id="ed22a-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="ed22a-107">Jede Stichprobe im Stream enthält einen Beschriftungs Eintrag und Formatierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="ed22a-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="ed22a-108">Die Zeitstempel der Stichproben werden aus den Zeit Informationen in der Sami-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="ed22a-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="ed22a-109">Dieser Filter ist für die Verwendung mit dem [internen rendererfilter für Skript Befehle](internal-script-command-renderer-filter.md) vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ed22a-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="ed22a-110">Der Renderer des internen Skript Befehls empfängt die Textbeispiele und sendet Sie in Form von Ereignis Benachrichtigungen an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ed22a-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="ed22a-111">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ed22a-111">For more information, see the Remarks section.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed22a-112">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed22a-112">Filter Interfaces</span></span>                        | <span data-ttu-id="ed22a-113">[**Iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="ed22a-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="ed22a-114">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="ed22a-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="ed22a-115">MediaType- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="ed22a-115">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="ed22a-116">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed22a-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ed22a-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ed22a-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="ed22a-118">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="ed22a-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="ed22a-119">MediaType \_ Text, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="ed22a-119">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="ed22a-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed22a-120">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ed22a-121">[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ed22a-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="ed22a-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="ed22a-122">Filter CLSID</span></span>                             | <span data-ttu-id="ed22a-123">{33fakfe0-a9be-11D0-A520-00a0d10129c0}</span><span class="sxs-lookup"><span data-stu-id="ed22a-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="ed22a-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="ed22a-124">Property Page CLSID</span></span>                      | <span data-ttu-id="ed22a-125">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="ed22a-125">No property page</span></span>                                                                                         |
| <span data-ttu-id="ed22a-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="ed22a-126">Executable</span></span>                               | <span data-ttu-id="ed22a-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="ed22a-127">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="ed22a-128">Verdienst</span><span class="sxs-lookup"><span data-stu-id="ed22a-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="ed22a-129">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="ed22a-129">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="ed22a-130">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="ed22a-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ed22a-131">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="ed22a-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ed22a-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed22a-132">Remarks</span></span>

<span data-ttu-id="ed22a-133">Im folgenden finden Sie eine einfache Sami-Datei:</span><span class="sxs-lookup"><span data-stu-id="ed22a-133">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="ed22a-134">Das **styletag** definiert zwei Spracheinstellungen: Englisch (. UMCC) und Französisch (. Frcc).</span><span class="sxs-lookup"><span data-stu-id="ed22a-134">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="ed22a-135">Außerdem werden zwei Stile definiert: \# Normal und \# greentext.</span><span class="sxs-lookup"><span data-stu-id="ed22a-135">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="ed22a-136">Jedes **synchronisierungstag** definiert die Startzeit für eine Beschriftung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ed22a-136">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="ed22a-137">Die **P** -Tags enthalten den Beschriftungs Text, während das **Class** -Attribut die Spracheinstellung angibt, auf die die Beschriftung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed22a-137">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="ed22a-138">Für jede Sprache und jeden Stil erstellt der Filter einen logischen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="ed22a-138">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="ed22a-139">Zu jedem Zeitpunkt sind genau ein sprach Datenstrom und ein stilstream aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed22a-139">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="ed22a-140">Wenn der Filter ein Beispiel generiert, wird die Beschriftung für die aktuelle Sprache ausgewählt und der aktuelle Stil angewendet.</span><span class="sxs-lookup"><span data-stu-id="ed22a-140">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="ed22a-141">Standardmäßig sind die in der Datei deklarierte erste Sprache und der in der Datei deklarierte Stil aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed22a-141">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="ed22a-142">Eine Anwendung kann die [**iamstreamselect:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) -Methode verwenden, um einen anderen Stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ed22a-142">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="ed22a-143">Mit den Standardeinstellungen erzeugt die erste Beschriftung in der Beispieldatei die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="ed22a-143">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="ed22a-144">Wenn die Ausgabe an den internen Renderer des Skript Befehls weitergeleitet wird, sendet dieser Filter eine Ereignis Benachrichtigung für das [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="ed22a-144">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="ed22a-145">Der zweite Ereignis Parameter ist ein BSTR mit dem Beschriftungs Text.</span><span class="sxs-lookup"><span data-stu-id="ed22a-145">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="ed22a-146">Die Anwendung kann das Ereignis abrufen und die Beschriftung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ed22a-146">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="ed22a-147">Im folgenden Beispiel wird gezeigt, wie Sie eine Sami-Datei, Datenstrom Informationen, streamingdatenströme und Beschriftungs Text Rendering darstellen.</span><span class="sxs-lookup"><span data-stu-id="ed22a-147">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="ed22a-148">Im Beispiel wird davon ausgegangen, dass die vorherige samische Datei als C: \\ Sami \_ Test \_ file. Sami gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="ed22a-148">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="ed22a-149">Aus Gründen der Kürze wurden in diesem Beispiel hart codierte streamindizes verwendet, wenn die **iamstreamselect:: enable** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed22a-149">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="ed22a-150">Außerdem führt es eine minimale Fehlerüberprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="ed22a-150">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="ed22a-151">Dieser Filter verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle zum Abrufen von Beispielen aus dem Quell Filter.</span><span class="sxs-lookup"><span data-stu-id="ed22a-151">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="ed22a-152">Daher wird die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle in der eingabepin nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed22a-152">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed22a-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed22a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed22a-154">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="ed22a-154">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



