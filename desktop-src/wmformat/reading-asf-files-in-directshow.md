---
title: Lesen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)
description: Die Wiedergabe von ASF-Dateien wird vom WM ASF-Readerfilter verarbeitet. Erfahren Sie mehr über das Lesen von ASF-Dateien in DirectShow im Windows Media Format 11 SDK.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Lesen von ASF-Dateien
- Windows Media Format SDK, WM ASF-Readerfilter
- Windows Media Format SDK, IMediaSeeking-Schnittstelle
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Advanced Systems Format (ASF), WM ASF-Readerfilter
- ASF (Advanced Systems Format), WM ASF-Readerfilter
- Advanced Systems Format (ASF), IMediaSeeking-Schnittstelle
- ASF (Advanced Systems Format), IMediaSeeking-Schnittstelle
- DirectShow,Lesen von ASF-Dateien
- Filter "DirectShow", "WM ASF Reader"
- DirectShow,IMediaSeeking-Schnittstelle
- WM ASF-Readerfilter
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404323"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lesen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)

Die Wiedergabe von ASF-Dateien wird vom [WM ASF-Readerfilter](wm-asf-reader-filter.md) verarbeitet. Wenn der WM ASF-Reader eine Datei liest, erstellt er automatisch einen Ausgabepin für jeden Stream, einschließlich Webstreams, Skriptbefehlsstreams und jeder anderen Art von beliebigem Stream. Bei Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt.

Der WM ASF-Reader unterstützt die DirectShow **IMediaSeeking-Schnittstelle,** mit der Anwendungen temporale Suchmöglichkeiten innerhalb der Datei ausführen können. Die Wiedergabe mit anderen Geschwindigkeiten als 1.0 (wie in **IMediaSeeking::SetRate** angegeben) wird jedoch nicht unterstützt.

Der Filter macht auch mehrere Windows Media Format SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben.



| Schnittstelle                                        | Verfügbar gemacht                            | Kommentare                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Über **IServiceProvider** für Filter | Wird für Anwendungen bereitgestellt, die Inhalte wieder geben müssen, die durch Digital Rights Management (DRM) geschützt sind. Diese Schnittstelle kann auch verwendet werden, um andere Schnittstellen für das Readerobjekt direkt zu erhalten. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface für** Filter           | Wird bereitgestellt, damit Anwendungen Datei- und Inhaltsattribute sowie Marker- und Skriptinformationen und Metadaten lesen können.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface für** Filter           | Teilweise im Filter implementiert, sodass Anwendungen auf die Informationsmethoden im WM-Reader-Objekt zugreifen können.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface für** Filter           | Teilweise im Filter implementiert, sodass Anwendungen auf die Informationsmethoden des Readerobjekts zugreifen können.                                                                         |



 

Der [WM ASF-Readerfilter](wm-asf-reader-filter.md) wurde erstmals in DirectShow 8.0 verfügbar gemacht. Die version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7. *x* des Windows Media Format SDK. Die neueste Version des Filters wird zusammen mit den anderen QASF-Komponenten im Windows Media Format 9 Series SDK und in späteren Versionen bereitgestellt und unterstützt es und ersetzt den Filter in DirectX 9.0. Wenn Sie das Windows Media Format SDK nach der Installation von DirectX 8 installieren. *x* oder 9. *x* SDK: Sie überschreiben die DirectX-Version qasf.dll Version der 9er Serie. Dies sollte keine Probleme verursachen, außer möglicherweise in einem Szenario, in dem es zu einem anderen Verhalten in der DirectShow **IGraphBuilder::RenderFile-Methode** führt. Die SDK-Version des Windows Media Format 9 Series des WM ASF-Readers ist der Standardquellenfilter für die Erweiterungen ASF, WMV und WMA. Dies bedeutet, dass der WM ASF-Reader automatisch erstellt und dem Filterdiagramm durch den Filtergraph-Manager in Methoden wie **IGraphBuilder::RenderFile** oder **IGraphBuilder::AddSourceFilter** hinzugefügt wird, wenn eine Datei dieses Typs angegeben wird. In DirectX 9.0 und früher und Windows XP Service Pack 1 und früher verwendet die **RenderFile-Methode** den älteren Windows Media Source Filter. Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6.4 verwendet haben. Weitere Informationen zum älteren Windows Media Source-Filter finden Sie in der DirectShow SDK-Dokumentation.

Um eine ASF-Datei mit Windows Media-basiertem Inhalt mithilfe des WM ASF-Readers wiederderherzustellen, müssen Sie in den drei Hauptschritten eine Instanz des Filterdiagramm-Managers erstellen, **IGraphBuilder::RenderFile** aufrufen, um das Diagramm zu erstellen, und dann **IMediaControl::Run** aufrufen, um die Datei wieder zu spielen. Das folgende Codebeispiel ist ein vollständiges Programm, das eine ASF-Datei mit DirectShow wieder gibt. Um dieses Beispiel ausführen zu können, muss das DirectX SDK installiert sein, und Ihre Buildumgebung muss gemäß den Anweisungen im DirectShow SDK-Dokumentationsthema "Einrichten der Buildumgebung" konfiguriert sein. Außerdem müssen Sie im Aufruf von RenderFile eine Datei auf Ihrem **Computer angeben.**


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



Beachten Sie, dass der Anwendungscode für dieses einfache Beispiel nie speziell auf den WM ASF-Reader verweist. Dieser Filter wird vom Filterdiagramm-Manager erstellt, verbunden, ausgeführt und schließlich freigegeben. In vielen Szenarien sollten Sie jedoch den WM ASF-Reader konfigurieren, bevor Sie mit der Wiedergabe beginnen.

 

 




