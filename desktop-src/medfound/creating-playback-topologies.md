---
description: In diesem Thema wird beschrieben, wie eine Topologie für die Audiowiedergabe oder Videowiedergabe erstellt wird.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Erstellen von Wiedergabe Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344386"
---
# <a name="creating-playback-topologies"></a>Erstellen von Wiedergabe Topologien

In diesem Thema wird beschrieben, wie eine Topologie für die Audiowiedergabe oder Videowiedergabe erstellt wird. Für die einfache Wiedergabe können Sie eine partielle Topologie erstellen, in der die Quellknoten direkt mit den Ausgabe Knoten verbunden sind. Sie müssen keine Knoten für die zwischen Transformationen, wie z. b. Decoder oder Farb Konverter, einfügen. Die Medien Sitzung verwendet den topologielader zum Auflösen der Topologie, und das topologielader fügt die benötigten Transformationen ein.

-   [Erstellen der Topologie](#creating-the-topology)
-   [Verbinden von Datenströmen mit Medien senken](#connecting-streams-to-media-sinks)
-   [Erstellen der Medien Senke](#creating-the-media-sink)
-   [Next Steps](#next-steps)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-topology"></a>Erstellen der Topologie

Im folgenden finden Sie die allgemeinen Schritte zum Erstellen einer partiellen Wiedergabe Topologie aus einer Medienquelle:

1.  Erstellen Sie die Medienquelle. In den meisten Fällen verwenden Sie den quellresolver zum Erstellen der Medienquelle. Weitere Informationen finden Sie unter [quellresolver](source-resolver.md).
2.  Den Präsentations Deskriptor der Medienquelle erhalten.
3.  Erstellen Sie eine leere Topologie.
4.  Verwenden Sie den Präsentations Deskriptor, um die streamdeskriptoren aufzuzählen. Für jeden Datenstrom Deskriptor:
    1.  Holen Sie sich den Haupt Medientyp des Streams, z. b. Audiodaten oder Videos.
    2.  Überprüfen Sie, ob der Stream aktuell ausgewählt ist. (Optional können Sie einen Stream basierend auf dem Medientyp auswählen oder deaktivieren.)
    3.  Wenn der Stream ausgewählt ist, erstellen Sie basierend auf dem Medientyp des Streams ein Aktivierungs Objekt für die Medien Senke.
    4.  Fügen Sie einen Quellknoten für den Stream und einen Ausgabe Knoten für die Medien Senke hinzu.
    5.  Verbinden Sie den Quellknoten mit dem Ausgabe Knoten.

Um diesen Prozess zu vereinfachen, ist der Beispielcode in diesem Thema in mehrere Funktionen gegliedert. Die Funktion der obersten Ebene hat den Namen `CreatePlaybackTopology` . Es werden drei Parameter benötigt:

-   Ein Zeiger auf eine [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.
-   Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors. Rufen Sie diesen Zeiger durch Aufrufen von [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)ab. Für Quellen mit mehreren Präsentationen werden die Präsentations Deskriptoren für nachfolgende Präsentationen im Ereignis [menewpresentation](menewpresentation.md) übermittelt.
-   Ein Handle für ein Anwendungsfenster. Wenn die Quelle über einen Videostream verfügt, wird das Video in diesem Fenster angezeigt.

Die-Funktion gibt einen Zeiger auf eine partielle Wiedergabe Topologie im *pptopology* -Parameter zurück.


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



Diese Funktion führt folgende Schritte aus:

1.  Rufen Sie [**mfkreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) auf, um die Topologie zu erstellen. Anfänglich enthält die Topologie keine Knoten.
2.  Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , um die Anzahl der Streams in der Präsentation zu erhalten.
3.  Für jeden Stream wird die Anwendungs definierte Funktion für `AddBranchToPartialTopology` eine Verzweigung in der Topologie aufgerufen. Diese Funktion wird im nächsten Abschnitt angezeigt.

## <a name="connecting-streams-to-media-sinks"></a>Verbinden von Datenströmen mit Medien senken

Fügen Sie für jeden ausgewählten Stream einen Quellknoten und einen Ausgabe Knoten hinzu, und verbinden Sie dann die beiden Knoten. Der Quellknoten stellt den Datenstrom dar. Der Ausgabe Knoten stellt den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) oder den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR) dar.

Die- `AddBranchToPartialTopology` Funktion, wie im folgenden Beispiel gezeigt, übernimmt die folgenden Parameter:

-   Ein Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie.
-   Ein Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Medienquelle.
-   Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors.
-   Der null basierte Index des Streams.
-   Ein Handle für das Videofenster. Dieses Handle wird nur für den Videostream verwendet.


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



Die Funktion führt Folgendes aus:

1.  Ruft [**IMF presentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf und übergibt den streamindex. Diese Methode gibt einen Zeiger auf den Datenstrom Deskriptor für diesen Stream zusammen mit einem booleschen Wert zurück, der angibt, ob der Stream ausgewählt ist.
2.  Wenn der Stream nicht ausgewählt ist, wird die Funktion beendet, und \_ es wird OK zurückgegeben, da die Anwendung nur dann eine topologieverzweigung für einen Stream erstellen muss, wenn Sie ausgewählt ist.
3.  Wenn der Stream ausgewählt ist, vervollständigt die Funktion den topologiebranch wie folgt:
    1.  Erstellt ein Aktivierungs Objekt für die Senke, indem die von der Anwendung definierte createmediasinkaktivierungs-Funktion aufgerufen wird. Diese Funktion wird im nächsten Abschnitt angezeigt.
    2.  Fügt der Topologie einen Quellknoten hinzu. Code für diesen Schritt finden Sie im Thema [Erstellen von Quellknoten](creating-source-nodes.md).
    3.  Fügt der Topologie einen Ausgabe Knoten hinzu. Code für diesen Schritt wird im Thema Erstellen von [Ausgabe Knoten](creating-output-nodes.md)gezeigt.
    4.  Verbindet die beiden Knoten durch Aufrufen von [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem Quellknoten. Durch das Verbinden der Knoten gibt die Anwendung an, dass der upstreamknoten Daten an den downstreamknoten übermitteln soll. Ein Quellknoten verfügt über eine Ausgabe, und ein Ausgabe Knoten verfügt über eine Eingabe, sodass beide streamindizes NULL sind.

Erweiterte Anwendungen können Streams auswählen oder deaktivieren, anstatt die Standardkonfiguration der Quelle zu verwenden. Eine Quelle kann über mehrere Datenströme verfügen, von denen jede möglicherweise standardmäßig ausgewählt ist. Der Präsentations Deskriptor der Medienquelle verfügt über einen Standardsatz von streamauswahlen. In einer einfachen Videodatei mit einem einzelnen Audiostream und Videostream wählt die Medienquelle in der Regel beide Streams standardmäßig aus. Eine Datei kann jedoch mehrere Audiostreams für verschiedene Sprachen oder mehrere Videostreams enthalten, die mit unterschiedlichen Bitraten codiert sind. In diesem Fall werden einige der Streams standardmäßig deaktiviert. Die Anwendung kann die Auswahl ändern, indem Sie [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) und [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) im Präsentations Deskriptor aufrufen.

## <a name="creating-the-media-sink"></a>Erstellen der Medien Senke

Die Next-Funktion erstellt ein Aktivierungs Objekt für die EVR-oder SAR-Medien Senke.


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



Diese Funktion führt folgende Schritte aus:

1.  Ruft [**IMF-Deskriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor auf. Diese Methode gibt einen [**IMF Media**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) Type-Schnittstellen Zeiger zurück.

2.  Ruft [**IMF mediatypeer Handler:: getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)auf. Diese Methode gibt die GUID des Haupt Typs für den Datenstrom zurück.

3.  Wenn der Streamtyp audiobasiert ist, ruft die Funktion [**mfkreateaudiorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) auf, um das Aktivierungs Objekt für audiorenderer zu erstellen. Wenn der Streamtyp "Video" ist, ruft die Funktion " [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) " auf, um das Videorenderer-Aktivierungs Objekt zu erstellen. Beide Funktionen geben einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle zurück. Dieser Zeiger wird verwendet, um den Ausgabe Knoten für die Senke zu initialisieren, wie zuvor gezeigt.

Für jeden anderen Streamtyp wird in diesem Beispiel ein Fehlercode zurückgegeben. Alternativ können Sie einfach den Datenstrom deaktivieren.

## <a name="next-steps"></a>Nächste Schritte

Um jeweils eine Mediendatei wiederzugeben, stellen Sie die Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in eine Warteschlange. Die Medien Sitzung verwendet den topologielader zum Auflösen der Topologie. Ein umfassendes Beispiel finden Sie unter wieder [Gabe von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabe nicht geschützter Mediendateien](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



