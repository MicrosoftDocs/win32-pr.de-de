---
description: Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481510"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Wenn [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) ein Video Bearbeitungs Projekt rendert, wählt die Rendering-Engine automatisch die erforderlichen Decoder aus. Dies kann innerhalb der Methode " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " oder dynamisch während des Renderings vorkommen.

Ein Benutzer kann mehrere decoderer installieren, die eine bestimmte Datei decodieren können. Wenn mehrere Decoder verfügbar sind, verwendet des den [intelligenten Verbindungs](intelligent-connect.md) Algorithmus, um den Decoder auszuwählen.

Es gibt keine Möglichkeit für die Anwendung, den zu verwendenden Decoder direkt anzugeben. Sie können den Decoder jedoch indirekt über die [**iamgraphbuildercallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) -Rückruf Schnittstelle auswählen. Durch Implementieren dieser Schnittstelle in der Anwendung können Sie während des Graph-Erstellens Benachrichtigungen empfangen und bestimmte Filter aus dem Diagramm ablehnen.

Beginnen Sie mit der Implementierung einer Klasse, die die [**iamgraphbuildercallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) -Schnittstelle verfügbar macht:


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



Erstellen Sie dann eine Instanz des Filter Graph-Managers, und registrieren Sie Ihre Klasse für den Empfang von Rückruf Benachrichtigungen:


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



Erstellen Sie als nächstes die Renderengine, und rufen Sie die Methode " [**irienderengine:: setfiltergraph**](irenderengine-setfiltergraph.md) " mit einem Zeiger auf den Filter Graph-Manager auf. Dadurch wird sichergestellt, dass die Renderingengine keinen eigenen Filter Diagramm-Manager erstellt, sondern stattdessen die Instanz verwendet, die Sie für Rückrufe konfiguriert haben.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Wenn das Projekt gerendert wird, wird die [**iamgraphbuildercallback:: selectedfilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) -Methode der Anwendung sofort aufgerufen, bevor der Filter Graph-Manager einen neuen Filter erstellt. Die **selectedfilter** -Methode empfängt einen Zeiger auf eine **IMoniker** -Schnittstelle, die einen Moniker für den Filter darstellt. Überprüfen Sie den Moniker, und geben Sie, wenn Sie sich entschließen, den Filter abzulehnen, einen Fehlercode von der **selectedfilter** -Methode zurück.

Der schwierige Teil besteht darin, zu ermitteln, welche Moniker Decoder darstellen – und insbesondere, welche Moniker Decoder darstellen, die Sie ablehnen möchten. Eine Lösung ist Folgendes:

-   Bevor Sie das Projekt rendern, verwenden Sie die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode, um eine Liste von Filtern zu erstellen, die als akzeptieren des gewünschten Eingabetyps registriert sind. Bei Video-oder Audiokomprimierungs Typen sollte diese Liste einem Satz von Decodern zugeordnet werden.
-   Die **enummatchingfilters** -Methode gibt eine Sammlung von Monikern zurück. Für jeden Moniker in der Auflistung wird die **DisplayName** -Eigenschaft wie unter [Verwenden des Filter Mappers](using-the-filter-mapper.md)beschrieben angezeigt.
-   Speichern Sie eine Liste der anzeigen Amen, aber lassen Sie den anzeigen Amen aus, der mit dem Filter übereinstimmt, den Sie für die Decodierung verwenden möchten. Anzeigen Amen für Softwarefilter haben folgende Form:

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

    

    die CLSID des Filters. Für DMOS ist das Format identisch, aber ändern `sw` Sie in `dmo` .

    Die Liste enthält nun anzeigen Amen für jeden Filter, der den gewünschten Medientyp ausgibt, aber nicht Ihren bevorzugten Filter.

-   In der **selectedfilter** -Methode können Sie die **Display Name** -Eigenschaft für den vorgeschlagenen Moniker aufrufen und diese anhand der gespeicherten Liste überprüfen. Wenn der Anzeige Name mit einem Eintrag in der Liste übereinstimmt, lehnen Sie diesen Filter ab. Andernfalls akzeptieren Sie es, indem Sie S OK zurückgeben \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 



