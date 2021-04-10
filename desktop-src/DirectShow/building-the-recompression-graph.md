---
description: Das neukomprimierungs Diagramm wird erstellt.
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Das neukomprimierungs Diagramm wird erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860035"
---
# <a name="building-the-recompression-graph"></a>Das neukomprimierungs Diagramm wird erstellt.

Ein typisches Filter Diagramm für die Neukomprimierung von AVI-Dateien sieht wie folgt aus:

![Diagramm der AVI-Neukomprimierung](images/avi2avi4.png)

Der [avi-Splitter Filter](avi-splitter-filter.md) Ruft Daten aus dem [Datei Quell Filter (Async)](file-source--async--filter.md) ab und analysiert sie in Video-und Audiostreams. Das Video Debug decodiert das komprimierte Video, bei dem es durch den Video-Kompressor erneut komprimiert wird. Die Auswahl der Dekompressoren hängt von der Quelldatei ab. Sie wird automatisch von [Intelligent Connect](intelligent-connect.md)verarbeitet. Die Anwendung muss den-Kompressor auswählen, in der Regel durch das präsentieren einer Liste für den Benutzer. (Siehe [Auswählen eines Komprimierungs Filters](choosing-a-compression-filter.md).)

Das komprimierte Video wechselt dann zum [AVI MUX-Filter](avi-mux-filter.md). Der Audiodatenstrom in diesem Beispiel ist nicht komprimiert und wird daher direkt vom avi-Splitter zum AVI MUX geleitet. Der AVI MUX lässt die beiden Streams ein, und der [dateiwriter-Filter](file-writer-filter.md) schreibt die Ausgabe auf den Datenträger. Beachten Sie, dass AVI MUX erforderlich ist, auch wenn die ursprüngliche Datei über keinen Audiodatenstrom verfügt.

Die einfachste Möglichkeit zum Erstellen dieses Filter Diagramms ist die Verwendung des [Erfassungs Diagramm](capture-graph-builder.md)-Generators, bei dem es sich um eine DirectShow-Komponente zum Erstellen von Erfassungs Diagrammen und anderen benutzerdefinierten Filter Diagrammen handelt.

Starten Sie, indem Sie CoCreateInstance aufrufen, um den Erfassungs Diagramm-Generator zu erstellen:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



Verwenden Sie dann den Erfassungs Diagramm-Generator, um das Filter Diagramm zu erstellen:

1.  Erstellen Sie den Renderingabschnitt des Diagramms, der den AVI MUX-Filter und den [dateiwriter](file-writer-filter.md)enthält.
2.  Fügen Sie dem Diagramm den Quell Filter und den Komprimierungs Filter hinzu.
3.  Verbinden Sie den Quell Filter mit dem MUX-Filter. Der Erfassungs Diagramm-Generator fügt alle Splitter Filter ein, die zum Analysieren der Quelldatei erforderlich sind. Sie kann auch die Video-und Audiostreams durch Komprimierungs Filter weiterleiten.

In den folgenden Abschnitten werden die einzelnen Schritte erläutert.

Erstellen des renderingabschnitts

Um den Renderingabschnitt des Diagramms zu erstellen, müssen Sie die [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) -Methode aufrufen. Diese Methode nimmt Eingabeparameter an, die den Medien Untertyp für die Ausgabe und den Namen der Ausgabedatei angeben. Sie gibt Zeiger auf den MUX-Filter und den dateiwriter zurück. Der Mux-Filter ist für die nächste Phase der Diagramm Bildung erforderlich. Der Zeiger auf den dateiwriter ist für dieses Beispiel nicht erforderlich, sodass der Parameter **null** sein kann:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Wenn die Methode zurückgegeben wird, hat der Mux-Filter einen ausstehenden Verweis Zähler. Achten Sie daher darauf, dass Sie den Zeiger später freigeben.

Das folgende Diagramm zeigt das Filter Diagramm an dieser Stelle.

![Renderingabschnitt des Filter Diagramms](images/avi2avi1.png)

Der Mux-Filter macht zwei Schnittstellen zum Steuern des AVI-Formats verfügbar:

-   [**Iconfiginterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): legt den Überlappung-Modus fest.
-   [**Iconfigavimux-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): legt den masterb Stream und den AVI-Kompatibilitäts Index fest.

Hinzufügen der Quell-und Komprimierungs Filter

Der nächste Schritt besteht darin, die Quell-und Komprimierungs Filter dem Filter Diagramm hinzuzufügen. Der Erfassungs Diagramm-Generator erstellt automatisch eine Instanz des Filter Graph-Managers, wenn Sie setoutputfilename aufrufen. Rufen Sie einen Zeiger darauf ab, indem Sie die [**ICaptureGraphBuilder2:: getfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) -Methode aufrufen:


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Aufrufen Sie nun die [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) -Methode, um den asynchronen Datei Quell Filter hinzuzufügen, und die [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode, um den Video-Kompressor hinzuzufügen:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



An diesem Punkt sind der Quell Filter und der Komprimierungs Filter nicht mit anderen im Diagramm verbunden, wie in der folgenden Abbildung dargestellt:

![Diagramm mit Quell-und Komprimierungs Filtern Filtern](images/avi2avi2.png)

Verbinden Sie die Quelle mit dem MUX

Der letzte Schritt besteht darin, den Quell Filter über den Video-Kompressor mit dem AVI MUX-Filter zu verbinden. Verwenden Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode, die eine Ausgabe-PIN im Quell Filter mit einem angegebenen Senderfilter verbindet, optional über einen Komprimierungs Filter.

Die ersten beiden Parameter geben an, welche der Pins des Quell Filters eine Verbindung herstellen soll, indem Sie eine PIN-Kategorie und einen Medientyp festlegen. Der asynchrone Datei Quell Filter hat nur eine Ausgabe-PIN, daher sollten diese Parameter **null** sein. Mit den nächsten drei Parametern werden der Quell Filter, der Komprimierungs Filter (falls vorhanden) und der Mux-Filter angegeben.

Im folgenden Codebeispiel wird der Videostream über den Video-Kompressor gerendert:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



Im folgenden Diagramm wird das Filter Diagramm bisher gezeigt.

![gerenderter Videostream](images/avi2avi3.png)

Angenommen, die Quelldatei enthält einen Audiodatenstrom. der [avi-Splitter](avi-splitter-filter.md) Filter hat eine Ausgabe-PIN für das Audioformat erstellt. Um diese PIN zu verbinden, nennen Sie RenderStream erneut:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Hier ist kein Komprimierungs Filter angegeben. Die Ausgabe-PIN des Quell Filters ist bereits verbunden, sodass die RenderStream-Methode im Splitter Filter eine nicht verbundene Ausgabe-PIN durchsucht. Er findet die audiopin und verbindet Sie direkt mit dem MUX-Filter. Wenn die Quelldatei nicht über einen Audiodatenstrom verfügt, tritt beim zweiten RenderStream-RenderStream ein Fehler auf. Dieses Verhalten ist normal. Das Diagramm ist nach dem ersten Aufruf von RenderStream fertiggestellt, sodass der Fehler im zweiten Aufruf harmlos ist.

In diesem Beispiel ist die Reihenfolge der beiden RenderStream-Aufrufe wichtig. Da der zweite-Befehl keinen-Kompressor angibt, verbindet er jede nicht verbundene PIN vom avi-Splitter. Wenn Sie diesen Vorgang vor dem anderen durchführen, wird der Videostream möglicherweise ohne den Video-Kompressor mit dem AVI-MUX verbunden. Daher muss der spezifischere-Befehl (mit dem Komprimierungs Filter) zuerst erfolgen.

Bei der vorherigen Erörterung wurde angenommen, dass die Quelldatei eine AVI-Datei ist. Diese Technik funktioniert jedoch auch mit anderen Dateitypen, z. b. MPEG-Dateien. Das resultierende Filter Diagramm unterscheidet sich etwas.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neukomprimieren einer AVI-Datei](recompressing-an-avi-file.md)
</dt> </dl>

 

 



