---
description: In diesem Thema wird die Verwendung der Sequencerquelle beschrieben.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Verwenden der Sequencerquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b0607d65d02e507f576a5177ea432f3f7e0fab57c3b575fbb34240a46e91be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972729"
---
# <a name="using-the-sequencer-source"></a>Verwenden der Sequencerquelle

In diesem Thema wird die Verwendung von [Sequencer Source](sequencer-source.md)beschrieben. Sie enthält die folgenden Abschnitte:

-   [Übersicht](#overview)
-   [Hinzufügen von Topologien](#adding-topologies)
-   [Löschen von Topologien](#deleting-topologies)
-   [Überspringen auf ein Segment](#skipping-to-a-segment)
-   [Zugehörige Themen](#related-topics)

Eine allgemeine Übersicht über die Sequencerquelle finden Sie unter [Informationen zur Sequencerquelle.](about-the-sequencer-source.md)

## <a name="overview"></a>Übersicht

Die Sequencerquelle macht die folgenden Schnittstellen verfügbar.



| Schnittstelle                                                                        | BESCHREIBUNG                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**WFMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Macht generische Medienquellfunktionen verfügbar.                                        |
| [**CERSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Ermöglicht der Anwendung das Hinzufügen oder Entfernen von Topologien.                               |
| [**WFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Ruft die nächste Topologie ab, die in der Mediensitzung in die Warteschlange eingereiht werden soll.                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Wird von der Mediensitzung für Endsegmente verwendet. Anwendungen verwenden diese Schnittstelle nicht. |
| [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Fragt die Sequencerquelle nach [Dienstschnittstellen](service-interfaces.md)ab.     |



 

Führen Sie die folgenden Schritte aus, um eine Sequenz von Medienquellen wiederzuspielen:

1.  Um die Sequencerquelle zu erstellen, rufen Sie die [**MFCreateSequencerSource-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) auf.
2.  Erstellen Sie für jedes Segment eine Wiedergabetopologie, wie unter [Erstellen von Wiedergabetopologien](creating-playback-topologies.md)beschrieben. Um die Topologie der Präsentation hinzuzufügen, rufen Sie [**DIE SOURCESequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)auf.
3.  Rufen Sie vor dem Starten der Wiedergabe [**DEN SEQUENCEMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Sequencerquelle auf. Diese Methode gibt einen Zeiger auf einen Präsentationsdeskriptor für das erste Segment zurück. Um die diesem Segment zugeordnete Topologie abzurufen, rufen Sie **QueryInterface** für die Sequencerquelle für die [**SCHNITTSTELLE VONMEDIASourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) auf. Übergeben Sie den Präsentationsdeskriptor an die [**METHODE VONMEDIASOURCETopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Diese Methode gibt einen Zeiger auf die Topologie zurück.
4.  Übergeben Sie die Topologie für das erste Segment an die Mediensitzung, indem Sie die [**METHODE VON MEDIAMEDIASession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) der Mediensitzung aufrufen.
5.  Starten Sie die Wiedergabe, indem Sie [**DEN AUFRUF VONMEDIASESSION::Start ausführen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)
6.  Wenn die Sequencerquelle bereit ist, das nächste Segment vorab zu erstellen, sendet sie ein [MENewPresentation-Ereignis,](menewpresentation.md) dessen Ereignisdaten ein [**POINTERPresentationDescriptor-Schnittstellenzeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) sind. Rufen Sie erneut die Topologie für das Segment ab, indem [**Sie GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) für die Sequencerquelle aufrufen, und legen Sie die Topologie in der Mediensitzung fest, indem [**Sie SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen. Es ist nicht erforderlich, die Medienquelle neu zu starten. es wird automatisch bis zum nächsten Segment wiedergegeben.
7.  Bevor die Anwendung beendet wird, fahren Sie die Sequencerquelle herunter, indem Sie [**DEN AUFRUF VONMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)aufrufen.

Der folgende Code zeigt, wie Sie die Topologie abrufen und in der Mediensitzung festlegen:


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



Ein vollständiges Codebeispiel finden Sie unter [Sequencer Source Example Code](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Hinzufügen von Topologien

Die Sequencerquelle verwaltet zwei Listen von Topologien: die *Eingabeliste* und die *Vorabliste*.

Bei der Eingabeliste handelt es sich um eine Sammlung von Topologien, die Wiedergabelistensegmenten entsprechen, in der Reihenfolge, in der sie von der Anwendung durch Aufrufen von [**APPENDSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)hinzugefügt wurden. Diese Methode weist jeder Topologie einen eindeutigen *Segmentbezeichner* des Typs **MFSequencerElementId** zu. Der Segmentbezeichner wird als Attribut für alle Quelltopologieknoten festgelegt. Eine Anwendung kann den Segmentbezeichner mithilfe des [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID-Attributs](mf-toponode-sequence-elementid-attribute.md) von einem Quellknoten abrufen. Die Eingabeliste kann doppelte Topologien aufweisen, wenn die Anwendung **AppendTopology** in derselben Topologie mehr als einmal aufgerufen hat. Sie werden jedoch durch ihre eindeutigen Segmentbezeichner identifiziert.

Die Vorabliste ist eine Sammlung von Eingabelistentopologien, die als Vorbereitung für die Wiedergabe initialisiert wurden. Dadurch kann die Mediensitzung nahtlos zur nächsten Topologie übergehen, wenn die aktive Topologie endet. Die Anwendung kann Topologien nicht direkt zur Vorabrollliste hinzufügen oder daraus entfernen. sie wird von der Sequencerquelle generiert, wenn eine Topologie aus der Eingabeliste für die Wiedergabe ausgewählt wird. Dies bewirkt, dass die Sequencerquelle die nächste Topologie aus der Eingabeliste der Vorabrollliste hinzufügt. Anschließend löst die Sequencerquelle asynchron das [MENewPresentation-Ereignis](menewpresentation.md) aus und übergibt den Präsentationsdeskriptor für die Prärolltopologie als Ereignisdaten. Die Anwendung muss auf dieses Ereignis lauschen, indem sie die [**SCHNITTSTELLE "OPCMediaEventGenerator"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) der Mediensitzung verwendet und die Prärolltopologie für die Mediensitzung in die Warteschlange einreiht, indem [**SIE DIE SESSIONMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufruft. Dies muss geschehen, bevor die Mediensitzung die Wiedergabe der aktiven Topologie abschließt. **SetTopology** informiert die Mediensitzung über die nächste Topologie, die nach dem Beenden der Wiedergabe der aktiven Topologie wiedergegeben werden muss. Um eine nahtlose Treansition sicherzustellen, muss die Anwendung **SetTopology** aufrufen, bevor die Mediensitzung die Wiedergabe der vorherigen Topologie abgeschlossen hat. Andernfalls besteht eine Lücke zwischen den Segmenten.

Das [MENewPresentation-Ereignis](menewpresentation.md) wird ausgelöst, solange eine Topologie nach der aktiven Topologie vorhanden ist. Wenn die Eingabeliste also nur eine Topologie enthält oder die aktive Topologie die letzte in der Eingabeliste ist, wird dieses Ereignis nicht ausgelöst.

Die Prerollliste wird mit der Eingabeliste synchronisiert und jedes Mal aktualisiert, wenn der Eingabeliste eine Topologie hinzugefügt oder aus dieser gelöscht wird.

## <a name="deleting-topologies"></a>Löschen von Topologien

Um eine Topologie aus der Sequencerquelle zu entfernen, muss eine Anwendung die [**METHODE VONSEQUENCERSOURCE::D eleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) aufrufen und den Segmentbezeichner angeben.

Vor dem Aufrufen von [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)muss die Anwendung sicherstellen, dass die Mediensitzung nicht die Topologie verwendet, die von der Anwendung gelöscht werden soll. Hierzu müssen beide folgenden Schritte ausgeführt werden, bevor die Anwendung **DeleteTopology** aufruft:

-   Das [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) mit MF \_ TOPOSTATUS \_ ENDED wird für die Topologie empfangen, um sicherzustellen, dass die Mediensitzung die Wiedergabe abgeschlossen hat.

-   [MESessionTopologyStatus](mesessiontopologystatus.md) mit MF \_ TOPOSTATUS \_ STARTED SOURCE wird für die nächste Topologie \_ empfangen, um sicherzustellen, dass die Mediensitzung mit der Wiedergabe der nächsten Topologie begonnen hat. Das [MESessionEnded-Ereignis](mesessionended.md) wird empfangen, um sicherzustellen, dass die Mediensitzung mit der letzten Topologie in der Sequencerquelle abgeschlossen wird.

Wenn das zu löschende Segment die aktive Topologie ist, wird die Wiedergabe beendet, und die Sequencerquelle löst das [MEEndOfPresentationSegment-Ereignis](meendofpresentationsegment.md) aus. Wenn die aktive Topologie auch die letzte Topologie ist, wird das [MEEndOfPresentation-Ereignis](meendofpresentation.md) ausgelöst.

## <a name="skipping-to-a-segment"></a>Überspringen auf ein Segment

Eine Anwendung kann zu einem bestimmten Segment in der Sequenz springen, indem sie die [Mediensitzung](media-session.md) wie folgt mit einem Segmentoffset startet:

1.  Rufen Sie die [**MFCreateSequencerSegmentOffset-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) auf, um den Segmentoffset zu erstellen. Geben Sie den Bezeichner des Segments im *dwId-Parameter* an. (Der Bezeichner wurde von der [**METHODE VONSEQUENCERSOURCE::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) zurückgegeben, als Sie der Sequencerquelle zum ersten Mal die Topologie hinzugefügt haben.) Der *Parameter hnsOffset* gibt einen Zeitoffset relativ zum Anfang des Segments an. Die Wiedergabe beginnt zu diesem Zeitpunkt. Übergeben Sie für den *pvarSegmentOffset-Parameter* die Adresse eines leeren **PROPVARIANT -Werts.** Wenn die Funktion zurückgegeben wird, enthält diese **PROPVARIANT** den Segmentoffset.

2.  Rufen Sie die [**METHODE VONMEDIASESSION::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) für die Mediensitzung auf. Verwenden Sie für den *Parameter pguidTimeFormat* den GUID-Wert MF \_ TIME FORMAT SEGMENT \_ \_ \_ OFFSET. Dieser Wert gibt die Suche nach Segmentoffset an. Übergeben Sie für den *Parameter pvarStartPosition* die Adresse des im vorherigen Schritt erstellten **PROPVARIANT.**

Im folgenden Codebeispiel wird gezeigt, wie sie zum Anfang eines angegebenen Segments in einer Sequenz springen.


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Wenn die Anwendung segmentübergreifend sucht, empfängt die Anwendung mehrere Ereignisse, während die Sequencerquelle das aktuelle Segment beendet und sich auf die Wiedergabe des neuen Segments vorbereitet. Da diese Ereignisse asynchron empfangen werden, ist es schwierig, die genaue Sequenz von Ereignissen vorherzusagen. Diese Ereignisse sind wie folgt:

-   Die Sequencerquelle sendet ein [MENewPresentation-Ereignis](menewpresentation.md) für das neue Segment, an das die Mediensitzung übersprungen wird.

-   Wenn die Sequencerquelle das aktive Segment beendet, sendet sie das [MEEndOfPresentationSegment-Ereignis.](meendofpresentationsegment.md)
-   Die Sequencerquelle bricht dann die Prärolltopologie ab. Dies führt zu den folgenden Ereignissen für die abgebrochene Topologie:

    -   [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) mit dem \_ MF TOPOSTATUS \_ READY-Flag.
    -   [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) mit dem \_ MF TOPOSTATUS \_ STARTED \_ SOURCE-Flag.
    -   [MEEndOfPresentationSegment-Ereignis](meendofpresentationsegment.md) mit dem [MF EVENT SOURCE \_ \_ \_ TOPOLOGY \_ CANCELED-Attribut,](mf-event-source-topology-canceled-attribute.md) um anzugeben, dass die Topologie von der Sequencerquelle abgebrochen wurde.

-   Als Nächstes sendet die Sequencerquelle Ereignisse für das neue Segment, einschließlich verschiedener [MESessionTopologyStatus-Ereignisse.](mesessiontopologystatus.md)
-   Wenn das neue Segment nicht das letzte in der Liste ist, aktualisiert die Sequencerquelle die Prerollliste und löst eine weitere [MENewPresentation](menewpresentation.md) für die neue Prärolltopologie aus. Informationen zu Topologien in der Prerollliste finden Sie unter [Informationen zur Sequencerquelle.](about-the-sequencer-source.md)

Weitere Informationen zu den ereignissen, die von der Sequencerquelle gesendet werden, finden Sie im Thema [Sequencer Source Events](sequencer-source-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Wiedergabeliste](how-to-create-a-playlist.md)
</dt> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 



