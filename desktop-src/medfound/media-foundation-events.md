---
description: Ereignisse Media Foundation
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Ereignisse Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a63beeb3222ffef4151f45be95d13f9cf9ff4f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363022"
---
# <a name="media-foundation-events"></a>Ereignisse Media Foundation



| Ereignis                                                                                        | BESCHREIBUNG                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Meaudiosessiondeviceremoved](meaudiosessiondeviceremoved.md)                               | Das Audiogerät wurde entfernt.                                                                                                                            |
| [Meaudiosessiontrennt](meaudiosessiondisconnected.md)                                 | Die Audiositzung wurde von einer Windows-Terminal Dienste-Sitzung getrennt.                                                                              |
| [Meaudiosessionexclusivemodeoverride](meaudiosessionexclusivemodeoverride.md)               | Die Audiositzung wurde durch eine Verbindung im exklusiven Modus vorzeitig entfernt.                                                                                         |
| [Meaudiosessionformatchanged](meaudiosessionformatchanged.md)                               | Das Standard Audioformat für das Audiogerät wurde geändert.                                                                                                   |
| [Meaudiosessiongroupingparamchanged](meaudiosessiongroupingparamchanged.md)                 | Die Gruppierungs Parameter für die Audiositzung wurden geändert.                                                                                                   |
| [Meaudiosessionieschanged](meaudiosessioniconchanged.md)                                   | Das Symbol für die Audiositzung wurde geändert.                                                                                                                          |
| [Meaudiosessionnamechanged](meaudiosessionnamechanged.md)                                   | Der Anzeige Name der Audiositzung wurde geändert.                                                                                                                  |
| [Meaudiosessionservershutdown](meaudiosessionservershutdown.md)                             | Das Windows-Audioserver-System wurde heruntergefahren.                                                                                                           |
| [Meaudiosessionvolumechaning](meaudiosessionvolumechanged.md)                               | Das Volume oder der stumm Zustand der Audiositzung wurde geändert.                                                                                                    |
| [Mebufferingstarted](mebufferingstarted.md)                                                 | Eine Medienquelle hat mit dem Puffern von Daten begonnen.                                                                                                                   |
| [Mebufferingbeendet](mebufferingstopped.md)                                                 | Eine Medienquelle hat das Puffern von Daten beendet.                                                                                                                   |
| [Mecaptureaudiosessiondeviceremoved](mecaptureaudiosessiondeviceremoved.md)                 | Das Gerät wurde entfernt.                                                                                                                                  |
| [Mecaptureaudiosessiontrennt](mecaptureaudiosessiondisconnected.md)                   | Die Verbindung mit der Audiositzung wird getrennt, da sich der Benutzer von einer Windows-Terminal Dienste-Sitzung (WTS) abgemeldet hat.                                            |
| [Mecaptureaudiosessionexclusivemodeoverride](mecaptureaudiosessionexclusivemodeoverride.md) | Der Benutzer hat einen Audiostream im exklusiven Modus geöffnet.                                                                                                       |
| [Mecaptureaudiosessionformatchanged](mecaptureaudiosessionformatchanged.md)                 | Das Audioformat wurde geändert.                                                                                                                                |
| [Mecaptureaudiosessionservershutdown](mecaptureaudiosessionservershutdown.md)               | Der audiositzungsserver wurde heruntergefahren.                                                                                                                       |
| [Mecaptureaudiosessionvolumechaning](mecaptureaudiosessionvolumechanged.md)                 | Das Volume wurde geändert.                                                                                                                                      |
| [Meconnectend](meconnectend.md)                                                             | Die Netzwerkquelle hat das Öffnen einer URL beendet.                                                                                                               |
| [Meconnectstart](meconnectstart.md)                                                         | Die Netzwerkquelle hat mit dem Öffnen einer URL begonnen.                                                                                                                |
| [Mecontentschutzmessage](mecontentprotectionmessage.md)                                 | Die Konfiguration wurde für ein Ausgabe Schutzschema geändert.                                                                                               |
| [Meenablerabgeschlossene](meenablercompleted.md)                                                 | Die Aktion eines inhaltsenabler-Objekts ist fertiggestellt.                                                                                                           |
| [Meenablerprogress](meenablerprogress.md)                                                   | Signalisiert den Fortschritt eines Inhalts Wegbereiter-Objekts.                                                                                                        |
| [Meendof Presentation](meendofpresentation.md)                                               | Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet.                                                                                                       |
| [Meendof presentationsegment](meendofpresentationsegment.md)                                 | Wird von der Sequencer-Quelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment.                                                           |
| [Meendof-Stream](meendofstream.md)                                                           | Wird von einem Mediendaten Strom ausgelöst, wenn der Stream endet.                                                                                                           |
| [Meerror](meerror.md)                                                                       | Signalisiert einen schwerwiegenden Fehler.                                                                                                                                 |
| [Meextendedtype](meextendedtype.md)                                                         | Benutzerdefinierter Ereignistyp.                                                                                                                                       |
| [Meindividualizationabgeschlossen](meindividualizationcompleted.md)                             | Die Individualisierung ist fertiggestellt.                                                                                                                           |
| [Meindividualizationstart](meindividualizationstart.md)                                     | Die Individualisierung beginnt in Kürze.                                                                                                                     |
| [Melicenabacquisitionabgeschlossene](melicenseacquisitioncompleted.md)                           | Der Lizenzerwerb ist fertiggestellt.                                                                                                                         |
| [Melicenmenacquisitionstart](melicenseacquisitionstart.md)                                   | Der Lizenzerwerb beginnt in Kürze.                                                                                                                   |
| [Memediasample](memediasample.md)                                                           | Wird ausgelöst, wenn ein Mediendaten Strom ein neues Beispiel liefert.                                                                                                        |
| [Menewpresentation](menewpresentation.md)                                                   | Durch eine Medienquelle ausgelöst, ist eine neue Präsentation bereit.                                                                                                    |
| [Menewstream](menewstream.md)                                                               | Wird durch eine Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.                                                                                                    |
| [Menonfatalerror](menonfatalerror.md)                                                       | Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten.                                                                                                             |
| [Mepolicychanged](mepolicychanged.md)                                                       | Die Ausgabe Richtlinie für einen Stream wurde geändert.                                                                                                                  |
| [Mepolicyerror](mepolicyerror.md)                                                           | Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgabe Richtlinie ein Fehler auftritt.                                                                         |
| [Mepolicyreport](mepolicyreport.md)                                                         | Enthält Statusinformationen zur Durchsetzung einer Ausgabe Richtlinie.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Die [**IMF outputtrustauthority:: setpolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) -Methode wurde abgeschlossen.                                                    |
| [Mequalitynotify](mequalitynotify.md)                                                       | Bietet Feedback zur Wiedergabequalität für den Quality Manager.                                                                                         |
| [Mereconnectend](mereconnectend.md)                                                         | Ausgelöst durch eine Medienquelle am Ende eines erneuten Verbindungsversuchs.                                                                                           |
| [Mereconnectstart](mereconnectstart.md)                                                     | Ausgelöst durch eine Medienquelle zu Beginn eines erneuten Verbindungsversuchs.                                                                                         |
| [Merendererevent](merendererevent.md)                                                       | Wird vom erweiterten Videorenderer (EVR) ausgelöst, wenn ein Benutzer Ereignis vom Präsentator empfangen wird.                                                            |
| [Mesequendcersourcetopologyupdate](mesequencersourcetopologyupdated.md)                     | Wird von der Sequencer-Quelle ausgelöst, wenn die [**IMF sequencersource:: updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) -Methode asynchron abgeschlossen wird. |
| [Mesessioncapabilitieschge](mesessioncapabilitieschanged.md)                             | Wird von der Medien Sitzung ausgelöst, wenn sich die Sitzungs Funktionen ändern.                                                                                        |
| [Mesessionclosed](mesessionclosed.md)                                                       | Wird ausgelöst, wenn die [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) -Methode asynchron abgeschlossen wird.                                                 |
| [Mesessionend](mesessionended.md)                                                         | Wird von der Medien Sitzung ausgelöst, wenn die Wiedergabe der letzten Präsentation in der Wiedergabe Warteschlange abgeschlossen ist.                                                    |
| [Mesessionnotifypresentationtime](mesessionnotifypresentationtime.md)                       | Wird von der Medien Sitzung ausgelöst, wenn eine neue Präsentation gestartet wird.                                                                                              |
| [Mesessionangeh alten](mesessionpaused.md)                                                       | Wird ausgelöst, wenn die [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) -Methode asynchron abgeschlossen wird.                                                 |
| [Mesessionratechanged](mesessionratechanged.md)                                             | Wird von der Medien Sitzung ausgelöst, wenn sich die Wiedergabe Rate ändert.                                                                                              |
| [Mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md)                             | Wird von der Medien Sitzung ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.                                                                                       |
| [Mesessionstarted](mesessionstarted.md)                                                     | Wird ausgelöst, wenn die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode asynchron abgeschlossen wird.                                                 |
| [Mesessionbeendet](mesessionstopped.md)                                                     | Wird ausgelöst, wenn die [**imfmediasession:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) -Methode asynchron abgeschlossen wird.                                                   |
| [Mesessionstreamsinkformatchanged](mesessionstreamsinkformatchanged.md)                     | Wird von der Medien Sitzung ausgelöst, wenn sich das Format in einer Medien Senke ändert.                                                                                     |
| [Mesessiontopologiesgelöscht](mesessiontopologiescleared.md)                                 | Wird von der Medien Sitzung ausgelöst, wenn die [**imfmediasession:: cleartopologien**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) -Methode asynchron abgeschlossen wird.        |
| [Mesessiontopologyset](mesessiontopologyset.md)                                             | Wird ausgelöst, nachdem die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode asynchron abgeschlossen wurde.                                     |
| [Mesessiontopologystatus](mesessiontopologystatus.md)                                       | Wird von der Medien Sitzung ausgelöst, wenn sich der Status einer Topologie ändert.                                                                                       |
| [Mesinkinvalidieren](mesinkinvalidated.md)                                                   | Wird ausgelöst, wenn eine Medien Senke ungültig wird.                                                                                                                |
| [Mesourcecharakteristicschge](mesourcecharacteristicschanged.md)                         | Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quelle ändern.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.                                                                                                   |
| [Mesourcepaused](mesourcepaused.md)                                                         | Wird von einer Medienquelle ausgelöst, wenn die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode asynchron abgeschlossen wird.                                 |
| [Mesourceratechanged](mesourceratechanged.md)                                               | Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergabe Rate ändert.                                                                                                 |
| [Mesourceratechangerequitessiert](mesourceratechangerequested.md)                               | Wird von einer Medienquelle ausgelöst, um eine neue Wiedergabe Rate anzufordern.                                                                                                 |
| [Mesourceseeked](mesourceseeked.md)                                                         | Wird ausgelöst, wenn eine Medienquelle eine neue Position ansucht.                                                                                                      |
| [Mesourcestarted](mesourcestarted.md)                                                       | Wird ausgelöst, wenn eine Medienquelle startet, ohne zu suchen.                                                                                                       |
| [Mesourcestpt](mesourcestopped.md)                                                       | Wird von einer Medienquelle ausgelöst, wenn die [**imfmediasource:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode asynchron abgeschlossen wird.                                   |
| [Mestreamformatchanged](mestreamformatchanged.md)                                           | Wird von einem Mediendaten Strom ausgelöst, wenn sich der Medientyp des Streams ändert.                                                                                      |
| [Mestreampaused](mestreampaused.md)                                                         | Wird von einem Medienstream ausgelöst, wenn die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode asynchron abgeschlossen wird.                                 |
| [Mestreamseeked](mestreamseeked.md)                                                         | Wird von einem Mediendaten Strom nach einem [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Rückruf ausgelöst und bewirkt eine Suche im Stream.                              |
| [Mestreamsinkdevicechanged](mestreamsinkdevicechanged.md)                                   | Wird von den streamsenken des EVR ausgelöst, wenn sich das Videogerät ändert.                                                                                       |
| [Mestreamsinkformatchanged](mestreamsinkformatchanged.md)                                   | Wird durch eine streamsenke ausgelöst, wenn der Medientyp der Senke nicht mehr gültig ist.                                                                                   |
| [Mestreamsink Marker](mestreamsinkmarker.md)                                                 | Wird durch eine streamsenke ausgelöst, nachdem die [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode aufgerufen wurde.                                      |
| [Mestreamsink angehalten](mestreamsinkpaused.md)                                                 | Wird durch eine streamsenke ausgelöst, wenn der Übergang zum angehaltenen Zustand abgeschlossen wird.                                                                            |
| [Mestreamsinkprerolled](mestreamsinkprerolled.md)                                           | Wird durch eine streamsenke ausgelöst, wenn der Stream genügend vorab Daten empfangen hat, um das Rendering zu beginnen.                                                             |
| [Mestreamsinkratechanged](mestreamsinkratechanged.md)                                       | Wird von einer streamsenke ausgelöst, wenn sich die Rate geändert hat.                                                                                                       |
| [Mestreamsinkrequestsample](mestreamsinkrequestsample.md)                                   | Wird von einer streamsenke ausgelöst, um ein neues Medien Beispiel aus der Pipeline anzufordern.                                                                                 |
| [Mestreamsinkscrubsamplecomplete](mestreamsinkscrubsamplecomplete.md)                       | Wird durch eine streamsenke ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.                                                                                           |
| [Mestreamsink Started](mestreamsinkstarted.md)                                               | Wird durch eine streamsenke ausgelöst, wenn der Übergang in den Status "wird ausgeführt" versetzt wird.                                                                           |
| [Mestreamsink beendet](mestreamsinkstopped.md)                                               | Wird durch eine streamsenke ausgelöst, wenn der Übergang zum beendeten Zustand abgeschlossen wird.                                                                           |
| [Mestreamstarted](mestreamstarted.md)                                                       | Wird von einem Medienstrom ausgelöst, wenn die Quelle startet, ohne zu suchen.                                                                                         |
| [Mestreambeendet](mestreamstopped.md)                                                       | Wird von einem Mediendaten Strom ausgelöst, wenn die [**imfmediasource:: beenden**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode asynchron abgeschlossen wird.                                   |
| [Mestreamthinmode](mestreamthinmode.md)                                                     | Wird von einem Medienstream ausgelöst, wenn der Stream gestartet oder beendet wird.                                                                                    |
| [Mestreamtick](mestreamtick.md)                                                             | Signalisiert, dass für einen Mediendaten Strom keine Daten zu einem angegebenen Zeitpunkt verfügbar sind.                                                                            |
| [Metransformdraunvollständig](metransformdraincomplete.md)                                     | Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn ein Ausgleichs Vorgang beendet ist.                                                             |
| [Metransformhaveoutput](metransformhaveoutput.md)                                           | Wird von einem asynchronen MFT gesendet, wenn neue Ausgabedaten aus dem MFT verfügbar sind.                                                                              |
| [Metransformmarker](metransformmarker.md)                                                   | Wird von einem asynchronen MFT als Antwort auf eine [**MFT- \_ Nachrichten \_ Befehls \_ markernachricht**](mft-message-command-marker.md) gesendet.                               |
| [Metransformneedinput](metransformneedinput.md)                                             | Wird von einem asynchronen MFT gesendet, um ein neues Eingabe Beispiel anzufordern.                                                                                               |
| [Meunknown](meunknown.md)                                                                   | Unbekannter Ereignistyp.                                                                                                                                      |
| [Meupdatedstream](meupdatedstream.md)                                                       | Wird von einer Medienquelle ausgelöst, wenn Sie neu gestartet wird oder einen Datenstrom sucht, der bereits aktiv ist.                                                                      |
| [Mevideocapturedevicepreempted](mevideocapturedevicepreempted.md)                           | Das Gerät wurde vorzeitig entfernt.                                                                                                                           |
| [Mevideocapturedeviceremoved](mevideocapturedeviceremoved.md)                               | Das Gerät wurde entfernt.                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> <dt>

[Medienereignis Generatoren](media-event-generators.md)
</dt> <dt>

[**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



