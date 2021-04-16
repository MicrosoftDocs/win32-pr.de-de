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
# <a name="sami-cc-parser-filter"></a>Sami (CC)-Parserfilter

Analysiert Untertitel Daten aus synchronisierten, zugänglichen Medienaustausch Dateien (Sami).

Sami ist ein Textformat, das HTML ähnelt, und wird zum Codieren zeitbasierter Beschriftungen verwendet. Dieser Filter konvertiert Sami-Daten in einen Textstream. Jede Stichprobe im Stream enthält einen Beschriftungs Eintrag und Formatierungsinformationen. Die Zeitstempel der Stichproben werden aus den Zeit Informationen in der Sami-Datei generiert.

Dieser Filter ist für die Verwendung mit dem [internen rendererfilter für Skript Befehle](internal-script-command-renderer-filter.md) vorgesehen. Der Renderer des internen Skript Befehls empfängt die Textbeispiele und sendet Sie in Form von Ereignis Benachrichtigungen an die Anwendung. Weitere Informationen finden Sie im Abschnitt "Hinweise".



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Stream                                                                                        |
| PIN-Eingabeschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Ausgabe-PIN-Medientypen                   | MediaType \_ Text, mediasubtype \_ null                                                                      |
| PIN-Schnittstellen                    | [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | {33fakfe0-a9be-11D0-A520-00a0d10129c0}                                                                   |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                         |
| Ausführbare Datei                               | quartz.dll                                                                                               |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                          |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie eine einfache Sami-Datei:


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



Das **styletag** definiert zwei Spracheinstellungen: Englisch (. UMCC) und Französisch (. Frcc). Außerdem werden zwei Stile definiert: \# Normal und \# greentext. Jedes **synchronisierungstag** definiert die Startzeit für eine Beschriftung in Millisekunden. Die **P** -Tags enthalten den Beschriftungs Text, während das **Class** -Attribut die Spracheinstellung angibt, auf die die Beschriftung angewendet wird.

Für jede Sprache und jeden Stil erstellt der Filter einen logischen Datenstrom. Zu jedem Zeitpunkt sind genau ein sprach Datenstrom und ein stilstream aktiviert. Wenn der Filter ein Beispiel generiert, wird die Beschriftung für die aktuelle Sprache ausgewählt und der aktuelle Stil angewendet. Standardmäßig sind die in der Datei deklarierte erste Sprache und der in der Datei deklarierte Stil aktiviert. Eine Anwendung kann die [**iamstreamselect:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) -Methode verwenden, um einen anderen Stream zu aktivieren.

Mit den Standardeinstellungen erzeugt die erste Beschriftung in der Beispieldatei die folgende Ausgabe:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Wenn die Ausgabe an den internen Renderer des Skript Befehls weitergeleitet wird, sendet dieser Filter eine Ereignis Benachrichtigung für das [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) . Der zweite Ereignis Parameter ist ein BSTR mit dem Beschriftungs Text. Die Anwendung kann das Ereignis abrufen und die Beschriftung anzeigen.

Im folgenden Beispiel wird gezeigt, wie Sie eine Sami-Datei, Datenstrom Informationen, streamingdatenströme und Beschriftungs Text Rendering darstellen. Im Beispiel wird davon ausgegangen, dass die vorherige samische Datei als C: \\ Sami \_ Test \_ file. Sami gespeichert wird.

Aus Gründen der Kürze wurden in diesem Beispiel hart codierte streamindizes verwendet, wenn die **iamstreamselect:: enable** -Methode aufgerufen wird. Außerdem führt es eine minimale Fehlerüberprüfung durch.


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



Dieser Filter verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle zum Abrufen von Beispielen aus dem Quell Filter. Daher wird die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle in der eingabepin nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



