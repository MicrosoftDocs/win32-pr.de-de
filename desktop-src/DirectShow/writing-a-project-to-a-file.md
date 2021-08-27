---
description: Schreiben eines Project in eine Datei
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Schreiben eines Project in eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efea1d0949c419ba6f595e7a381b689d8a8ce69836609d328b555ee695743b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051370"
---
# <a name="writing-a-project-to-a-file"></a>Schreiben eines Project in eine Datei

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In diesem Artikel wird beschrieben, wie Sie ein [DirectShow Editing Services-Projekt](directshow-editing-services.md) in eine Datei schreiben. Zunächst wird beschrieben, wie eine Datei mit der einfachen Render-Engine geschrieben wird. Anschließend wird die intelligente Neukomprimierung mit der intelligenten Render-Engine beschrieben.

Eine Übersicht darüber, wie DirectShow Editing Services Projekte rendert, finden Sie unter [Informationen zu Render-Engines.](about-the-render-engines.md)

**Verwenden der einfachen Render-Engine**

Erstellen Sie zunächst das Front-End des Diagramms wie folgt:

1.  Erstellen Sie die Render-Engine.
2.  Geben Sie die Zeitachse an.
3.  Legen Sie den Renderbereich fest. (Optional)
4.  Erstellen Sie das Front-End des Diagramms.

Im folgenden Codebeispiel werden diese Schritte veranschaulicht.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



Fügen Sie als Nächstes dem Filterdiagramm Multiplexer- und Dateischreibfilter hinzu. Die einfachste Möglichkeit hierfür ist die [Erfassung Graph Builder,](capture-graph-builder.md)einer DirectShow-Komponente zum Erstellen von Erfassungsdiagrammen. Der Aufzeichnungsgraph-Generator macht die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) verfügbar. Führen Sie die folgenden Schritte aus:

1.  Erstellen Sie eine Instanz des Aufzeichnungsgraph-Generators.
2.  Rufen Sie einen Zeiger auf das Diagramm ab, und übergeben Sie ihn an den Graph-Generator.
3.  Geben Sie den Namen und den Medientyp der Ausgabedatei an. Dieser Schritt ruft auch einen Zeiger auf den mux-Filter ab, der später erforderlich ist.

Im folgenden Codebeispiel werden diese Schritte veranschaulicht.


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



Verbinden Sie abschließend die Ausgabepins am Front-End mit dem Mux-Filter.

1.  Ruft die Anzahl der Gruppen ab.
2.  Rufen Sie für jede Stecknadel einen Zeiger auf den Stecknadel ab.
3.  Erstellen Sie optional eine Instanz eines Komprimierungsfilters, um den Stream zu komprimieren. Der Typ der Gruppierung hängt vom Medientyp der Gruppe ab. Sie können den [Systemgeräte-Enumerator](system-device-enumerator.md) verwenden, um die verfügbaren Komprimierungsfilter aufzuzählen. Weitere Informationen finden Sie unter [Aufzählen von Geräten und Filtern.](enumerating-devices-and-filters.md)
4.  Legen Sie optional Komprimierungsparameter wie die Keyframerate fest. Dieser Schritt wird weiter unten in diesem Artikel ausführlich erläutert.
5.  Rufen Sie [**ICaptureGraphBuilder2::RenderStream auf.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Diese Methode verwendet Zeiger auf den Pin, den Komprimierungsfilter (falls vorhanden) und den Multiplexer.

Das folgende Codebeispiel zeigt, wie Die Ausgabepins verbunden werden.


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



Verwenden Sie die [**IAMVideoCompression-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) um Komprimierungsparameter (Schritt 4, zuvor) festzulegen. Diese Schnittstelle wird auf den Ausgabepins von Komprimierungsfiltern verfügbar gemacht. Aufzählen sie die Pins des Komprimierungsfilters, und fragen Sie jeden Ausgabepin nach **IAMVideoCompression ab.** (Informationen zum Aufzählen von Pins finden Sie unter [Enumerating Pins](enumerating-pins.md).) Stellen Sie sicher, dass Sie alle Schnittstellenzeiger freigeben, die Sie während dieses Schritts abgerufen haben.

Nachdem Sie das Filterdiagramm erstellt haben, rufen Sie die [**IMediaControl::Run-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-run) im Filterdiagramm-Manager auf. Während der Ausführung des Filterdiagramms werden die Daten in eine Datei geschrieben. Verwenden Sie die Ereignisbenachrichtigung, um auf den Abschluss der Wiedergabe zu warten. (Siehe [Reagieren auf Ereignisse](responding-to-events.md).) Wenn die Wiedergabe abgeschlossen ist, müssen Sie [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) explizit aufrufen, um das Filterdiagramm zu beenden. Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.

**Verwenden der intelligenten Render-Engine**

Um die Vorteile der intelligenten Neukomprimierung zu nutzen, verwenden Sie die intelligente Render-Engine anstelle der grundlegenden Render-Engine. Die Schritte zum Erstellen des Diagramms sind fast identisch. Der Hauptunterschied besteht darin, dass die Komprimierung im Front-End des Diagramms und nicht im Abschnitt zum Schreiben von Dateien erfolgt.

> [!IMPORTANT]
> Verwenden Sie die intelligente Render-Engine nicht, um Windows Mediendateien zu lesen oder zu schreiben.

 

Jede Videogruppe verfügt über eine -Eigenschaft, die das Komprimierungsformat für diese Gruppe angibt. Das Komprimierungsformat muss genau mit dem nicht komprimierten Format der Gruppe in Höhe, Breite, Bittiefe und Bildfrequenz übereinstimmen. Die intelligente Render-Engine verwendet beim Erstellen des Diagramms das Komprimierungsformat. Stellen Sie vor dem Festlegen des Komprimierungsformats sicher, dass Sie das nicht komprimierte Format für diese Gruppe festlegen, indem Sie [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md)aufrufen.

Um das Komprimierungsformat einer Gruppe festzulegen, rufen Sie die [**IAMTimelineGroup::SetSmartRecompressFormat-Methode**](iamtimelinegroup-setsmartrecompressformat.md) auf. Diese Methode verwendet einen Zeiger auf eine [**SCompFmt0-Struktur.**](scompfmt0.md) Die **SCompFmt0-Struktur** verfügt über zwei Member: **nFormatId**, die null sein muss, und **MediaType**, eine [**AM MEDIA \_ \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Initialisieren Sie die **AM \_ MEDIA \_ TYPE-Struktur** mit den Formatinformationen.

> [!Note]  
> Wenn das endgültige Projekt das gleiche Format wie eine Ihrer Quelldateien aufweisen soll, können Sie die AM \_ MEDIA \_ TYPE-Struktur direkt aus der Quelldatei abrufen, indem Sie die Medienerkennung verwenden. Siehe [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Wandeln Sie die [**Variable SCompFmt0**](scompfmt0.md) in einen Zeiger vom Typ **long** um, wie im folgenden Beispiel gezeigt.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



Die intelligente Render-Engine sucht automatisch nach einem kompatiblen Komprimierungsfilter. Sie können auch einen Komprimierungsfilter für eine Gruppe angeben, indem [**Sie ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)aufrufen.

Führen Sie zum Erstellen des Diagramms die gleichen Schritte aus, die im vorherigen Abschnitt für die Grundlegende Render-Engine beschrieben wurden. Die einzigen Unterschiede sind die folgenden:

-   Verwenden Sie die intelligente Render-Engine, nicht die einfache Render-Engine. Der Klassenbezeichner ist CLSID \_ SmartRenderEngine.
-   Legen Sie Komprimierungsparameter fest, nachdem Sie das Front-End erstellt haben, aber bevor Sie die Ausgabepins rendern. Rufen Sie die [**ISmartRenderEngine::GetGroupCompressor-Methode**](ismartrenderengine-getgroupcompressor.md) auf, um einen Zeiger auf den Komprimierungsfilter einer Gruppe abzurufen. Fragen Sie dann die [**IAMVideoCompression-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ab, wie zuvor beschrieben.
-   Wenn Sie die Ausgabepins rendern, ist es nicht erforderlich, einen Komprimierungsfilter einzufügen. Der Stream ist bereits komprimiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> </dl>

 

 



