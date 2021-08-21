---
description: Wiederspielen einer Datei
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Wiederspielen einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d20a021ec5053746c279598d08117c6b25a5fe6a52946fed56f19eda3cafe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401148"
---
# <a name="how-to-play-a-file"></a>Wiederspielen einer Datei

Dieser Artikel soll Ihnen die Variante der DirectShow-Programmierung bieten. Es stellt eine einfache Konsolenanwendung vor, die eine Audio- oder Videodatei wieder gibt. Das Programm ist nur wenige Zeilen lang, zeigt jedoch einen Teil der Leistung der DirectShow-Programmierung.

Wie im Artikel [Einführung in directShow-Anwendungsprogrammierung](introduction-to-directshow-application-programming.md) beschrieben, führt eine DirectShow-Anwendung immer die gleichen grundlegenden Schritte aus:

1.  Erstellen Sie eine Instanz von [Filter Graph Manager](filter-graph-manager.md).
2.  Verwenden Sie den Filter Graph Manager, um ein Filterdiagramm zu erstellen.
3.  Führen Sie den Graphen aus, sodass Die Daten durch die Filter bewegt werden.

Um den Code in diesem Thema zu kompilieren und zu verknüpfen, fügen Sie die Headerdatei Dshow.h und einen Link zur statischen Bibliotheksdatei strmiids.lib ein. Weitere Informationen finden Sie unter [Erstellen von DirectShow-Anwendungen.](setting-up-the-build-environment.md)

Rufen Sie zunächst [**CoInitialize oder**](/windows/desktop/api/objbase/nf-objbase-coinitialize) [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) auf, um die COM-Bibliothek zu initialisieren:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Um die Dinge einfach zu halten, ignoriert dieses Beispiel den Rückgabewert, aber Sie sollten immer den **HRESULT-Wert** aus jedem Methodenaufruf überprüfen.

Rufen Sie als Nächstes [**CoCreateInstance auf,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) um den Filter Graph Manager zu erstellen:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Wie gezeigt, ist der Klassenbezeichner (CLSID) CLSID \_ FilterGraph. Der Filter Graph Manager wird von einer Prozess-DLL bereitgestellt, sodass der **Ausführungskontext CLSCTX \_ INPROC \_ SERVER ist.** DirectShow unterstützt das Freethreadingmodell, sodass Sie [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) auch mit dem **COINIT \_ MULTITHREADED-Flag aufrufen** können.

Der Aufruf von [**CoCreateInstance gibt**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) zurück, die hauptsächlich Methoden zum Erstellen des Filterdiagramms enthält. Für dieses Beispiel sind zwei weitere Schnittstellen erforderlich:

-   [**IMediaControl steuert**](/windows/desktop/api/Control/nn-control-imediacontrol) das Streaming. Sie enthält Methoden zum Beenden und Starten des Diagramms.
-   [**IMediaEvent verfügt**](/windows/desktop/api/Control/nn-control-imediaevent) über Methoden zum Abrufen von Ereignissen aus dem Filter Graph Manager. In diesem Beispiel wird die -Schnittstelle verwendet, um auf den Abschluss der Wiedergabe zu warten.

Beide Schnittstellen werden vom Filter-Graph verfügbar gemacht. Verwenden Sie den [**zurückgegebenen IGraphBuilder-Zeiger,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) um sie abfragt:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Nun können Sie das Filterdiagramm erstellen. Für die Dateiwiedergabe erfolgt dies durch einen einzelnen Methodenaufruf:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



Die [**IGraphBuilder::RenderFile-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) erstellt ein Filterdiagramm, das die angegebene Datei wieder geben kann. Der erste Parameter ist der Dateiname, der als Breitzeichenzeichenfolge (2 Byte) dargestellt wird. Der zweite Parameter ist reserviert und muss NULL **sein.**

Diese Methode kann fehlschlagen, wenn die angegebene Datei nicht vorhanden ist oder das Dateiformat nicht erkannt wird. Unter der Annahme, dass die Methode erfolgreich ist, ist das Filterdiagramm jetzt für die Wiedergabe bereit. Rufen Sie zum Ausführen des Graphen die [**IMediaControl::Run-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-run) auf:


```C++
hr = pControl->Run();
```



Wenn das Filterdiagramm ausgeführt wird, werden Die Daten durch die Filter bewegt und als Video und Audio gerendert. Die Wiedergabe erfolgt in einem separaten Thread. Sie können warten, bis die Wiedergabe abgeschlossen ist, indem Sie die [**IMediaEvent::WaitForCompletion-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) aufrufen:


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Diese Methode blockiert, bis die Wiedergabe der Datei oder das angegebene Time out-Intervall verstrichen ist. Der Wert INFINITE bedeutet, dass die Anwendung unbegrenzt blockiert wird, bis die Wiedergabe der Datei abgeschlossen ist. Ein realistischeres Beispiel für die Ereignisbehandlung finden Sie unter [Reagieren auf Ereignisse](responding-to-events.md).

Wenn die Anwendung abgeschlossen ist, geben Sie die Schnittstellenzeker frei, und schließen Sie die COM-Bibliothek:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Beispielcode

Hier ist der vollständige Code für das in diesem Artikel beschriebene Beispiel:


```C++
#include <dshow.h>
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

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> </dl>

 

 
