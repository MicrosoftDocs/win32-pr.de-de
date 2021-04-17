---
description: In diesem Thema wird beschrieben, wie die Sequenz Quelle verwendet wird, um eine Sequenz von Dateien wiederzugeben.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Erstellen einer Wiedergabeliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527689"
---
# <a name="how-to-create-a-playlist"></a>Erstellen einer Wiedergabeliste

In diesem Thema wird beschrieben, wie die Sequenz Quelle verwendet wird, um eine Sequenz von Dateien wiederzugeben.

## <a name="overview"></a>Übersicht

Zum Wiedergeben von Mediendateien in einer Sequenz muss die Anwendung Topologien in einer Sequenz hinzufügen, um eine Wiedergabeliste zu erstellen, und diese Topologien in der Medien Sitzung zur Wiedergabe in eine Warteschlange stellen.

Die Sequencer-Quelle sorgt für eine nahtlose Wiedergabe durch initialisieren und Laden der nächsten Topologie, bevor die Medien Sitzung mit der Wiedergabe der aktuellen Topologie beginnt. Dadurch kann die Anwendung die nächste Topologie schnell starten, wenn Sie benötigt wird.

Die Medien Sitzung ist für das Füttern von Daten in die senken und das Abspielen der Topologien in der Sequenz Quelle verantwortlich. Außerdem verwaltet die Medien Sitzung die Präsentationszeit für die Segmente.

Weitere Informationen zum Verwalten von Topologien durch die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).

Diese exemplarische Vorgehensweise enthält die folgenden Schritte:

1.  [Voraussetzungen](#prerequisites)
2.  [Media Foundation wird initialisiert.](#initializing-media-foundation)
3.  [Erstellen von Media Foundation Objekten](#creating-media-foundation-objects)
4.  [Erstellen der Medienquelle](#creating-the-media-source)
5.  [Erstellen von partiellen Topologien](#creating-partial-topologies)
6.  [Hinzufügen von Topologien zur Sequencer-Quelle](#adding-topologies-to-the-sequencer-source)
7.  [Festlegen der ersten Topologie in der Medien Sitzung](#setting-the-first-topology-on-the-media-session)
8.  [Nächste Topologie in der Medien Sitzung in die Warteschlange eingereiht](#queuing-the-next-topology-on-the-media-session)
9.  [Freigeben der Sequencer-Quelle](#releasing-the-sequencer-source)

Die in diesem Thema gezeigten Codebeispiele sind Ausschnitte aus dem Thema [Sequencer-Quell Codebeispiel Code](sequencer-source-example-code.md), der den gesamten Beispielcode enthält.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit dieser exemplarischen Vorgehensweise beginnen, machen Sie sich mit den folgenden Media Foundation Konzepten vertraut:

-   [Medien Sitzung](media-session.md)
-   [Topologien](topologies.md)
-   [Medienereignis Generatoren](media-event-generators.md)
-   [Präsentations Deskriptoren](presentation-descriptors.md)

Lesen Sie außerdem die Informationen zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md), da der Code in diesem Thema den Code in diesem Thema erweitert.

## <a name="initializing-media-foundation"></a>Media Foundation wird initialisiert.

Bevor Sie beliebige Media Foundation Schnittstellen oder Methoden verwenden können, initialisieren Sie Media Foundation, indem Sie die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion aufrufen. Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Erstellen von Media Foundation Objekten

Erstellen Sie als nächstes die folgenden Media Foundation Objekte:

-   Medien Sitzung. Dieses Objekt macht die [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstelle verfügbar, die Methoden zum Abspielen, anhalten und stoppen der aktuellen Topologie bereitstellt.
-   Sequencer-Quelle. Dieses Objekt macht die [**imfsequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) -Schnittstelle verfügbar, die Methoden zum Hinzufügen, aktualisieren und Löschen von Topologien in einer Sequenz bereitstellt.

1.  Rufen Sie die [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) -Funktion auf, um die Medien Sitzung zu erstellen.
2.  Aufrufen von [**imfmediaeventqueue:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) , um das erste Ereignis aus der Medien Sitzung anzufordern.
3.  Rufen Sie die [**mfkreatesequencersource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) -Funktion auf, um die Sequencer-Quelle zu erstellen.

Mit dem folgenden Code wird die Medien Sitzung erstellt und das erste Ereignis angefordert:


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

Erstellen Sie als nächstes eine Medienquelle für das erste Wiedergabelisten Segment. Verwenden Sie den [quellresolver](source-resolver.md) , um eine Medienquelle aus einer URL zu erstellen. Rufen Sie hierzu die [**mffroatesourceresolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) -Funktion auf, um einen quellresolver zu erstellen, und rufen Sie dann die [**imfsourceresolver::**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) -Methode auf, um die Medienquelle zu erstellen.

Weitere Informationen zu Medienquellen finden Sie unter [Medienquellen](media-sources.md).

## <a name="creating-partial-topologies"></a>Erstellen von partiellen Topologien

Jedes Segment in der Sequencer-Quelle verfügt über eine eigene partielle Topologie. Erstellen Sie als nächstes partielle Topologien für Medienquellen. Bei einer partiellen Topologie sind die Quellknoten der Topologie direkt mit den Ausgabe Knoten verbunden, ohne dass zwischen Transformationen angegeben werden. Die Medien Sitzung verwendet das topologielademobjekt zum Auflösen der Topologie. Nachdem eine Topologie aufgelöst wurde, werden die erforderlichen Decoder und andere Transformations Knoten hinzugefügt. Die Sequencer-Quelle kann auch vollständige Topologien enthalten.

Verwenden Sie zum Erstellen des topologieobjekts die [**mfkreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) -Funktion, und verwenden Sie dann die [**imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) -Schnittstelle zum Erstellen von streamknoten.

Umfassende Anweisungen zur Verwendung dieser Programmier Elemente zum Erstellen von Topologien finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).

Eine Anwendung kann einen ausgewählten Teil der systemeigenen Quelle wiedergeben, indem der Quellknoten konfiguriert wird. Legen Sie zu diesem Zweck das [**MF- \_ toponode \_ mediastart**](mf-toponode-mediastart-attribute.md) -Attribut und das [**MF- \_ toponode \_ mediastop**](mf-toponode-mediastop-attribute.md) -Attribut auf den Knoten der Knoten Topologie der **MF- \_ Topologie \_ \_** fest. Geben Sie die Start Zeit des Mediums und die Endzeit des Mediums in Bezug auf den Start der systemeigenen Quelle als **UINT64** -Typen an.

## <a name="adding-topologies-to-the-sequencer-source"></a>Hinzufügen von Topologien zur Sequencer-Quelle

Fügen Sie als nächstes die partiellen Topologien, die Sie erstellt haben, der Sequencer-Quelle hinzu. Jedem Sequence-Element, das als *Segment* bezeichnet wird, wird ein **mfsequencerelementid-** Bezeichner zugewiesen. Weitere Informationen zum Verwalten von Topologien durch die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).

Nachdem alle Topologien der Sequencer-Quelle hinzugefügt wurden, muss die Anwendung das letzte Segment in der Sequenz markieren, um die Wiedergabe in der Pipeline beenden zu können. Ohne dieses Flag erwartet die Sequencer-Quelle, dass weitere Topologien hinzugefügt werden.

1.  Wenden Sie die [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Methode an, um der Sequencer-Quelle eine bestimmte Topologie hinzuzufügen.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**Appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) fügt der Sequenz die angegebene Topologie hinzu. Diese Methode gibt den Segment Bezeichner im *pdwid-* Parameter zurück.

    Wenn die Topologie die letzte in der Sequencer-Quelle ist, übergeben Sie sequencertopologyflags \_ zuletzt im *dwFlags* -Parameter. Dieser Wert wird in der [**MF sequencertopologyflags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) -Enumeration definiert.

2.  Aufrufen von [**imfsequencersource:: updatetopologyflags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) zum Aktualisieren der Flags für die Topologie, die dem Segment Bezeichner in der Eingabeliste zugeordnet ist. In diesem Fall gibt der-Befehl an, dass es sich bei dem angegebenen Segment um das letzte Segment im Sequencer handelt. (Dieser-Befehl ist optional, wenn die letzte Topologie im [**appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Befehl angegeben wird.)

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

    

Die Anwendung kann die Topologie eines Segments durch eine andere Topologie ersetzen, indem Sie die [**imfsequencersource:: updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) aufrufen und die neue Topologie in *ptopology* übergibt. Wenn neue Native Quellen in der neuen Topologie vorhanden sind, werden die Quellen dem Quell Cache hinzugefügt. Die vorab Liste wird ebenfalls aktualisiert.

## <a name="setting-the-first-topology-on-the-media-session"></a>Festlegen der ersten Topologie in der Medien Sitzung

Als Nächstes stellen Sie die erste Topologie in der Sequenz Quelle in der Medien Sitzung in die Warteschlange. Wenn Sie die erste Topologie aus der Sequencer-Quelle abrufen möchten, muss die Anwendung die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen. Diese Methode gibt die partielle Topologie zurück, die von der Medien Sitzung aufgelöst wird.

Weitere Informationen zu partiellen Topologien finden Sie unter Informationen [zu Topologien](about-topologies.md).

1.  Rufen Sie die native Medienquelle für die erste Topologie der Sequenz Quelle ab.
2.  Erstellen Sie einen Präsentations Deskriptor für die Medienquelle, indem Sie die [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) -Methode aufrufen.
3.  Rufen Sie die zugehörige Topologie für die Präsentation ab, indem Sie die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen.
4.  Legen Sie die erste Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)fest.

    Aufrufen der [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , bei der der *dwsettopologyflags* -Parameter auf **null** festgelegt ist. Dies weist die Medien Sitzung an, die angegebene Topologie zu starten, wenn die aktuelle Topologie abgeschlossen wurde. Da in diesem Fall die angegebene Topologie die erste Topologie ist und keine aktuelle Präsentation vorhanden ist, startet die Medien Sitzung die neue Präsentation sofort.

    Der **null** -Wert gibt auch an, dass die Medien Sitzung die Topologie auflösen muss, da die vom topologieanbieter zurückgegebene Topologie immer eine partielle Topologie ist.


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



## <a name="queuing-the-next-topology-on-the-media-session"></a>Nächste Topologie in der Medien Sitzung in die Warteschlange eingereiht

Als nächstes muss die Anwendung das [menewpresentation](menewpresentation.md) -Ereignis behandeln.

Die Sequencer-Quelle löst [menewpresentation](menewpresentation.md) aus, wenn die Medien Sitzung mit der Wiedergabe eines Segments beginnt, dem ein anderes Segment folgt. Dieses Ereignis informiert die Anwendung über die nächste Topologie in der Sequenz Quelle, indem Sie den Präsentations Deskriptor für das nächste Segment in der vorab Liste bereitstellt. Die Anwendung muss die zugeordnete Topologie mit dem topologieanbieter abrufen und in der Medien Sitzung in eine Warteschlange stellen. Die Sequencer-Quelle stellt dann eine Vorabversion dieser Topologie dar, wodurch ein nahtloser Übergang zwischen Präsentationen sichergestellt wird.

Wenn die Anwendung über Segmente hinweg sucht, empfängt die Anwendung mehrere [menewpresentation](menewpresentation.md) -Ereignisse, da die Sequencer-Quelle die vorab Liste aktualisiert und die richtige Topologie einrichtet. Die Anwendung muss jedes Ereignis verarbeiten und die in den Ereignisdaten zurückgegebene Topologie in der Medien Sitzung in die Warteschlange stellen. Weitere Informationen zum Überspringen von Segmenten finden [Sie unter Verwenden der Sequencer-Quelle](using-the-sequencer-source.md).

Informationen zum erhalten von Sequencer-Quell Benachrichtigungen finden Sie unter [Sequencer](sequencer-source-events.md)-Quell Ereignisse.

1.  Rufen Sie im [menewpresentation](menewpresentation.md) -Ereignishandler den Präsentations Deskriptor für das nächste Segment aus den Ereignisdaten ab.
2.  Rufen Sie die zugehörige Topologie für die Präsentation ab, indem Sie die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen.
3.  Legen Sie die Topologie für die Medien Sitzung fest, indem Sie die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode aufrufen.

    Die Medien Sitzung startet die neue Präsentation, wenn die aktuelle Präsentation abgeschlossen ist.


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



## <a name="releasing-the-sequencer-source"></a>Freigeben der Sequencer-Quelle

Beenden Sie abschließend die Sequencer-Quelle. Dazu können Sie die [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) -Methode für die Sequencer-Quelle verwenden. Durch diesen aufzurufenden Befehl werden alle zugrunde liegenden systemeigenen Medienquellen in der Sequencer-Quelle heruntergefahren.

Nachdem die Sequencer-Quelle freigegeben wurde, sollte die Anwendung die Medien Sitzung schließen und beenden, indem [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) und [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)in dieser Reihenfolge aufgerufen wird.

Um Speicher Verluste zu vermeiden, muss die Anwendung Zeiger auf Media Foundation-Schnittstellen freigeben, wenn Sie nicht mehr benötigt werden.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie eine einfache Wiedergabeliste mithilfe der Sequencer-Quelle erstellt wird. Nachdem Sie die Wiedergabeliste erstellt haben, können Sie erweiterte Funktionen hinzufügen, wie z. b. das Überspringen von Segmenten, das Ändern des Wiedergabe Zustands und das Suchen innerhalb eines Segments. In der folgenden Liste finden Sie Links zu den verwandten Themen:

-   [Steuern von Präsentations Zuständen](how-to-control-presentation-states.md): die Sequencer-Quelle basiert auf der Medien Sitzung, um die Transportsteuerung wie, wiedergeben, anhalten und stoppen bereitzustellen.
-   [In diesem](how-to-perform-scrubbing.md) Thema werden die Schritte beschrieben, die erforderlich sind, um eine bestimmte Position in einem Stream zu suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 



