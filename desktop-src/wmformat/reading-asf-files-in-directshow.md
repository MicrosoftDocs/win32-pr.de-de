---
title: Lesen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)
description: Lesen von ASF-Dateien in DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Lesen von ASF-Dateien
- Windows Media-Format-SDK, WM-ASF-Reader-Filter
- Windows Media-Format-SDK, imediaseeking-Schnittstelle
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Advanced Systems Format (ASF), WM-ASF-Lesefilter
- ASF (Advanced Systems Format), WM-ASF-Lesefilter
- Advanced Systems Format (ASF), imediaseeking-Schnittstelle
- ASF (Advanced Systems Format), imediaseeking-Schnittstelle
- DirectShow, Lesen von ASF-Dateien
- DirectShow, WM-ASF-Reader-Filter
- DirectShow, imediaseeking-Schnittstelle
- WM-ASF-Lesefilter
- Imediaseeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340147"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lesen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)

Die Wiedergabe von ASF-Dateien wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter behandelt. Wenn der WM-ASF-Reader eine Datei liest, erstellt er automatisch eine Ausgabe-PIN für jeden Stream, einschließlich Webstreams, Skript befehlsstreams und beliebiger anderer Typen von beliebigem Stream. Im Fall von Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt.

Der WM-ASF-Reader unterstützt die Schnittstelle DirectShow **imediaseeking** , mit der Anwendungen eine temporale Suche innerhalb der Datei durchführen können. Die Wiedergabe mit einer anderen Geschwindigkeit als 1,0 (wie in **imediaseeking::*** angegeben) wird jedoch nicht unterstützt.

Der Filter macht auch mehrere Windows Media-Format-SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben.



| Schnittstelle                                        | Verfügbar gemacht                            | Kommentare                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Über **IServiceProvider** beim Filter | Wird für Anwendungen bereitgestellt, die durch Digital Rights Management (DRM) geschützte Inhalte wiedergeben müssen. Diese Schnittstelle kann auch verwendet werden, um andere Schnittstellen des Reader-Objekts direkt abzurufen. |
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** bei Filter           | Bereitgestellt, damit Anwendungen Datei-und Inhalts Attribute sowie Marker-und Skriptinformationen sowie Metadaten lesen können.                                                                  |
| [**Iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** bei Filter           | Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des WM-Reader-Objekts zugreifen können.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** bei Filter           | Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des Reader-Objekts zugreifen können.                                                                         |



 

Der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter wurde zuerst in DirectShow 8,0 verfügbar gemacht. Die Version des Filters, die im Lieferumfang von DirectShow 8,1 und 9,0 enthalten ist, unterstützt Version 7. *x* des SDK für den Windows Media-Format. Die neueste Version des Filters, zusammen mit den anderen qasf-Komponenten, ist im Lieferumfang des SDK der Windows Media-Serie 9 und höher enthalten und unterstützt das Windows Media-Format der Serie 9 und höhere Versionen und ersetzt den Filter in DirectX 9,0. Wenn Sie das Windows Media-Format-SDK nach der Installation von DirectX 8 installieren. *x* oder 9. *x* SDK: Sie überschreiben die DirectX-Version von qasf.dll mit der Version 9 der Serie. Dies sollte keine Probleme darstellen, außer möglicherweise in einem Szenario, in dem es zu einem anderen Verhalten in der DirectShow **igraphbuilder:: RenderFile** -Methode führt. Die SDK-Version des Windows Media Format 9-Formats des WM-ASF-Readers ist der Standard Quell Filter für die Dateinamen Erweiterungen ". ASF", ". wmv" und ". wma". Dies bedeutet, dass der WM-ASF-Reader vom Filter Graph-Manager in Methoden wie **igraphbuilder:: RenderFile** oder **igraphbuilder:: addsourcefilter** automatisch erstellt und dem Filter Diagramm hinzugefügt wird, wenn eine Datei dieses Typs angegeben wird. In DirectX 9,0 und früheren Versionen und Windows XP Service Pack 1 und früher verwendet die **RenderFile** -Methode den älteren Windows Media-Quell Filter. Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6,4 verwendet haben. Weitere Informationen zum Legacy-Windows Media-Quell Filter finden Sie in der DirectShow SDK-Dokumentation.

Um eine ASF-Datei mit Windows Media – basierten Inhalt mithilfe des WM-ASF-Readers wiederzugeben, müssen Sie zunächst eine Instanz des Filter Graph-Managers erstellen, **igraphbuilder:: RenderFile** zum Erstellen des Diagramms und dann **IMediaControl:: Run** zum Wiedergeben der Datei abrufen. Das folgende Codebeispiel ist ein umfassendes Programm, das eine ASF-Datei mithilfe von DirectShow wieder gibt. Zum Ausführen dieses Beispiels müssen Sie das DirectX SDK installiert haben, und ihre Buildumgebung muss gemäß den Anweisungen im DirectShow SDK-Dokumentations Thema "Einrichten der Buildumgebung" konfiguriert werden. Außerdem müssen Sie im **RenderFile**-aufruppenbefehl eine Datei auf Ihrem Computer angeben.


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



Beachten Sie, dass der Anwendungscode für dieses einfache Beispiel nie auf den WM-ASF-Reader verweist. Dieser Filter wird erstellt, verbunden, ausgeführt und schließlich vom Filter Graph-Manager freigegeben. In vielen Szenarien empfiehlt es sich jedoch, den WM-ASF-Reader vor der Wiedergabe zu konfigurieren.

 

 




