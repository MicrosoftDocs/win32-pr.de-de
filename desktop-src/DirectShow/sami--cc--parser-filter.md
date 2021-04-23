---
description: SAMI-Parserfilter (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: SAMI-Parserfilter (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909678"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="39de6-103">SAMI-Parserfilter (CC)</span><span class="sxs-lookup"><span data-stu-id="39de6-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="39de6-104">Analysiert Untertiteldaten aus SAMI-Dateien (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="39de6-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="39de6-105">SAMI ist ein Textformat, das HTML ähnelt und zum Codieren zeitbasierter Beschriftungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39de6-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="39de6-106">Dieser Filter konvertiert SAMI-Daten in einen Textstream.</span><span class="sxs-lookup"><span data-stu-id="39de6-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="39de6-107">Jedes Beispiel im Stream enthält einen Beschriftungseintrag sowie Formatinformationen.</span><span class="sxs-lookup"><span data-stu-id="39de6-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="39de6-108">Die Zeitstempel für die Beispiele werden aus den Zeitinformationen in der SAMI-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="39de6-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="39de6-109">Dieser Filter ist für die Verwendung mit dem Filter ["Interner Skriptbefehlsrenderer"](internal-script-command-renderer-filter.md) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="39de6-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="39de6-110">Der Renderer für interne Skriptbefehle empfängt die Textbeispiele und sendet sie in Form von Ereignisbenachrichtigungen an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="39de6-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="39de6-111">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="39de6-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="39de6-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="39de6-112">Label</span></span> | <span data-ttu-id="39de6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="39de6-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39de6-114">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="39de6-114">Filter Interfaces</span></span>                        | <span data-ttu-id="39de6-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="39de6-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="39de6-116">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="39de6-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="39de6-117">\_MEDIATYPE-Stream</span><span class="sxs-lookup"><span data-stu-id="39de6-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="39de6-118">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="39de6-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="39de6-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="39de6-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="39de6-120">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="39de6-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="39de6-121">MEDIATYPE \_ Text, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="39de6-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="39de6-122">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="39de6-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="39de6-123">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="39de6-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="39de6-124">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="39de6-124">Filter CLSID</span></span>                             | <span data-ttu-id="39de6-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="39de6-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="39de6-126">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="39de6-126">Property Page CLSID</span></span>                      | <span data-ttu-id="39de6-127">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="39de6-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="39de6-128">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="39de6-128">Executable</span></span>                               | <span data-ttu-id="39de6-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="39de6-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="39de6-130">Verdienst</span><span class="sxs-lookup"><span data-stu-id="39de6-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="39de6-131">WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH</span><span class="sxs-lookup"><span data-stu-id="39de6-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="39de6-132">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="39de6-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="39de6-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="39de6-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="39de6-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39de6-134">Remarks</span></span>

<span data-ttu-id="39de6-135">Im Folgenden finden Sie eine einfache SAMI-Datei:</span><span class="sxs-lookup"><span data-stu-id="39de6-135">The following is a simple SAMI file:</span></span>


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



<span data-ttu-id="39de6-136">Das **STYLE-Tag** definiert zwei Spracheinstellungen: Englisch (. ENCC) und Französisch (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="39de6-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="39de6-137">Außerdem werden zwei Stile definiert: \# NORMAL und \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="39de6-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="39de6-138">Jedes **SYNC-Tag** definiert die Startzeit für eine Beschriftung in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="39de6-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="39de6-139">Die **P-Tags** enthalten den Beschriftungstext, während das **CLASS-Attribut** die Spracheinstellung angibt, auf die die Beschriftung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="39de6-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="39de6-140">Für jede Sprache und jeden Stil erstellt der Filter einen logischen Stream.</span><span class="sxs-lookup"><span data-stu-id="39de6-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="39de6-141">Zu jedem Zeitpunkt sind genau ein Sprachstream und ein Stilstream aktiviert.</span><span class="sxs-lookup"><span data-stu-id="39de6-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="39de6-142">Wenn der Filter ein Beispiel generiert, wählt er die Beschriftung für die aktuelle Sprache aus und wendet den aktuellen Stil an.</span><span class="sxs-lookup"><span data-stu-id="39de6-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="39de6-143">Standardmäßig sind die erste Sprache und der erste Stil, die in der Datei deklariert sind, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="39de6-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="39de6-144">Eine Anwendung kann die [**IAMStreamSelect::Enable-Methode verwenden,**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) um einen anderen Stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39de6-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="39de6-145">Mit den Standardeinstellungen erzeugt die erste Beschriftung in der Beispieldatei die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="39de6-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="39de6-146">Wenn die Ausgabe an den Renderer des internen Skriptbefehls gesendet wird, sendet dieser Filter eine [**EC \_ OLE \_ EVENT-Ereignisbenachrichtigung.**](ec-ole-event.md)</span><span class="sxs-lookup"><span data-stu-id="39de6-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="39de6-147">Der zweite Ereignisparameter ist ein BSTR mit dem Beschriftungstext.</span><span class="sxs-lookup"><span data-stu-id="39de6-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="39de6-148">Die Anwendung kann das Ereignis abrufen und die Beschriftung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="39de6-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="39de6-149">Das folgende Beispiel zeigt, wie sie eine SAMI-Datei rendern, Datenstrominformationen abrufen, Streams aktivieren und Beschriftungstext anzeigen.</span><span class="sxs-lookup"><span data-stu-id="39de6-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="39de6-150">Im Beispiel wird davon ausgegangen, dass die vorherige SAMI-Datei als C: \\ Sami \_ test \_ file.sami gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="39de6-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="39de6-151">Aus Gründen der Übersichtlichkeit wurden in diesem Beispiel hart codierte Streamindizes verwendet, wenn die **IAMStreamSelect::Enable-Methode** aufruft.</span><span class="sxs-lookup"><span data-stu-id="39de6-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="39de6-152">Außerdem wird eine minimale Fehlerüberprüfung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="39de6-152">It also performs minimal error checking.</span></span>


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



<span data-ttu-id="39de6-153">Dieser Filter verwendet die [**IAsyncReader-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) um Beispiele aus dem Quellfilter zu pullen.</span><span class="sxs-lookup"><span data-stu-id="39de6-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="39de6-154">Daher wird die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) auf dem Eingabepin nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39de6-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39de6-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39de6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39de6-156">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="39de6-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



