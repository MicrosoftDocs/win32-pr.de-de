---
description: Erstellen der Neukomprimierungs Graph
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Erstellen der Neukomprimierungs Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0432f51e5309a308b32535993fef04da1762d45f179e1ab3a6826d4c5432b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159119"
---
# <a name="building-the-recompression-graph"></a>Erstellen der Neukomprimierungs Graph

Ein typisches Filterdiagramm für die ERNEUTE Komprimierung von AVI-Dateien sieht wie folgt aus:

![Avi-Rekomprimierungsdiagramm](images/avi2avi4.png)

Der [AVI-Splitterfilter](avi-splitter-filter.md) pullt Daten aus dem Filter ["File Source (Async)"](file-source--async--filter.md) und analysiert sie in Video- und Audiostreams. Der Videodekomprimierungs-Dekomprimierer decodiert das komprimierte Video, wo es von der Videobeodruckung erneut komprimiert wird. Die Auswahl der Dekomprimatoren hängt von der Quelldatei ab. wird automatisch von Intelligent [Verbinden.](intelligent-connect.md) Die Anwendung muss den Zettel auswählen, in der Regel indem dem Benutzer eine Liste angezeigt wird. (Siehe [Auswählen eines Komprimierungsfilters.)](choosing-a-compression-filter.md)

Das komprimierte Video geht dann zum [AVI Mux Filter](avi-mux-filter.md). Der Audiostream in diesem Beispiel ist nicht komprimiert und wird daher direkt vom AVI-Splitter an den AVI Mux übertragen. Der AVI Mux verkettet die beiden Datenströme, und der [File Writer-Filter](file-writer-filter.md) schreibt die Ausgabe auf den Datenträger. Beachten Sie, dass die AVI Mux-Datei auch dann erforderlich ist, wenn die ursprüngliche Datei keinen Audiostream enthält.

Die einfachste Möglichkeit zum Erstellen dieses Filterdiagramms ist die Verwendung des [Capture Graph Builder,](capture-graph-builder.md)einer DirectShow-Komponente zum Erstellen von Erfassungsdiagrammen und anderen benutzerdefinierten Filterdiagrammen.

Rufen Sie zunächst CoCreateInstance auf, um den Capture Graph Builder zu erstellen:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



Verwenden Sie dann den Capture Graph Builder, um das Filterdiagramm zu erstellen:

1.  Erstellen Sie den Renderingabschnitt des Diagramms, der den AVI Mux-Filter und den [File Writer enthält.](file-writer-filter.md)
2.  Fügen Sie dem Diagramm den Quellfilter und den Komprimierungsfilter hinzu.
3.  Verbinden quellfilter an den MUX-Filter. Der Generator für Erfassungsdiagramme fügt alle Splitter- und Decoderfilter ein, die zum Analysieren der Quelldatei erforderlich sind. Sie kann die Video- und Audiodatenströme auch über Komprimierungsfilter routen.

In den folgenden Abschnitten werden die einzelnen Schritte erläutert.

Erstellen des Renderingabschnitts

Um den Renderingabschnitt des Diagramms zu erstellen, rufen Sie die [**ICaptureGraphBuilder2::SetOutputFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) auf. Diese Methode verwendet Eingabeparameter, die den Medienuntertyp für die Ausgabe und den Namen der Ausgabedatei angeben. Sie gibt Zeiger auf den MUX-Filter und den Dateiwriter zurück. Der MUX-Filter wird für die nächste Phase der Graphen-Entwicklung benötigt. Der Zeiger auf den Dateiwriter ist für dieses Beispiel nicht erforderlich, sodass der Parameter NULL sein **kann:**


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Wenn die Methode zurückgegeben wird, verfügt der MUX-Filter über einen ausstehenden Verweiszähler. Stellen Sie daher sicher, dass Sie den Zeiger später wieder frei geben.

Das folgende Diagramm zeigt das Filterdiagramm an diesem Punkt.

![Renderingabschnitt des Filterdiagramms](images/avi2avi1.png)

Der MUX-Filter macht zwei Schnittstellen zum Steuern des AVI-Formats verfügbar:

-   [**IConfigInterleaving-Schnittstelle:**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)Legt den Überlappungsmodus fest.
-   [**IConfigAviMux-Schnittstelle:**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)Legt den Masterdatenstrom und den AVI-Kompatibilitätsindex fest.

Hinzufügen der Quell- und Komprimierungsfilter

Im nächsten Schritt fügen Sie dem Filterdiagramm die Quell- und Komprimierungsfilter hinzu. Der Capture Graph Builder erstellt automatisch eine Instanz des Filter-Graph-Managers, wenn Sie SetOutputFileName aufrufen. Rufen Sie einen Zeiger darauf ab, indem Sie die [**ICaptureGraphBuilder2::GetFiltergraph-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) aufrufen:


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Rufen Sie nun die [**IGraphBuilder::AddSourceFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um den Filter Async File Source hinzuzufügen, und die [**IFilterGraph::AddFilter-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) um das Video zu hinzufügen:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



An diesem Punkt sind der Quellfilter und der Komprimierungsfilter mit nichts anderem im Diagramm verbunden, wie in der folgenden Abbildung dargestellt:

![Filterdiagramm mit Quell- und Komprimierungsfiltern](images/avi2avi2.png)

Verbinden der Quelle an den Mux

Der letzte Schritt besteht im Verbinden des Quellfilters mit dem AVI Mux-Filter über den Videobeweis. Verwenden Sie [**die ICaptureGraphBuilder2::RenderStream-Methode,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der ein Ausgabepin auf dem Quellfilter mit einem angegebenen Senkenfilter (optional über einen Komprimierungsfilter) verknüpft wird.

Die ersten beiden Parameter geben an, welche der Pins des Quellfilters eine Verbindung herstellen soll, indem eine Stecknadelkategorie und ein Medientyp festgelegt werden. Der Filter Async File Source verfügt nur über einen Ausgabepin, daher sollten diese Parameter **NULL sein.** Die nächsten drei Parameter geben den Quellfilter, den Komprimierungsfilter (falls noch) und den Mux-Filter an.

Im folgenden Codebeispiel wird der Videostream über den Videostream gerendert:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



Das folgende Diagramm zeigt das filter-Diagramm, das bisher erstellt wurde.

![Gerenderter Videostream](images/avi2avi3.png)

Unter der Annahme, dass die Quelldatei über einen Audiostream verfügt, hat der [AVI-Splitterfilter](avi-splitter-filter.md) einen Ausgabepin für die Audiodatei erstellt. Um diese Stecknadel zu verbinden, rufen Sie RenderStream erneut auf:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Hier wird kein Komprimierungsfilter angegeben. Der Ausgabepin des Quellfilters ist bereits verbunden, sodass die RenderStream-Methode nach einem nicht verbundenen Ausgabepin für den Splitterfilter sucht. Er findet den Audiopin und verbindet ihn direkt mit dem MUX-Filter. Wenn die Quelldatei über keinen Audiostream verfügt, ist beim zweiten Aufruf von RenderStream ein Fehler zu sehen. Dieses Verhalten ist normal. Das Diagramm ist nach dem ersten Aufruf von RenderStream abgeschlossen, sodass der Fehler im zweiten Aufruf unbedenklich ist.

In diesem Beispiel ist die Reihenfolge der beiden RenderStream-Aufrufe wichtig. Da im zweiten Aufruf kein Heft angegeben wird, werden alle nicht verbundenen Stecknadeln aus dem AVI-Splitter verbunden. Wenn Sie diesen Aufruf vor dem anderen aufrufen, wird der Videostream möglicherweise ohne Ihre Videobeendung mit der AVI Mux-Datei verbinden. Daher muss der spezifischere Aufruf (mit dem Komprimierungsfilter) zuerst geschehen.

In der vorherigen Diskussion wurde davon ausgegangen, dass es sich bei der Quelldatei um eine AVI-Datei handelt. Dieses Verfahren funktioniert jedoch auch mit anderen Dateitypen, z. B. MPEG-Dateien. Das resultierende Filterdiagramm ist etwas anders.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneutes Dekomprimieren einer AVI-Datei](recompressing-an-avi-file.md)
</dt> </dl>

 

 



