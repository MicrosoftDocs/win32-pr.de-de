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
# <a name="sami-cc-parser-filter"></a>SAMI-Parserfilter (CC)

Analysiert Untertiteldaten aus SAMI-Dateien (Synchronized Accessible Media Interchange).

SAMI ist ein Textformat, das HTML ähnelt und zum Codieren zeitbasierter Beschriftungen verwendet wird. Dieser Filter konvertiert SAMI-Daten in einen Textstream. Jedes Beispiel im Stream enthält einen Beschriftungseintrag sowie Formatinformationen. Die Zeitstempel für die Beispiele werden aus den Zeitinformationen in der SAMI-Datei generiert.

Dieser Filter ist für die Verwendung mit dem Filter ["Interner Skriptbefehlsrenderer"](internal-script-command-renderer-filter.md) konzipiert. Der Renderer für interne Skriptbefehle empfängt die Textbeispiele und sendet sie in Form von Ereignisbenachrichtigungen an die Anwendung. Weitere Informationen finden Sie im Abschnitt "Hinweise".



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Eingabe-Stecknadelmedientypen                    | \_MEDIATYPE-Stream                                                                                        |
| Eingabe-Pin-Schnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Text, MEDIASUBTYPE \_ NULL                                                                      |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                         |
| Ausführbare Datei                               | quartz.dll                                                                                               |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                          |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Im Folgenden finden Sie eine einfache SAMI-Datei:


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



Das **STYLE-Tag** definiert zwei Spracheinstellungen: Englisch (. ENCC) und Französisch (. FRCC). Außerdem werden zwei Stile definiert: \# NORMAL und \# GREENTEXT. Jedes **SYNC-Tag** definiert die Startzeit für eine Beschriftung in Millisekunden. Die **P-Tags** enthalten den Beschriftungstext, während das **CLASS-Attribut** die Spracheinstellung angibt, auf die die Beschriftung angewendet wird.

Für jede Sprache und jeden Stil erstellt der Filter einen logischen Stream. Zu jedem Zeitpunkt sind genau ein Sprachstream und ein Stilstream aktiviert. Wenn der Filter ein Beispiel generiert, wählt er die Beschriftung für die aktuelle Sprache aus und wendet den aktuellen Stil an. Standardmäßig sind die erste Sprache und der erste Stil, die in der Datei deklariert sind, aktiviert. Eine Anwendung kann die [**IAMStreamSelect::Enable-Methode verwenden,**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) um einen anderen Stream zu aktivieren.

Mit den Standardeinstellungen erzeugt die erste Beschriftung in der Beispieldatei die folgende Ausgabe:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Wenn die Ausgabe an den Renderer des internen Skriptbefehls gesendet wird, sendet dieser Filter eine [**EC \_ OLE \_ EVENT-Ereignisbenachrichtigung.**](ec-ole-event.md) Der zweite Ereignisparameter ist ein BSTR mit dem Beschriftungstext. Die Anwendung kann das Ereignis abrufen und die Beschriftung anzeigen.

Das folgende Beispiel zeigt, wie sie eine SAMI-Datei rendern, Datenstrominformationen abrufen, Streams aktivieren und Beschriftungstext anzeigen. Im Beispiel wird davon ausgegangen, dass die vorherige SAMI-Datei als C: \\ Sami \_ test \_ file.sami gespeichert wird.

Aus Gründen der Übersichtlichkeit wurden in diesem Beispiel hart codierte Streamindizes verwendet, wenn die **IAMStreamSelect::Enable-Methode** aufruft. Außerdem wird eine minimale Fehlerüberprüfung durchgeführt.


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



Dieser Filter verwendet die [**IAsyncReader-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) um Beispiele aus dem Quellfilter zu pullen. Daher wird die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) auf dem Eingabepin nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



