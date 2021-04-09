---
description: Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860472"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator

Trotz des Namens ist der Erfassungs Diagramm-Generator nützlich zum Erstellen vieler Arten von benutzerdefinierten Filter Diagrammen, nicht nur zum Erfassen von Diagrammen. Dieser Artikel bietet einen kurzen Überblick über die Verwendung dieses Objekts.

Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar. Beginnen Sie, indem Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um den Erfassungs Diagramm-Generator und den Filter Graph-Manager zu erstellen. Initialisieren Sie dann den Erfassungs Diagramm-Generator, indem Sie [**ICaptureGraphBuilder2:: setfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) mit einem Zeiger auf den Filter Graph-Manager wie folgt aufrufen:


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>Verbinden von Filtern

Mit der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode werden zwei oder drei Filter in einer Kette miteinander verbunden. Im Allgemeinen funktioniert die-Methode am besten, wenn jeder Filter nicht mehr als eine Eingabe-PIN oder eine Ausgabe-PIN desselben Typs aufweist. In dieser Diskussion werden zunächst die ersten beiden Parameter von **RenderStream** ignoriert und die letzten drei Parameter fokussiert. Der dritte Parameter ist ein [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger, der entweder einen Filter (als [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstellen Zeiger) oder eine Ausgabe-PIN (als [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen Zeiger) angeben kann. Der vierte und fünfte Parameter geben **ibasefilter** -Zeiger an. Die **RenderStream** -Methode verbindet alle drei Filter in einer Kette. Nehmen wir beispielsweise an, dass *A*, *B* und *C* Filter sind. Nehmen Sie jetzt an, dass jeder Filter genau eine Eingabe-und eine Ausgabe-PIN hat. Der folgende-Befehl verbindet A mit b und dann b mit C:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

Alle Verbindungen sind "intelligent", was bedeutet, dass dem Diagramm nach Bedarf zusätzliche Filter hinzugefügt werden. Weitere Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md). Legen Sie den Mittelwert auf **null** fest, um nur zwei Filter zu verbinden. Beispielsweise wird mit diesem-Befehl eine mit C verbunden:

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

Sie können längere Ketten erstellen, indem Sie die-Methode zweimal aufrufen:

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

Wenn der letzte Parameter **null** ist, sucht die Methode automatisch einen Standardrenderer. Er verwendet den [Videorenderer](video-renderer-filter.md) für Video und den [DirectSound-Renderer](directsound-renderer-filter.md) für Audio. Bisher

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

für die folgende Syntax:

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

Dabei ist *R* der geeignete Renderer. Um den Filter für den Video Mischungs Renderer anstelle des Videorenderers zu verbinden, müssen Sie ihn jedoch explizit angeben.

Wenn Sie anstelle einer PIN einen Filter im dritten Parameter angeben, müssen Sie möglicherweise angeben, welche Ausgabepin für die Verbindung verwendet werden soll. Dies ist der Zweck der ersten beiden Parameter der Methode. Der erste Parameter gilt nur für Erfassungs Filter. Gibt eine GUID an, die eine PIN-Kategorie angibt. Eine umfassende Liste der Kategorien finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md). Zwei der Kategorien sind für alle Erfassungs Filter gültig:

-   **Erfassung der PIN- \_ Kategorie \_**
-   **\_Kategorie \_ Vorschau anheften**

Wenn ein Erfassungs Filter keine separaten Pins für Erfassung und Vorschau bereitstellt, fügt die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode einen [intelligenten Tee](smart-tee-filter.md) -Filter ein, der den Stream in einen Erfassungsdaten Strom und einen Vorschau Datenstrom teilt. Aus Sicht der Anwendung können Sie einfach alle Erfassungs Filter als separate Pins behandeln und die zugrunde liegende Topologie des Diagramms ignorieren.

Verbinden Sie für die Datei Erfassung den Erfassungs-PIN mit einem MUX-Filter. Verbinden Sie für die Live Vorschau die Vorschau-PIN mit einem Renderer. Wenn Sie die beiden Kategorien umschalten, kann das Diagramm während der Datei Erfassung eine übermäßige Anzahl von Frames löschen. Wenn das Diagramm jedoch ordnungsgemäß verbunden ist, werden die Vorschau Rahmen nach Bedarf gelöscht, um den Durchsatz für den Aufzeichnungsdaten Strom aufrechtzuerhalten.

Im folgenden Beispiel wird gezeigt, wie beide Streams verbunden werden:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



Einige Erfassungs Filter unterstützen auch Untertitel, die durch die **Pin- \_ Kategorie \_ VBI** angegeben werden. Um die Untertitel in einer Datei zu erfassen, müssen Sie diese Kategorie in den MUX-Filter Rendering. Um die Untertitel in Ihrem Vorschaufenster anzuzeigen, stellen Sie eine Verbindung mit dem Renderer her:


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



Der zweite Parameter für [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifiziert den Medientyp und ist in der Regel einer der folgenden:

-   MediaType \_ -Audiodatei
-   MediaType- \_ Video
-   Überlappende MediaType \_ (DV)

Sie können diesen Parameter immer dann verwenden, wenn die Ausgabe Pins des Filters die Enumeration bevorzugter Medientypen unterstützen. Bei Datei Quellen fügt der Erfassungs Diagramm-Generator bei Bedarf automatisch einen Parserfilter hinzu und fragt dann die Medientypen auf dem Parser ab. (Ein Beispiel finden Sie unter [Erneutes Komprimieren einer AVI-Datei](recompressing-an-avi-file.md).) Wenn der letzte Filter in der Kette über mehrere Eingabe Pins verfügt, versucht die-Methode, ihre Medientypen aufzuzählen. Diese Funktionalität wird jedoch nicht von allen Filtern unterstützt.

## <a name="finding-interfaces-on-filters-and-pins"></a>Suchen nach Schnittstellen für Filter und Pins

Nachdem Sie ein Diagramm erstellt haben, müssen Sie in der Regel verschiedene Schnittstellen suchen, die von Filtern und Pins im Diagramm verfügbar gemacht werden. Ein Erfassungs Filter kann z. b. die [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) -Schnittstelle verfügbar machen, während die Ausgabe Pins des Filters die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle verfügbar machen können.

Die einfachste Möglichkeit, eine Schnittstelle zu finden, ist die Verwendung der [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode. Diese Methode durchläuft das Diagramm (Filter und Pins), bis die gewünschte Schnittstelle angezeigt wird. Sie können den Startpunkt für die Suche angeben, und Sie können die Suche auf Filter auf Upstream oder downstreamwerte vom Startpunkt beschränken.

Im folgenden Beispiel wird die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle in einer Video Vorschau-Pin gesucht:


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> Das Thema [Suchen einer Schnittstelle in einem Filter oder einer PIN](find-an-interface-on-a-filter-or-pin.md) zeigt einen alternativen Ansatz, der anstelle von [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle verwendet. Welche Vorgehensweise verwendet werden soll, hängt von Ihrer Anwendung ab. Wenn Ihre Anwendung bereits **ICaptureGraphBuilder2** zum Erstellen des Diagramms verwendet, ist [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ein guter Ansatz. Andernfalls sollten Sie die **igraphbuilder** -Methode verwenden.

 

## <a name="finding-pins"></a>Suchen von Pins

In den meisten Fällen müssen Sie möglicherweise eine einzelne PIN für einen Filter finden, obwohl die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -und [**findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methoden in den meisten Fällen Ihnen die Probleme ersparen. Wenn Sie eine bestimmte PIN für einen Filter finden müssen, ist die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Hilfsmethode nützlich. Geben Sie die Kategorie, den Medientyp (Video oder Audiodatei) und die Richtung an, und geben Sie an, ob die PIN nicht verbunden sein muss.

Der folgende Code sucht z. b. nach einer nicht verbundenen Video Vorschau-PIN für einen Erfassungs Filter:


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 
