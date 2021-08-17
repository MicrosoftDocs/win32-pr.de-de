---
description: Auswählen eines Decoders in DirectShow Editing Services
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Auswählen eines Decoders in DirectShow Editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcff63d44918a189f49e11527fe6fef35d108b7f20c1dadefa0a045e2c895b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341270"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Auswählen eines Decoders in DirectShow Editing Services

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Wenn [DirectShow Editing Services](directshow-editing-services.md) (DES) ein Videobearbeitungsprojekt rendert, wählt die Rendering-Engine automatisch die erforderlichen Decoder aus. Dies kann innerhalb der [**IRenderEngine::ConnectFrontEnd-Methode**](irenderengine-connectfrontend.md) oder dynamisch während des Renderings erfolgen.

Ein Benutzer installiert möglicherweise mehrere Decoder, die eine bestimmte Datei decodieren können. Wenn mehrere Decoder verfügbar sind, verwendet DES den [Intelligent Verbinden-Algorithmus,](intelligent-connect.md) um den Decoder auszuwählen.

Es gibt keine Möglichkeit für die Anwendung, direkt anzugeben, welcher Decoder verwendet werden soll. Sie können den Decoder jedoch indirekt über die [**IAMGraphBuilderCallback-Rückrufschnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) auswählen. Indem Sie diese Schnittstelle in Ihrer Anwendung implementieren, können Sie während des Grapherstellungsprozesses Benachrichtigungen empfangen und bestimmte Filter aus dem Diagramm ablehnen.

Implementieren Sie zunächst eine Klasse, die die [**IAMGraphBuilderCallback-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) verfügbar macht:


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



Erstellen Sie dann eine Instanz von Filter Graph Manager, und registrieren Sie Ihre Klasse, um Rückrufbenachrichtigungen zu erhalten:


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



Erstellen Sie als Nächstes die Render-Engine, und rufen Sie die [**IRenderEngine::SetFilterGraph-Methode**](irenderengine-setfiltergraph.md) mit einem Zeiger auf den Filter Graph-Manager auf. Dadurch wird sichergestellt, dass die Render-Engine keinen eigenen Filter-Graph-Manager erstellt, sondern stattdessen die Instanz verwendet, die Sie für Rückrufe konfiguriert haben.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Wenn das Projekt gerendert wird, wird die [**IAMGraphBuilderCallback::SelectedFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) der Anwendung unmittelbar aufgerufen, bevor der Filter Graph Manager einen neuen Filter erstellt. Die **SelectedFilter-Methode** empfängt einen Zeiger auf eine **IMoniker-Schnittstelle,** die einen Moniker für den Filter darstellt. Untersuchen Sie den Moniker, und wenn Sie den Filter ablehnen möchten, geben Sie einen Fehlercode von der **SelectedFilter-Methode** zurück.

Der schwierige Teil besteht darin, zu ermitteln, welche Moniker Decoder darstellen – und insbesondere welche Moniker Decoder darstellen, die Sie ablehnen möchten. Eine Lösung ist die folgende:

-   Verwenden Sie vor dem Rendern des Projekts die [**IFilterMapper2::EnumMatchingFilters-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) um eine Liste von Filtern zu erstellen, die als Akzeptieren des gewünschten Eingabetyps registriert sind. Bei Video- oder Audiokomprimierungstypen sollte diese Liste einer Gruppe von Decodern zugeordnet werden.
-   Die **EnumMatchingFilters-Methode** gibt eine Auflistung von Monikern zurück. Abrufen Sie für jeden Moniker in der Auflistung die **DisplayName-Eigenschaft,** wie unter [Verwenden der Filterzuordnung](using-the-filter-mapper.md)beschrieben.
-   Store eine Liste der Anzeigenamen, lassen Sie jedoch den Anzeigenamen aus, der dem Filter entspricht, den Sie für die Decodierung verwenden möchten. Anzeigenamen für Softwarefilter weisen das folgende Format auf:

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    where

    ```C++
    CategoryGUID
    ```

    

    ist die GUID der Filterkategorie, und

    ```C++
    FilterCLSID
    ```

    

    ist die CLSID des Filters. Für DMOs ist das Format identisch, ändern Sie jedoch `sw` in `dmo` .

    Die Liste enthält jetzt Anzeigenamen für jeden Filter, der den gewünschten Medientyp ausgibt, aber nicht Ihr bevorzugter Filter ist.

-   Abrufen sie in der **SelectedFilter-Methode** die **DisplayName-Eigenschaft** für den vorgeschlagenen Moniker, und überprüfen Sie sie anhand der gespeicherten Liste. Wenn der Anzeigename mit einem Eintrag in der Liste übereinstimmt, weisen Sie diesen Filter zurück. Akzeptieren Sie sie andernfalls, indem Sie S \_ OK zurückgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> </dl>

 

 



