---
description: Schreiben eines Projekts in eine Datei
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Schreiben eines Projekts in eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348663"
---
# <a name="writing-a-project-to-a-file"></a>Schreiben eines Projekts in eine Datei

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Artikel wird beschrieben, wie Sie ein [DirectShow-Bearbeitungs Dienst](directshow-editing-services.md) Projekt in eine Datei schreiben. Zunächst wird beschrieben, wie Sie eine Datei mit der grundlegenden Renderingengine schreiben. Anschließend wird die intelligente Neukomprimierung mit dem intelligenten Renderingmodul beschrieben.

Einen Überblick darüber, wie DirectShow-Bearbeitungs Dienste Projekte rendern, finden Sie unter [Informationen zu den renderingmodulen](about-the-render-engines.md).

**Verwenden der grundlegenden Renderingengine**

Beginnen Sie, indem Sie das Front-End des Diagramms wie folgt aufbauen:

1.  Erstellen Sie die Rendering-Engine.
2.  Angeben der Zeitachse.
3.  Legen Sie den Rendering-Bereich fest. (Optional)
4.  Erstellen Sie das Front-End des Diagramms.

Das folgende Codebeispiel zeigt diese Schritte.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Fügen Sie als nächstes Multiplexer-und Datei Schreib Filter zum Filter Diagramm hinzu. Dies lässt sich am einfachsten mit dem [Erfassungs Diagramm](capture-graph-builder.md)-Generator, einer DirectShow-Komponente zum Erstellen von Erfassungs Diagrammen, erreichen. Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar. Führen Sie die folgenden Schritte aus:

1.  Erstellen Sie eine Instanz des Erfassungs Diagramm-Generators.
2.  Rufen Sie einen Zeiger auf das Diagramm ab, und übergeben Sie ihn an den Diagramm-Generator.
3.  Geben Sie den Namen und den Medientyp der Ausgabedatei an. In diesem Schritt wird auch ein Zeiger auf den MUX-Filter abgerufen, der später erforderlich ist.

Das folgende Codebeispiel zeigt diese Schritte.


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



Verbinden Sie schließlich die Ausgabe Pins auf dem Front-End mit dem MUX-Filter.

1.  Abrufen der Anzahl von Gruppen.
2.  Rufen Sie für jede PIN einen Zeiger auf die PIN ab.
3.  Erstellen Sie optional eine Instanz eines Komprimierungs Filters, um den Stream zu komprimieren. Der Typ des-Kompressors hängt vom Medientyp der Gruppe ab. Sie können den [Enumerator "System Geräte](system-device-enumerator.md) " verwenden, um die verfügbaren Komprimierungs Filter aufzuzählen. Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).
4.  Legen Sie optional Komprimierungs Parameter fest, z. b. die Keyframe-Rate. Dieser Schritt wird weiter unten in diesem Artikel ausführlich erläutert.
5.  [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aufzurufen. Diese Methode nimmt Zeiger auf die PIN, den Komprimierungs Filter (falls vorhanden) und den Multiplexer.

Im folgenden Codebeispiel wird gezeigt, wie die Ausgabe Pins verbunden werden.


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



Verwenden Sie zum Festlegen von Komprimierungs Parametern (Schritt 4, früher) die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle. Diese Schnittstelle wird auf den Ausgabe Pins von Komprimierungs Filtern verfügbar gemacht. Zählen Sie die Pins des Komprimierungs Filters auf, und Fragen Sie jede Ausgabe-PIN für **IAMVideoCompression** ab. (Informationen zum Auflisten von Pins finden Sie unter [Enumerieren von Pins](enumerating-pins.md).) Achten Sie darauf, alle Schnittstellen Zeiger freizugeben, die Sie während dieses Schritts abgerufen haben.

Nachdem Sie das Filter Diagramm erstellt haben, können Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode für den Filter Graph-Manager aufruft. Während der Ausführung des Filter Diagramms werden die Daten in eine Datei geschrieben. Verwenden Sie die Ereignis Benachrichtigung, um die Wiedergabe zu warten. (Weitere Informationen finden [Sie unter reagieren auf Ereignisse](responding-to-events.md).) Wenn die Wiedergabe abgeschlossen ist, müssen Sie [**IMediaControl:: beenden**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) explizit zum Beenden des Filter Diagramms aufruft. Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.

**Verwenden der intelligenten Renderingengine**

Um die Vorteile der intelligenten Neukomprimierung zu nutzen, verwenden Sie die Smart-Rendering-Engine anstelle der grundlegenden Renderingengine. Die Schritte zum Aufbau des Diagramms sind fast identisch. Der Hauptunterschied besteht darin, dass die Komprimierung am Front-End des Diagramms erfolgt, nicht im Abschnitt zum Schreiben von Dateien.

> [!IMPORTANT]
> Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien.

 

Jede Videogruppe verfügt über eine-Eigenschaft, die das Komprimierungs Format für diese Gruppe angibt. Das Komprimierungs Format muss in Höhe, Breite, Bittiefe und Framerate genau mit dem unkomprimierten Format der Gruppe übereinstimmen. Das Smart-Renderingmodul verwendet das Komprimierungs Format beim Erstellen des Diagramms. Bevor Sie das Komprimierungs Format festlegen, stellen Sie sicher, dass das unkomprimierte Format für diese Gruppe durch Aufrufen von [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md)festgelegt wird.

Um das Komprimierungs Format einer Gruppe festzulegen, rufen Sie die [**iamtimelinegroup:: sezmartrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md) -Methode auf. Diese Methode nimmt einen Zeiger auf eine [**SCompFmt0**](scompfmt0.md) -Struktur. Die **SCompFmt0** -Struktur verfügt über zwei Member: **nformatid**, die 0 (null) sein muss, und **mediaType**, die eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur ist. Initialisieren Sie die **am- \_ \_ Medientyp** Struktur mit den Formatinformationen.

> [!Note]  
> Wenn Sie möchten, dass das endgültige Projekt das gleiche Format wie eine der Quelldateien hat, können Sie die am- \_ \_ Medientyp Struktur mithilfe des Medien Detektors direkt aus der Quelldatei beziehen. Weitere Informationen finden [**Sie unter imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md).

 

Wandeln Sie die [**SCompFmt0**](scompfmt0.md) -Variable in einen Zeiger vom Typ **Long** um, wie im folgenden Beispiel gezeigt.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



Die intelligente Renderingengine sucht automatisch nach einem kompatiblen Komprimierungs Filter. Sie können auch einen Komprimierungs Filter für eine Gruppe angeben, indem Sie [**ismartrenderengine:: setgroupkompressor**](ismartrenderengine-setgroupcompressor.md)aufrufen.

Um das Diagramm zu erstellen, verwenden Sie die gleichen Schritte, die im vorherigen Abschnitt für die grundlegende Renderingengine beschrieben wurden. Die einzigen Unterschiede sind die folgenden:

-   Verwenden Sie die Smart-Rendering-Engine, nicht die grundlegende Rendering-Engine. Der Klassen Bezeichner ist CLSID \_ smartrenderengine.
-   Legen Sie Komprimierungs Parameter fest, nachdem Sie das Front-End erstellt haben, aber bevor Sie die Ausgabe Pins renden Rufen Sie die [**ismartrenderengine:: getgroupcompressor**](ismartrenderengine-getgroupcompressor.md) -Methode auf, um einen Zeiger auf den Komprimierungs Filter einer Gruppe zu erhalten. Fragen Sie dann die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle ab, wie zuvor beschrieben.
-   Wenn Sie die Ausgabe Pins rendernen, ist es nicht erforderlich, einen Komprimierungs Filter einzufügen. Der Stream ist bereits komprimiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 



