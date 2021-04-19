---
description: In diesem Thema wird beschrieben, wie die Sequencer-Quelle verwendet wird.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Verwenden der Sequencer-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356574"
---
# <a name="using-the-sequencer-source"></a>Verwenden der Sequencer-Quelle

In diesem Thema wird beschrieben, wie die [Sequencer-Quelle](sequencer-source.md)verwendet wird. Sie enthält die folgenden Abschnitte:

-   [Übersicht](#overview)
-   [Hinzufügen von Topologien](#adding-topologies)
-   [Löschen von Topologien](#deleting-topologies)
-   [Überspringen zu einem Segment](#skipping-to-a-segment)
-   [Zugehörige Themen](#related-topics)

Eine allgemeine Übersicht über die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).

## <a name="overview"></a>Übersicht

Die Sequencer-Quelle macht die folgenden Schnittstellen verfügbar.



| Schnittstelle                                                                        | BESCHREIBUNG                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | Macht Funktionen der generischen Medienquelle verfügbar.                                        |
| [**IMF sequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | Ermöglicht es der Anwendung, Topologien hinzuzufügen oder zu entfernen.                               |
| [**Imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | Ruft die nächste Topologie in die Warteschlange für die Medien Sitzung ab.                         |
| [**Imfmediasourcepresentationprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | Wird von der Medien Sitzung zum Beenden von Segmenten verwendet. Diese Schnittstelle wird von Anwendungen nicht verwendet. |
| [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | Fragt die Sequencer-Quelle für [Dienst Schnittstellen](service-interfaces.md)ab.     |



 

Führen Sie die folgenden Schritte aus, um eine Sequenz von Medienquellen wiederzugeben:

1.  Um die Sequencer-Quelle zu erstellen, rufen Sie die [**mfkreatesequencersource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) -Funktion auf.
2.  Erstellen Sie für jedes Segment eine Wiedergabe Topologie, wie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md)beschrieben. Um der Präsentation die Topologie hinzuzufügen, nennen Sie [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).
3.  Bevor Sie die Wiedergabe starten, müssen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Sequencer-Quelle aufrufen. Diese Methode gibt einen Zeiger auf einen Präsentations Deskriptor für das erste Segment zurück. Um die diesem Segment zugeordnete Topologie abzurufen, nennen Sie **QueryInterface** in der Sequencer-Quelle für die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle. Übergeben Sie den Präsentations Deskriptor an die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode. Diese Methode gibt einen Zeiger auf die Topologie zurück.
4.  Übergeben Sie die Topologie für das erste Segment an die Medien Sitzung, indem Sie die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode der Medien Sitzung aufrufen.
5.  Wiedergabe durch Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)starten.
6.  Wenn die Sequencer-Quelle für das vorab Ausführen des nächsten Segments bereit ist, sendet Sie ein [menewpresentation](menewpresentation.md) -Ereignis, dessen Ereignisdaten ein [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstellen Zeiger ist. Rufen Sie die Topologie für das Segment ab, indem Sie [**getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) für die Sequencer-Quelle aufrufen, und legen Sie die Topologie für die Medien Sitzung fest, indem Sie [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen. Die Medienquelle muss nicht neu gestartet werden. Er wird automatisch bis zum nächsten Segment durchgespielt.
7.  Bevor die Anwendung beendet wird, fahren Sie die Sequencer-Quelle durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)herunter.

Der folgende Code zeigt, wie Sie die Topologie erhalten und in der Medien Sitzung festlegen:


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



Ein umfassendes Codebeispiel finden Sie unter [Beispielcode für die Sequencer-Quelle](sequencer-source-example-code.md).

## <a name="adding-topologies"></a>Hinzufügen von Topologien

Die Sequencer-Quelle verwaltet zwei Listen von Topologien: die *Eingabeliste* und die *vorab Liste*.

Die Eingabeliste ist eine Auflistung von Topologien, die Wiedergabelisten Segmenten entsprechen, in der Reihenfolge, in der Sie durch die Anwendung hinzugefügt wurden, indem [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)aufgerufen wurde. Diese Methode weist jeder Topologie einen eindeutigen *Segment Bezeichner* des Typs **MF sequencerelementid** zu. Der Segment Bezeichner wird als Attribut für alle Knoten der Quell Topologie festgelegt. Eine Anwendung kann den Segment Bezeichner von einem Quellknoten mit dem [Element "MF \_ toponode \_ Sequence \_ elementId](mf-toponode-sequence-elementid-attribute.md) " erhalten. Die Eingabeliste kann doppelte Topologien aufweisen, wenn die Anwendung **appendtopology** mehrmals in derselben Topologie aufrief. Sie werden jedoch durch Ihre eindeutigen Segment Bezeichner identifiziert.

Die ein Vorlauf ausgeführt-Liste ist eine Auflistung von Eingabe Listen Topologien, die zur Vorbereitung der Wiedergabe initialisiert wurden. Dies ermöglicht es der Medien Sitzung, nahtlos zur nächsten Topologie zu wechseln, wenn die aktive Topologie endet. Die Anwendung kann keine Topologien direkt aus der ein Vorlauf ausgeführt-Liste hinzufügen oder entfernen. Sie wird von der Sequencer-Quelle generiert, wenn eine Topologie aus der Eingabeliste für die Wiedergabe ausgewählt wird. Dies bewirkt, dass die Sequencer-Quelle die nächste Topologie aus der Eingabeliste der ein Vorlauf ausgeführt-Liste hinzufügt. Danach löst die Sequencer-Quelle das Ereignis " [menewpresentation](menewpresentation.md) " asynchron aus und übergibt den Präsentations Deskriptor für die ein Vorlauf ausgeführt-Topologie als Ereignisdaten. Die Anwendung muss dieses Ereignis überwachen, indem Sie die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medien Sitzung verwendet und die ein Vorlauf ausgeführt-Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in die Warteschlange eingereiht. Dies muss erfolgen, bevor die Wiedergabe der aktiven Topologie in der Medien Sitzung abgeschlossen ist. Die **settopologie** informiert die Medien Sitzung über die nächste Topologie, die Sie wiedergeben muss, nachdem die Wiedergabe der aktiven Topologie beendet wurde. Um eine nahtlose treansition sicherzustellen, muss die Anwendung **settopology** aufzurufen, bevor die Medien Sitzung die Wiedergabe der vorherigen Topologie abschließt. Andernfalls besteht eine Lücke zwischen den Segmenten.

Das [menewpresentation](menewpresentation.md) -Ereignis wird ausgelöst, solange eine Topologie vorhanden ist, die der aktiven Topologie folgt. Folglich wird dieses Ereignis nicht ausgelöst, wenn die Eingabeliste nur eine Topologie enthält oder wenn es sich bei der aktiven Topologie um das letzte in der Eingabeliste handelt.

Die vorab Liste ist mit der Eingabeliste synchronisiert und wird jedes Mal aktualisiert, wenn der Eingabeliste eine Topologie hinzugefügt oder aus ihr gelöscht wird.

## <a name="deleting-topologies"></a>Löschen von Topologien

Um eine Topologie aus der Sequencer-Quelle zu entfernen, muss eine Anwendung die [**imfsequencersource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) -Methode abrufen und den Segment Bezeichner angeben.

Bevor [**deletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)aufgerufen wird, muss die Anwendung sicherstellen, dass die Medien Sitzung nicht die Topologie verwendet, die von der Anwendung gelöscht werden soll. Zu diesem Zweck müssen die beiden folgenden Punkte auftreten, bevor die Anwendung **deletetopology** aufruft:

-   Das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit der "MF \_ topostatus" \_ wurde für die Topologie empfangen, um sicherzustellen, dass die Wiedergabe der Medien Sitzung abgeschlossen ist

-   [Mesessiontopologystatus](mesessiontopologystatus.md) mit \_ der von MF topostatus \_ gestartete \_ Quelle wird für die nächste Topologie empfangen, um sicherzustellen, dass die Medien Sitzung mit der nächsten Topologie begonnen hat. das [mesessionend](mesessionended.md) -Ereignis wird empfangen, um sicherzustellen, dass die Medien Sitzung mit der letzten Topologie in der Sequencer-Quelle ausgeführt wird.

Wenn das Segment, das gelöscht wird, die aktive Topologie ist, wird die Wiedergabe angehalten, und die Sequencer-Quelle löst das [meendof presentationsegment](meendofpresentationsegment.md) -Ereignis aus. Wenn die aktive Topologie auch die letzte Topologie ist, wird das [meendof Presentation](meendofpresentation.md) -Ereignis ausgelöst.

## <a name="skipping-to-a-segment"></a>Überspringen zu einem Segment

Eine Anwendung kann mit einem bestimmten Segment in der Sequenz übersprungen werden, indem die [Medien Sitzung](media-session.md) mit einem Segment Offset wie folgt gestartet wird:

1.  Rufen Sie die [**mfkreatesequencersegmentoffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) -Funktion auf, um den Segment Offset zu erstellen. Geben Sie den Bezeichner des Segments im *dwID* -Parameter an. (Der Bezeichner wurde von der [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Methode zurückgegeben, als Sie die Topologie zum ersten Mal der Sequencer-Quelle hinzugefügt haben.) Der *hnsoffset* -Parameter gibt einen Zeit Offset relativ zum Anfang des Segments an. Die Wiedergabe wird zu diesem Zeitpunkt gestartet. Übergeben Sie für den *pvarsegmentoffset* -Parameter die Adresse eines leeren **PROPVARIANT**-Parameters. Wenn die Funktion zurückgegeben wird, enthält diese **PROPVARIANT** den Segment Offset.

2.  Nennen Sie die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode für die Medien Sitzung. Verwenden Sie für den *pguidtimeformat* -Parameter den GUID-Wert MF- \_ Zeit \_ Format \_ Segment \_ Offset. Dieser Wert gibt die Suche nach Segment Offset an. Übergeben Sie für den *pvarstartposition* -Parameter die Adresse der im vorherigen Schritt erstellten **PROPVARIANT** .

Im folgenden Codebeispiel wird veranschaulicht, wie mit dem Anfang eines angegebenen Segments in einer Sequenz übersprungen wird.


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



Wenn die Anwendung über Segmente hinweg sucht, empfängt die Anwendung mehrere Ereignisse, da die Sequencer-Quelle das aktuelle Segment beendet und die Wiedergabe des neuen Segments vorbereitet. Da diese Ereignisse asynchron empfangen werden, ist es schwierig, die genaue Reihenfolge der Ereignisse vorherzusagen. Diese Ereignisse lauten wie folgt:

-   Die Sequencer-Quelle sendet ein [menewpresentation](menewpresentation.md) -Ereignis für das neue Segment, an das die Medien Sitzung übersprungen wird.

-   Wenn die Sequencer-Quelle das aktive Segment beendet, sendet Sie das [meendofpresentationsegment](meendofpresentationsegment.md) -Ereignis.
-   Die Sequencer-Quelle bricht dann die ein Vorlauf ausgeführt-Topologie ab. Dies führt zu den folgenden Ereignissen für die abgebrochene Topologie:

    -   [Mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem MF- \_ Flag "topostatus \_ Ready".
    -   Das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem \_ \_ quellflag "MF topostatus Started" \_ .
    -   Das [meendofpresentationsegment](meendofpresentationsegment.md) -Ereignis mit der [MF- \_ Ereignis \_ Quell Topologie hat das Attribut \_ \_ abgebrochen](mf-event-source-topology-canceled-attribute.md) , um anzugeben, dass die Topologie von der Sequencer-Quelle abgebrochen wurde.

-   Als nächstes sendet die Sequencer-Quelle Ereignisse für das neue Segment, einschließlich verschiedener [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignisse.
-   Wenn das neue Segment nicht das letzte in der Liste ist, aktualisiert die Sequencer-Quelle die vorab Liste und löst eine weitere [menewpresentation](menewpresentation.md) für die neue ein Vorlauf ausgeführt-Topologie aus. Weitere Informationen zu Topologien in der ein Vorlauf ausgeführt-Liste finden Sie unter Informationen zur [Sequencer-Quelle](about-the-sequencer-source.md).

Weitere Informationen zu den von der Sequencer-Quelle gesendeten Ereignissen finden Sie im Thema [Sequencer-Quell Ereignisse](sequencer-source-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Wiedergabeliste](how-to-create-a-playlist.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 



