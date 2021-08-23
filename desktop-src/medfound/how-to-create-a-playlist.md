---
description: In diesem Thema wird beschrieben, wie Sie die Sequenzquelle verwenden, um eine Sequenz von Dateien wiederzuspielen.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Erstellen einer Wiedergabeliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d2a36735d29510e0622882a399fff199fd2289261453a51f281414b5076826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828170"
---
# <a name="how-to-create-a-playlist"></a>Erstellen einer Wiedergabeliste

In diesem Thema wird beschrieben, wie Sie die Sequenzquelle verwenden, um eine Sequenz von Dateien wiederzuspielen.

## <a name="overview"></a>Übersicht

Um Mediendateien in einer Sequenz wiederzugeben, muss die Anwendung Topologien in einer Sequenz hinzufügen, um eine Wiedergabeliste zu erstellen, und diese Topologien für die Wiedergabe in der Mediensitzung in die Warteschlange stellen.

Die Sequencerquelle stellt eine nahtlose Wiedergabe sicher, indem die nächste Topologie initialisiert und geladen wird, bevor die Mediensitzung mit der Wiedergabe der aktuellen Topologie beginnt. Dies ermöglicht es der Anwendung, die nächste Topologie schnell zu starten, wenn sie erforderlich ist.

Die Mediensitzung ist für die Einspeisung von Daten an die Senken und die Wiedergabe der Topologien in der Sequenzquelle zuständig. Darüber hinaus verwaltet die Mediensitzung die Präsentationszeit für die Segmente.

Weitere Informationen zur Verwaltung von Topologien durch die Sequencerquelle finden Sie unter [Informationen zur Sequencerquelle.](about-the-sequencer-source.md)

Diese exemplarische Vorgehensweise enthält die folgenden Schritte:

1.  [Voraussetzungen](#prerequisites)
2.  [Initialisieren Media Foundation](#initializing-media-foundation)
3.  [Erstellen von Media Foundation-Objekten](#creating-media-foundation-objects)
4.  [Erstellen der Medienquelle](#creating-the-media-source)
5.  [Erstellen von Teiltopologien](#creating-partial-topologies)
6.  [Hinzufügen von Topologien zur Sequencerquelle](#adding-topologies-to-the-sequencer-source)
7.  [Festlegen der ersten Topologie in der Mediensitzung](#setting-the-first-topology-on-the-media-session)
8.  [Queuing the Next Topology on the Media Session](#queuing-the-next-topology-on-the-media-session)
9.  [Freigeben der Sequencerquelle](#releasing-the-sequencer-source)

Die in diesem Thema gezeigten Codebeispiele sind Auszüge aus dem Thema [Sequencer Source Example Code](sequencer-source-example-code.md), das den vollständigen Beispielcode enthält.

## <a name="prerequisites"></a>Voraussetzungen

Machen Sie sich vor Beginn dieser exemplarischen Schritte mit den folgenden Media Foundation Konzepten vertraut:

-   [Mediensitzung](media-session.md)
-   [Topologien](topologies.md)
-   [Medienereignisgeneratoren](media-event-generators.md)
-   [Präsentationsdeskriptoren](presentation-descriptors.md)

Lesen Sie auch [Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md), da der hier enthaltene Beispielcode den Code in diesem Thema erweitert.

## <a name="initializing-media-foundation"></a>Initialisieren Media Foundation

Bevor Sie Media Foundation Schnittstellen oder Methoden verwenden können, initialisieren Sie Media Foundation, indem Sie die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) aufrufen. Weitere Informationen finden Sie unter [Initialisieren Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Erstellen von Media Foundation-Objekten

Erstellen Sie als Nächstes die folgenden Media Foundation-Objekte:

-   Mediensitzung. Dieses Objekt macht die [**INTERFACESMediaSession-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) verfügbar, die Methoden zum Wiedergeben, Anhalten und Beenden der aktuellen Topologie bereitstellt.
-   Sequencerquelle. Dieses Objekt macht die [**INTERFACESSequencerSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) verfügbar, die Methoden zum Hinzufügen, Aktualisieren und Löschen von Topologien in einer Sequenz bereitstellt.

1.  Rufen Sie die [**MFCreateMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um die Mediensitzung zu erstellen.
2.  Rufen Sie [**DEN AUFRUF VONMEDIAEVENTQUEUE::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) auf, um das erste Ereignis aus der Mediensitzung anzufordern.
3.  Rufen Sie die [**MFCreateSequencerSource-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) auf, um die Sequencerquelle zu erstellen.

Der folgende Code erstellt die Mediensitzung und fordert das erste Ereignis an:


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>Erstellen der Medienquelle

Erstellen Sie als Nächstes eine Medienquelle für das erste Wiedergabelistensegment. Verwenden Sie den [Quelllöser,](source-resolver.md) um eine Medienquelle aus einer URL zu erstellen. Rufen Sie zu diesem Zweck die [**MFCreateSourceResolver-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) auf, um einen Quellresolver zu erstellen, und rufen Sie dann die [**METHODE VONSOURCEResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) auf, um die Medienquelle zu erstellen.

Informationen zu Medienquellen finden Sie unter [Medienquellen.](media-sources.md)

## <a name="creating-partial-topologies"></a>Erstellen von Teiltopologien

Jedes Segment in der Sequencerquelle verfügt über eine eigene partielle Topologie. Erstellen Sie als Nächstes Teiltopologien für Medienquellen. Bei einer partiellen Topologie werden die Topologiequellknoten direkt mit den Ausgabeknoten verbunden, ohne zwischengeschaltete Transformationen anzugeben. Die Mediensitzung verwendet das Topologieladeprogrammobjekt, um die Topologie aufzulösen. Nachdem eine Topologie aufgelöst wurde, werden die erforderlichen Decoder und andere Transformationsknoten hinzugefügt. Die Sequencerquelle kann auch vollständige Topologien enthalten.

Um das Topologieobjekt zu erstellen, verwenden Sie die [**MFCreateTopology-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) und dann die [**NODESTopologyNode-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) um Streamknoten zu erstellen.

Eine vollständige Anleitung zur Verwendung dieser Programmierelemente zum Erstellen von Topologien finden Sie unter [Erstellen von Wiedergabetopologien.](creating-playback-topologies.md)

Eine Anwendung kann einen ausgewählten Teil der nativen Quelle wiedergeben, indem der Quellknoten konfiguriert wird. Legen Sie hierzu das [**MF \_ TOPONODE \_ MEDIASTART-Attribut**](mf-toponode-mediastart-attribute.md) und das [**MF \_ TOPONODE \_ MEDIASTOP-Attribut**](mf-toponode-mediastop-attribute.md) auf **MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE-Topologieknotenknoten** fest. Geben Sie die Startzeit des Mediums und die Medienstoppzeit relativ zum Start der nativen Quelle als **UINT64-Typen** an.

## <a name="adding-topologies-to-the-sequencer-source"></a>Hinzufügen von Topologien zur Sequencerquelle

Fügen Sie als Nächstes der Sequencerquelle die partiellen Topologien hinzu, die Sie erstellt haben. Jedem Sequenzelement, das als *Segment* bezeichnet wird, wird ein **MFSequencerElementId-Bezeichner** zugewiesen. Weitere Informationen zur Verwaltung von Topologien durch die Sequencerquelle finden Sie unter [Informationen zur Sequencerquelle.](about-the-sequencer-source.md)

Nachdem alle Topologien der Sequencerquelle hinzugefügt wurden, muss die Anwendung das letzte Segment in der Sequenz kennzeichnen, um die Wiedergabe in der Pipeline zu beenden. Ohne dieses Flag erwartet die Sequencerquelle, dass weitere Topologien hinzugefügt werden.

1.  Rufen Sie die [**APPENDSequencerSource::AppendTopology-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) auf, um der Sequencerquelle eine bestimmte Topologie hinzuzufügen.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) fügt der Sequenz die angegebene Topologie hinzu. Diese Methode gibt den Segmentbezeichner im *pdwId-Parameter* zurück.

    Wenn die Topologie die letzte in der Sequencerquelle ist, übergeben Sie SequencerTopologyFlags \_ Last im *dwFlags-Parameter.* Dieser Wert wird in der [**MFSequencerTopologyFlags-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) definiert.

2.  Rufen Sie [**DEN AUFRUFEQUENCERSOURCE::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) auf, um die Flags für die Topologie zu aktualisieren, die dem Segmentbezeichner in der Eingabeliste zugeordnet ist. In diesem Fall gibt der Aufruf an, dass das angegebene Segment das letzte Segment im Sequencer ist. (Dieser Aufruf ist optional, wenn die letzte Topologie im [**AppendTopology-Aufruf**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) angegeben ist.)

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

Die Anwendung kann die Topologie eines Segments durch eine andere Topologie ersetzen, indem sie [**DIE QuencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) aufruft und die neue Topologie in *pTopology* übergibt. Wenn neue native Quellen in der neuen Topologie vorhanden sind, werden die Quellen dem Quellcache hinzugefügt. Die Prerollliste wird ebenfalls aktualisiert.

## <a name="setting-the-first-topology-on-the-media-session"></a>Festlegen der ersten Topologie in der Mediensitzung

Als Nächstes wird die erste Topologie in der Sequenzquelle in der Mediensitzung in die Warteschlange eingereiht. Um die erste Topologie aus der Sequencerquelle abzurufen, muss die Anwendung die [**METHODE VONMEDIASourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) aufrufen. Diese Methode gibt die partielle Topologie zurück, die von der Mediensitzung aufgelöst wird.

Informationen zu Teiltopologien finden Sie unter [Informationen zu Topologien.](about-topologies.md)

1.  Rufen Sie die native Medienquelle für die erste Topologie der Sequenzquelle ab.
2.  Erstellen Sie einen Präsentationsdeskriptor für die Medienquelle, indem Sie die [**METHODE VONMEDIASOURCE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) aufrufen.
3.  Rufen Sie die zugeordnete Topologie für die Präsentation ab, indem Sie die [**METHODE VONMEDIASOURCETopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) aufrufen.
4.  Legen Sie die erste Topologie in der Mediensitzung fest, indem Sie [**DIE SESSIONMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.

    Rufen [**Sie SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, wobei der *dwSetTopologyFlags-Parameter* auf **NULL** festgelegt ist. Dadurch wird die Mediensitzung angewiesen, die angegebene Topologie zu starten, wenn die aktuelle Topologie abgeschlossen wurde. Da in diesem Fall die angegebene Topologie die erste Topologie ist und keine aktuelle Präsentation vorhanden ist, startet die Mediensitzung die neue Präsentation sofort.

    Der **NULL-Wert** gibt auch an, dass die Mediensitzung die Topologie auflösen muss, da die vom Topologieanbieter zurückgegebene Topologie immer eine partielle Topologie ist.


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



## <a name="queuing-the-next-topology-on-the-media-session"></a>Queuing the Next Topology on the Media Session

Als Nächstes muss die Anwendung das [MENewPresentation-Ereignis](menewpresentation.md) verarbeiten.

Die Sequencerquelle löst [MENewPresentation](menewpresentation.md) aus, wenn die Mediensitzung mit der Wiedergabe eines Segments beginnt, dem ein weiteres Segment folgt. Dieses Ereignis informiert die Anwendung über die nächste Topologie in der Sequenzquelle, indem der Präsentationsdeskriptor für das nächste Segment in der Prärollliste angegeben wird. Die Anwendung muss die zugeordnete Topologie mithilfe des Topologieanbieters abrufen und in der Mediensitzung in die Warteschlange stellen. Die Sequencerquelle führt dann eine Vorrolling dieser Topologie durch, wodurch ein nahtloser Übergang zwischen Präsentationen sichergestellt wird.

Wenn die Anwendung segmentübergreifend sucht, empfängt die Anwendung mehrere [MENewPresentation-Ereignisse,](menewpresentation.md) während die Sequencerquelle die Vorabrollliste aktualisiert und die richtige Topologie einrichtet. Die Anwendung muss jedes Ereignis verarbeiten und die in den Ereignisdaten zurückgegebene Topologie in der Mediensitzung in die Warteschlange stellen. Informationen zum Überspringen von Segmenten finden Sie unter [Verwenden der Sequencerquelle](using-the-sequencer-source.md).

Informationen zum Abrufen von Sequencer-Quellbenachrichtigungen finden Sie unter [Sequencer-Quellereignisse.](sequencer-source-events.md)

1.  Rufen Sie im [MENewPresentation-Ereignishandler](menewpresentation.md) den Präsentationsdeskriptor für das nächste Segment aus den Ereignisdaten ab.
2.  Rufen Sie die zugeordnete Topologie für die Präsentation ab, indem Sie [**die METHODETOPOLOGYMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) aufrufen.
3.  Legen Sie die Topologie für die Mediensitzung fest, indem Sie [**die METHODETOPOLOGYMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) aufrufen.

    Die Mediensitzung startet die neue Präsentation, wenn die aktuelle Präsentation abgeschlossen wurde.


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>Freigeben der Sequencerquelle

Fahren Sie abschließend die Sequencerquelle herunter. Rufen Sie zu diesem Schritt die METHODE 1002211111111177111 der [**Sequencerquelle**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf. Dieser Aufruf fährt alle zugrunde liegenden nativen Medienquellen in der Sequencerquelle herunter.

Nachdem die Sequencerquelle veröffentlicht wurde, sollte die Anwendung die Mediensitzung schließen und herunterfahren, indem sie IN DIESER Reihenfolge [**DURCH DEN Aufruf von DURCHEMEDIASession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) und DURCH DIE [**VeröffentlichungSsitzung::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)beendet wird.

Um Speicherverlusten zu vermeiden, muss die Anwendung Zeiger auf Media Foundation Schnittstellen veröffentlichen, wenn sie nicht mehr benötigt werden.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise wurde veranschaulicht, wie Sie mithilfe der Sequencerquelle eine einfache Wiedergabeliste erstellen. Nach dem Erstellen der Wiedergabeliste sollten Sie erweiterte Features hinzufügen, z. B. Segment überspringen, den Wiedergabezustand ändern und innerhalb eines Segments suchen. Die folgende Liste enthält Links zu den verwandten Themen:

-   [Steuern von Präsentationszuständen:](how-to-control-presentation-states.md)Die Sequencerquelle nutzt die Mediensitzung, um Transportsteuerung wie Wiedergabe, Anhalten und Beenden zu ermöglichen.
-   [How to Perform Scrubbing (How to Perform Scrubbing)](how-to-perform-scrubbing.md) beschreibt die Schritte, die erforderlich sind, um eine bestimmte Position in einem Stream zu suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 



