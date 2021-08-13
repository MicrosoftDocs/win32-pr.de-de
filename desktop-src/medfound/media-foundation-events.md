---
description: Media Foundation Ereignisse
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Media Foundation Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a922127941bd94103eac9cfb02ef33d1c0b789eb632f2689a3adc81494c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268820"
---
# <a name="media-foundation-events"></a>Media Foundation Ereignisse



| Ereignis                                                                                        | BESCHREIBUNG                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Das Audiogerät wurde entfernt.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | Die Audiositzung wurde von einer Windows-Terminal Services-Sitzung getrennt.                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | Die Audiositzung wurde durch eine Verbindung im exklusiven Modus vorab beendet.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | Das Standardaudioformat für das Audiogerät wurde geändert.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Die Gruppierungsparameter wurden für die Audiositzung geändert.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | Das Audiositzungssymbol wurde geändert.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | Der Anzeigename der Audiositzung wurde geändert.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | Das Windows Audioserversystem wurde heruntergefahren.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | Der Lautstärke- oder Stummschaltungsstatus der Audiositzung wurde geändert.                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Eine Medienquelle wurde gestartet, um Daten zu puffern.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Eine Medienquelle hat die Pufferung von Daten beendet.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | Das Gerät wurde entfernt.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | Die Audiositzung wird getrennt, da sich der Benutzer von einer Windows-Terminal Services-Sitzung (WTS) abgemelgt hat.                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | Der Benutzer hat einen Audiostream im exklusiven Modus geöffnet.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | Das Audioformat wurde geändert.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | Der Audiositzungsserver wird heruntergefahren.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | Das Volume wurde geändert.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | Die Netzwerkquelle hat das Öffnen einer URL beendet.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | Die Netzwerkquelle hat mit dem Öffnen einer URL begonnen.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | Die Konfiguration für ein Ausgabeschutzschema wurde geändert.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | Die Aktion eines Inhaltsermöglichungsobjekts ist abgeschlossen.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Signalisiert den Fortschritt eines Inhalts-Enabler-Objekts.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Wird von der Sequencerquelle ausgelöst, wenn ein Segment abgeschlossen ist und auf das ein anderes Segment folgt.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Wird von einem Medienstream ausgelöst, wenn der Stream endet.                                                                                                           |
| [MEError](meerror.md)                                                                       | Signalisiert einen schwerwiegenden Fehler.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Benutzerdefinierter Ereignistyp.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | Die Individualisierung ist abgeschlossen.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | Die Individualisierung beginnt.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | Der Lizenzerwerb ist abgeschlossen.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | Der Lizenzerwerb beginnt.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Wird ausgelöst, wenn ein Medienstream ein neues Beispiel liefert.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Durch eine Medienquelle ausgelöst, ist eine neue Präsentation bereit.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Wird von einer Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | Die Ausgaberichtlinie für einen Stream wurde geändert.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgaberichtlinie ein Fehler auftritt.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Enthält Statusinformationen zur Erzwingung einer Ausgaberichtlinie.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Die [**METHODE FÜR DIE Vertrauenswürdigkeits-AuthentifizierungSPUTOUTPUTTrustAuthority::SetPolicy wurde**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) abgeschlossen.                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Gibt Dem Quality Manager Feedback zur Wiedergabequalität.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Wird von einer Medienquelle am Ende eines Verbindungsversuchs ausgelöst.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Wird von einer Medienquelle zu Beginn eines Verbindungsversuchs ausgelöst.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Wird vom erweiterten Videorenderer (EVR) ausgelöst, wenn er ein Benutzerereignis vom Moderator empfängt.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Wird von der Sequencerquelle ausgelöst, wenn die [**ASYNCHRONOUSSequencerSource::UpdateTopology-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) asynchron abgeschlossen wird. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Wird von der Mediensitzung ausgelöst, wenn sich die Sitzungsfunktionen ändern.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Wird ausgelöst, [**wenn die ASYNCHRONOUSMediaSession::Close-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) asynchron abgeschlossen wird.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Wird von der Mediensitzung ausgelöst, wenn die Wiedergabe der letzten Präsentation in der Wiedergabewarteschlange abgeschlossen ist.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Wird von der Mediensitzung ausgelöst, wenn eine neue Präsentation beginnt.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Wird ausgelöst, wenn die [**:P ause-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) asynchron abgeschlossen wird.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Wird von der Mediensitzung ausgelöst, wenn sich die Wiedergaberate ändert.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Wird von der Mediensitzung ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Wird ausgelöst, wenn die [**ASYNCHRONOUSMediaSession::Start-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) asynchron abgeschlossen wird.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Wird ausgelöst, wenn die [**ASYNCHRONOUSMediaSession::Stop-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) asynchron abgeschlossen wird.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Wird von der Mediensitzung ausgelöst, wenn sich das Format in einer Mediensenke ändert.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Wird von der Mediensitzung ausgelöst, wenn die [**METHODE VONMEDIASESSION::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) asynchron abgeschlossen wird.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Wird ausgelöst, nachdem die [**METHODE "ASYNCHRONOUSMediaSession::SetTopology"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) asynchron abgeschlossen wurde.                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Wird von der Mediensitzung ausgelöst, wenn sich der Status einer Topologie ändert.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Wird ausgelöst, wenn eine Mediensenke ungültig wird.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quelle ändern.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Wird von einer Medienquelle ausgelöst, wenn die [**METHODE VONMEDIASOURCE::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) asynchron abgeschlossen wird.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergaberate ändert.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Wird von einer Medienquelle ausgelöst, um eine neue Wiedergaberate anzufordern.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Wird ausgelöst, wenn eine Medienquelle an eine neue Position sucht.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Wird ausgelöst, wenn eine Medienquelle ohne Suche gestartet wird.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Wird von einer Medienquelle ausgelöst, wenn die [**METHODE VONMEDIASOURCE::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) asynchron abgeschlossen wird.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Wird von einem Medienstream ausgelöst, wenn sich der Medientyp des Streams ändert.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Wird von einem Medienstream ausgelöst, wenn die [**METHODE "Source::P ause"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) asynchron abgeschlossen wird.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Wird von einem Medienstream nach einem Aufruf von [**SEEKMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ausgelöst, wird eine Suche im Stream ausgelöst.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Wird von den Streamsenken der EVR ausgelöst, wenn sich das Videogerät ändert.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Wird von einer Streamsenke ausgelöst, wenn der Medientyp der Senke nicht mehr gültig ist.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Wird von einer Streamsenke ausgelöst, nachdem die [**METHODE VONSTREAMSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) aufgerufen wurde.                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Wird von einer Streamsenke ausgelöst, wenn der Übergang in den angehaltenen Zustand abgeschlossen ist.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Wird von einer Streamsenke ausgelöst, wenn der Stream genügend Vorabrolldaten empfangen hat, um mit dem Rendern zu beginnen.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Wird von einer Streamsenke ausgelöst, wenn sich die Rate geändert hat.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Wird von einer Streamsenke ausgelöst, um ein neues Medienbeispiel aus der Pipeline anzufordern.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Wird von einer Streamsenke ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Wird von einer Streamsenke ausgelöst, wenn der Übergang in den Ausführungszustand abgeschlossen ist.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Wird von einer Streamsenke ausgelöst, wenn der Übergang in den Zustand "Beendet" abgeschlossen ist.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Wird von einem Medienstream ausgelöst, wenn die Quelle ohne Suche gestartet wird.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Wird von einem Mediendatenstrom ausgelöst, wenn die [**METHODE VONMEDIASOURCE::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) asynchron abgeschlossen wird.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Wird von einem Medienstream ausgelöst, wenn er den Stream startet oder beendet.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Signalisiert, dass für einen Medienstream zu einem bestimmten Zeitpunkt keine Daten verfügbar sind.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Wird von einer asynchronen Media Foundation Transformation (MFT) gesendet, wenn ein Entleerungsvorgang abgeschlossen ist.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Wird von einem asynchronen MFT gesendet, wenn neue Ausgabedaten aus dem MFT verfügbar sind.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Wird von einem asynchronen MFT als Reaktion auf eine [**MFT \_ MESSAGE COMMAND \_ \_ MARKER-Nachricht**](mft-message-command-marker.md) gesendet.                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Wird von einem asynchronen MFT gesendet, um ein neues Eingabebeispiel anzufordern.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Unbekannter Ereignistyp.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Wird von einer Medienquelle ausgelöst, wenn ein bereits aktiver Stream neu gestartet oder gesucht wird.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | Das Gerät wurde vorzeitig beendet.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | Das Gerät wurde entfernt.                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> <dt>

[Medienereignisgeneratoren](media-event-generators.md)
</dt> <dt>

[**WFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



