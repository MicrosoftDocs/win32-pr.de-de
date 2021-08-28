---
description: In diesem Thema wird beschrieben, wie Sie eine Topologie für die Audio- oder Videowiedergabe erstellen.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Erstellen von Wiedergabetopologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563fcef0c9ba8b1a4a33aefc17c5cea744f051470bb04df0ab4699ed4af6fa8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600820"
---
# <a name="creating-playback-topologies"></a>Erstellen von Wiedergabetopologien

In diesem Thema wird beschrieben, wie Sie eine Topologie für die Audio- oder Videowiedergabe erstellen. Für die grundlegende Wiedergabe können Sie eine partielle Topologie erstellen, in der die Quellknoten direkt mit den Ausgabeknoten verbunden sind. Sie müssen keine Knoten für die Zwischentransformationen einfügen, z. B. Decoder oder Farbkonverter. Die Mediensitzung verwendet das Topologielader zum Auflösen der Topologie, und das Topologielader fügt die erforderlichen Transformationen ein.

-   [Erstellen der Topologie](#creating-the-topology)
-   [Verbinden von Streams mit Mediensenken](#connecting-streams-to-media-sinks)
-   [Erstellen der Mediensenke](#creating-the-media-sink)
-   [Next Steps](#next-steps)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-topology"></a>Erstellen der Topologie

Im Folgenden finden Sie die allgemeinen Schritte zum Erstellen einer Topologie für die Teilwiedergabe aus einer Medienquelle:

1.  Erstellen Sie die Medienquelle. In den meisten Fällen verwenden Sie den Quellre resolver, um die Medienquelle zu erstellen. Weitere Informationen finden Sie unter [Quellre resolver](source-resolver.md).
2.  Hier erhalten Sie den Präsentationsdeskriptor der Medienquelle.
3.  Erstellen Sie eine leere Topologie.
4.  Verwenden Sie den Präsentationsdeskriptor, um die Streamdeskriptoren aufzählen. Für jeden Streamdeskriptor:
    1.  Hier erhalten Sie den Hauptmedientyp des Streams, z. B. Audio oder Video.
    2.  Überprüfen Sie, ob der Stream derzeit ausgewählt ist. (Optional können Sie einen Stream basierend auf dem Medientyp auswählen oder deaktivieren.)
    3.  Wenn der Stream ausgewählt ist, erstellen Sie basierend auf dem Medientyp des Streams ein Aktivierungsobjekt für die Mediensenke.
    4.  Fügen Sie einen Quellknoten für den Stream und einen Ausgabeknoten für die Mediensenke hinzu.
    5.  Verbinden quellknoten auf den Ausgabeknoten.

Um diesen Prozess einfacher zu verfolgen, ist der Beispielcode in diesem Thema in mehrere Funktionen organisiert. Die Funktion der obersten Ebene heißt `CreatePlaybackTopology` . Es werden drei Parameter verwendet:

-   Ein Zeiger auf eine [**BENUTZEROBERFLÄCHEMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) der Medienquelle.
-   Ein Zeiger auf die [**BESCHRIFTUNGDescriptor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) des Präsentationsdeskriptors. Rufen Sie diesen Zeiger ab, indem [**Sie DENKMediaSource::CreatePresentationDescriptor aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) Für Quellen mit mehreren Präsentationen werden die Präsentationsdeskriptoren für nachfolgende Präsentationen im [MENewPresentation-Ereignis](menewpresentation.md) bereitgestellt.
-   Ein Handle für ein Anwendungsfenster. Wenn die Quelle über einen Videostream verfügt, wird das Video in diesem Fenster angezeigt.

Die Funktion gibt einen Zeiger auf eine Teilwiedergabetopologie im *ppTopology-Parameter* zurück.


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

1.  Rufen [**Sie MFCreateTopology auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) um die Topologie zu erstellen. Anfänglich enthält die Topologie keine Knoten.
2.  Rufen [**SieGEPRESENTationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) auf, um die Anzahl der Streams in der Präsentation zu erhalten.
3.  Rufen Sie für jeden Stream die anwendungsdefinierte Funktion `AddBranchToPartialTopology` für einen Branch in der Topologie auf. Diese Funktion wird im nächsten Abschnitt gezeigt.

## <a name="connecting-streams-to-media-sinks"></a>Verbinden von Streams mit Mediensenken

Fügen Sie für jeden ausgewählten Stream einen Quellknoten und einen Ausgabeknoten hinzu, und verbinden Sie dann die beiden Knoten. Der Quellknoten stellt den Stream dar. Der Ausgabeknoten stellt entweder den [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) oder den [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) dar.

Die `AddBranchToPartialTopology` im nächsten Beispiel gezeigte Funktion verwendet die folgenden Parameter:

-   Ein Zeiger auf [**dieTOPOLOGYTopology-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) der Topologie.
-   Ein Zeiger auf die [**BENUTZEROBERFLÄCHEMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) der Medienquelle.
-   Ein Zeiger auf die [**BESCHRIFTUNGDescriptor-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) des Präsentationsdeskriptors.
-   Der nullbasierte Index des Streams.
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

1.  Ruft [**DIEPRESENTPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf und übergibt den Streamindex. Diese Methode gibt einen Zeiger auf den Streamdeskriptor für diesen Stream zurück, zusammen mit einem booleschen Wert, der angibt, ob der Stream ausgewählt ist.
2.  Wenn der Stream nicht ausgewählt ist, wird die Funktion beendet und gibt S OK zurück, da die Anwendung keinen Topologiezweig für einen Stream erstellen muss, es sei denn, \_ er ist ausgewählt.
3.  Wenn der Stream ausgewählt ist, schließt die Funktion den Topologiezweig wie folgt ab:
    1.  Erstellt ein Aktivierungsobjekt für die Senke, indem die anwendungsdefinierte CreateMediaSinkActivate-Funktion aufruft. Diese Funktion wird im nächsten Abschnitt gezeigt.
    2.  Fügt der Topologie einen Quellknoten hinzu. Der Code für diesen Schritt wird im Thema Erstellen [von Quellknoten gezeigt.](creating-source-nodes.md)
    3.  Fügt der Topologie einen Ausgabeknoten hinzu. Der Code für diesen Schritt wird im Thema Erstellen [von Ausgabeknoten gezeigt.](creating-output-nodes.md)
    4.  Verbindet die beiden Knoten durch Aufrufen [**vonTOPOLOGYNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem Quellknoten. Durch das Verbinden der Knoten gibt die Anwendung an, dass der Upstreamknoten Daten an den Downstreamknoten liefern soll. Ein Quellknoten verfügt über eine Ausgabe, und ein Ausgabeknoten verfügt über eine Eingabe, sodass beide Streamindizes 0 (null) sind.

Erweiterte Anwendungen können Streams auswählen oder deaktivieren, anstatt die Standardkonfiguration der Quelle zu verwenden. Eine Quelle kann mehrere Datenströme haben, und jeder dieser Datenströme kann standardmäßig ausgewählt werden. Der Präsentationsdeskriptor der Medienquelle verfügt über einen Standardsatz von Streamauswahlen. In einer einfachen Videodatei mit einem einzelnen Audio- und Videostream wählt die Medienquelle in der Regel standardmäßig beide Streams aus. Eine Datei kann jedoch mehrere Audiostreams für verschiedene Sprachen oder mehrere Videostreams haben, die mit unterschiedlichen Bitraten codiert sind. In diesem Fall wird die Auswahl einiger Streams standardmäßig aufgehoben. Die Anwendung kann die Auswahl ändern, indem [**sie FÜR DEN Präsentationsdeskriptor DIE FOLGENDEN Aufrufe**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) ankn.: SELECTStream und [**DANNPresentationDescriptor::D eselectStream.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)

## <a name="creating-the-media-sink"></a>Erstellen der Mediensenke

Die nächste Funktion erstellt ein Aktivierungsobjekt für die EVR- oder SAR-Mediensenke.


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

1.  Ruft [**FÜR DEN Streamdeskriptor DEN WERTSTREAMDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) auf. Diese Methode gibt einen [**INTERFACE-Zeiger FÜR DIEMEDIATYPEHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) zurück.

2.  Ruft [**DEN TYP DESMEDIATYPEHandler::GetMajorType auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype) Diese Methode gibt die Haupttyp-GUID für den Stream zurück.

3.  Wenn der Streamtyp Audio ist, ruft die Funktion [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) auf, um das Aktivierungsobjekt des Audiorenderers zu erstellen. Wenn der Streamtyp Video ist, ruft die Funktion [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) auf, um das Aktivierungsobjekt des Videorenderers zu erstellen. Beide Funktionen geben einen Zeiger auf die [**BERACTIVate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück. Dieser Zeiger wird verwendet, um den Ausgabeknoten für die Senke zu initialisieren, wie zuvor gezeigt.

Für jeden anderen Streamtyp gibt dieses Beispiel einen Fehlercode zurück. Alternativ können Sie einfach die Auswahl des Streams aufheben.

## <a name="next-steps"></a>Nächste Schritte

Um eine Mediendatei nach der anderen wiederzugeben, stellen Sie die Topologie in der Mediensitzung in die Warteschlange, indem [**Sie DEN AUFRUF VON DURCHWAHLMediaSession::SetTopology aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) Die Mediensitzung verwendet das Topologielader, um die Topologie aufzulösen. Ein vollständiges Beispiel finden Sie unter [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiederspielen von ungeschützten Mediendateien](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



