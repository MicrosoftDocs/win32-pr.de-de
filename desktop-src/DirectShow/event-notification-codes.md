---
description: Ereignisbenachrichtigungscodes
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Ereignisbenachrichtigungscodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54792e433535ceefad416033d7758f4398b7777951173256c9be9b83913d61f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015788"
---
# <a name="event-notification-codes"></a>Ereignisbenachrichtigungscodes

In diesem Abschnitt werden die DirectShow-Ereignisse aufgelistet, die nicht dvdspezifisch sind. Informationen zu DVD-spezifischen Ereignissen finden Sie unter [DVD-Ereignisbenachrichtigungscodes.](dvd-notification-codes.md)

Filter senden Ereignisse an den Filter Graph Manager, indem sie die [**IMediaEventSink::Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) aufrufen. Der Filter Graph Manager verarbeitet einige Ereignisse und Warteschlangen für die Anwendung. Die Anwendung ruft sie durch Aufrufen der [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ab.

In den folgenden Abschnitten listet jeder Eintrag den Ereigniscode, die Bedeutung der Ereignisparameter und ggf. die Standardaktion Filter Graph Manager für das Ereignis auf. Um die Standardaktion zu überschreiben, rufen [**Sie IMediaEvent::CancelDefaultHandling auf.**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) Ereigniscodes werden in den Headerdateien Evcode.h und Audevcod.h definiert. Wenn keine Standardaktion vorhanden ist, leitet der Filter Graph Manager das Ereignis automatisch an die Anwendung weiter (über die Ereigniswarteschlange).

**Benutzerdefinierte Ereignisse**

Filter können benutzerdefinierte Ereignisse mit Ereigniscodes im Bereich EC \_ USER und höher definieren. Die Filter Graph Manager platzieren diese direkt in der Ereigniswarteschlange. Es gelten jedoch die folgenden Einschränkungen:

-   Der Filter Graph-Manager kann die Ereignisparameter nicht mithilfe der normalen [**IMediaEvent::FreeEventParams-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) freigeben. Die Anwendung muss alle Arbeitsspeicher- oder Verweiszähler freigeben, die den Ereignisparametern zugeordnet sind.
-   Der Filter sollte das Ereignis nur aus einer Anwendung senden, die für die Behandlung des Ereignisses vorbereitet ist. (Möglicherweise kann die Anwendung eine benutzerdefinierte Eigenschaft für den Filter festlegen, um anzugeben, dass das Ereignis sicher gesendet werden kann.)



| Ereignisbenachrichtigungscode                                                 | Beschreibung                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                                     | Ein Videofenster wird aktiviert oder deaktiviert.                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | Wird nicht unterstützt.                                                                                                            |
| [**\_EC-PUFFERUNGSDATEN \_**](ec-buffering-data.md)                        | Das Diagramm puffert Daten oder hat das Puffern von Daten beendet.                                                               |
| [**EC \_ BUILT**](ec-built.md)                                           | Wird vom Videosteuerelement gesendet, wenn ein Diagramm erstellt wurde. Nicht an Anwendungen weitergeleitet.                                     |
| [**\_EC-UHR \_ GEÄNDERT**](ec-clock-changed.md)                          | Die Verweisuhr wurde geändert.                                                                                          |
| [**EC \_ CLOCK \_ UNSET**](ec-clock-unset.md)                              | Der Uhranbieter wurde getrennt.                                                                                      |
| [**EC \_ \_ CODECAPI-EREIGNIS**](ec-codecapi-event.md)                        | Wird von einem Encoder gesendet, um ein Codierungsereignis zu signalisieren.                                                                           |
| [**EC \_ COMPLETE**](ec-complete.md)                                     | Alle Daten aus einem bestimmten Stream wurden gerendert.                                                                      |
| [**\_EC-INHALTEIGENSCHAFT \_ GEÄNDERT**](ec-contentproperty-changed.md)      | Wird nicht unterstützt.                                                                                                            |
| [**\_EC-GERÄT \_ VERLOREN**](ec-device-lost.md)                              | Ein Plug & Play Gerät wurde entfernt oder ist wieder verfügbar.                                                         |
| [**\_EC-ANZEIGE \_ GEÄNDERT**](ec-display-changed.md)                      | Der Anzeigemodus wurde geändert.                                                                                             |
| [**\_EC-ENDE \_ DES \_ SEGMENTS**](ec-end-of-segment.md)                       | Das Ende eines Segments wurde erreicht.                                                                                    |
| [**\_EC-EOS \_ IN KÜRZE**](ec-eos-soon.md)                                    | Wird nicht unterstützt.                                                                                                            |
| [**\_EC-FEHLER \_ WIRD WEITERHIN WIEDERGEGEBEN**](ec-error-stillplaying.md)                | Ein asynchroner Befehl zum Ausführen des Graphen ist fehlgeschlagen.                                                                      |
| [**EC \_ ERRORABORT**](ec-errorabort.md)                                 | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**EC \_ ERRORABORTEX**](ec-errorabortex.md)                             | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**EC \_ EXTDEVICE \_ MODE \_ CHANGE**](ec-extdevice-mode-change.md)         | Wird nicht unterstützt.                                                                                                            |
| [**\_EC-DATEI \_ GESCHLOSSEN**](ec-file-closed.md)                              | Die Quelldatei wurde aufgrund eines unerwarteten Ereignisses geschlossen.                                                                |
| [**\_EC-VOLLBILD \_ VERLOREN**](ec-fullscreen-lost.md)                      | Der Videorenderer wechselt aus dem Vollbildmodus.                                                                  |
| [**EC \_ GRAPH \_ GEÄNDERT**](ec-graph-changed.md)                          | Das Filterdiagramm wurde geändert.                                                                                             |
| [**EC \_ LENGTH CHANGED (EC-LÄNGE \_ GEÄNDERT)**](ec-length-changed.md)                        | Die Länge einer Quelle wurde geändert.                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.                                                         |
| [**\_ \_ EC-MARKERTREFFER**](ec-marker-hit.md)                                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ NEED \_ RESTART**](ec-need-restart.md)                            | Ein Filter fordert an, dass das Diagramm neu gestartet wird.                                                                       |
| [**EC \_ NEW \_ PIN**](ec-new-pin.md)                                      | Wird nicht unterstützt.                                                                                                            |
| [**FENSTER \_ "EC-BENACHRICHTIGUNG" \_**](ec-notify-window.md)                          | Benachrichtigt einen Filter über das Fenster des Videorenderers.                                                                         |
| [**EC \_ \_ OLE-EREIGNIS**](ec-ole-event.md)                                  | Ein Filter übergibt eine Textzeichenfolge an die Anwendung.                                                                     |
| [**EC \_ OPENING \_ FILE**](ec-opening-file.md)                            | Das Diagramm öffnet eine Datei oder hat das Öffnen einer Datei abgeschlossen.                                                              |
| [**EC \_ PALETTE \_ GEÄNDERT**](ec-palette-changed.md)                      | Die Videopalette wurde geändert.                                                                                            |
| [**EC \_ ANGEHALTEN**](ec-paused.md)                                         | Eine Pausenanforderung wurde abgeschlossen.                                                                                            |
| [**EC \_ PLEASE \_ REOPEN**](ec-please-reopen.md)                          | Die Quelldatei wurde geändert.                                                                                              |
| [**EC \_ PREPROCESS \_ COMPLETE**](ec-preprocess-complete.md)              | Wird vom [WM ASF Writer-Filter](wm-asf-writer-filter.md) gesendet, wenn die Vorverarbeitung für multipass-Codierung abgeschlossen ist. |
| [**\_ \_ EC-VERARBEITUNGSLATENZ**](ec-processing-latency.md)                | Gibt den Zeitraum an, den eine Komponente für die Verarbeitung der einzelnen Stichproben nimmt.                                           |
| [**ÄNDERUNG \_ DER EC-QUALITÄT \_**](ec-quality-change.md)                        | Das Diagramm verwerfen Stichproben für die Qualitätskontrolle.                                                                       |
| [**EC \_ RENDER \_ FINISHED (EC-RENDER ABGESCHLOSSEN)**](ec-render-finished.md)                      | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                                       | Ein Videorenderer erfordert einen erneuten Strich.                                                                                      |
| [**\_ \_ EC-BEISPIELLATENZ**](ec-sample-latency.md)                        | Gibt an, wie weit eine Komponente für die Verarbeitung von Beispielen hinter dem Zeitplan zurückliegt.                                                  |
| [**\_EC-BEISPIEL \_ ERFORDERLICH**](ec-sample-needed.md)                          | Fordert ein neues Eingabebeispiel vom Filter Enhanced Video Renderer (EVR) an.                                                |
| [**\_EC-BEREINIGUNGSZEIT \_**](ec-scrub-time.md)                                | Gibt den Zeitstempel für den letzten Frameschritt an.                                                                  |
| [**\_EC-SEGMENT \_ GESTARTET**](ec-segment-started.md)                      | Ein neues Segment wurde gestartet.                                                                                                |
| [**EC \_ SHUTING DOWN (EC WIRD \_ HERUNTERGEFAHREN)**](ec-shutting-down.md)                          | Das Filterdiagramm wird heruntergefahren, bevor es zerstört wird.                                                              |
| [**EC \_ SNDDEV \_ IN \_ ERROR**](ec-snddev-in-error.md)                     | In einem Audioerfassungsfilter ist ein Gerätefehler aufgetreten.                                                                   |
| [**EC \_ SNDDEV \_ OUT \_ ERROR**](ec-snddev-out-error.md)                   | In einem Audiorendererfilter ist ein Gerätefehler aufgetreten.                                                                  |
| [**EC \_ STARVATION**](ec-starvation.md)                                 | Ein Filter empfängt nicht genügend Daten.                                                                                    |
| [**EC \_ STATE \_ CHANGE**](ec-state-change.md)                            | Der Zustand des Filterdiagramms wurde geändert.                                                                                       |
| [**\_EC-STATUS**](ec-status.md)                                         | Enthält zwei beliebige Statuszeichenfolgen.                                                                                    |
| [**\_EC-SCHRITT \_ ABGESCHLOSSEN**](ec-step-complete.md)                          | Ein Filter, der Frameschritte vor sich geht, hat die angegebene Anzahl von Frames abgestuft.                                            |
| [**EC \_ STREAM CONTROL STARTED \_ (EC STREAM-STEUERELEMENT \_ GESTARTET)**](ec-stream-control-started.md)       | Ein Startbefehl für das Streamsteuersteuersystem ist wirksam.                                                                          |
| [**EC \_ STREAM \_ CONTROL \_ STOPPED**](ec-stream-control-stopped.md)       | Ein Befehl zum Beenden der Streamsteuerung ist wirksam.                                                                           |
| [**EC \_ STREAM \_ ERROR \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | In einem Stream ist ein Fehler aufgetreten. Der Stream wird weiterhin abspielt.                                                           |
| [**EC \_ STREAM \_ ERROR \_ STOPPED**](ec-stream-error-stopped.md)           | Ein Stream wurde aufgrund eines Fehlers beendet.                                                                                 |
| [**EC \_ TIMECODE \_ VERFÜGBAR**](ec-timecode-available.md)                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | Senden über das Videosteuersystem, wenn ein Diagramm heruntergefahren wurde. Nicht an Anwendungen weitergeleitet.                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | Der Benutzer hat die Wiedergabe beendet.                                                                                         |
| [**EC \_ VIDEO SIZE CHANGED (EC-VIDEOGRÖßE \_ \_ GEÄNDERT)**](ec-video-size-changed.md)               | Die Größe des nativen Videos wurde geändert.                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | Ein Videoframe kann angezeigt werden.                                                                                       |
| [**FEHLER BEI \_ DER WIEDERHERSTELLUNG DER EC-VMR-VERBINDUNG \_ \_**](ec-vmr-reconnection-failed.md)     | Wird von VMR-7 und VMR-9 gesendet, wenn eine dynamische Formatänderungsanforderung vom Upstreamdecoder nicht akzeptiert werden konnte.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ SET**](ec-vmr-renderdevice-set.md)           | Wird gesendet, wenn der VMR seinen Renderingmechanismus ausgewählt hat.                                                                   |
| [**\_EC-VMR-OBERFLÄCHE \_ \_ GEKIPPT**](ec-vmr-surface-flipped.md)             | Wird gesendet, wenn der Zuweisungsbeteiliger von VMR-7 die DirectDraw Flip-Methode auf der dargestellten Oberfläche aufgerufen hat.           |
| [**EC \_ WINDOW \_ DESTROYED**](ec-window-destroyed.md)                    | Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.                                                               |
| [**EC \_ WMT \_ EVENT**](ec-wmt-event.md)                                  | Wird vom WM ASF-Readerfilter gesendet, wenn er ASF-Dateien liest, die durch Digital Rights Management (DRM) geschützt sind.                    |
| [**EC \_ WMT \_ INDEX \_ EVENT**](ec-wmt-index-event.md)                     | Wird gesendet, wenn eine Anwendung den WM ASF Writer zum Indizieren Windows Media Video-Dateien verwendet.                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



