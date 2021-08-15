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

In diesen Abschnitten werden die DirectShow-Ereignisse aufgeführt, die nicht dvdspezifisch sind. Informationen zu DVD-spezifischen Ereignissen finden Sie unter [DVD-Ereignisbenachrichtigungscodes.](dvd-notification-codes.md)

Filter senden Ereignisse an den Filter Graph Manager, indem sie die [**IMediaEventSink::Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) aufrufen. Der Filter Graph Manager verarbeitet einige Ereignisse und reiht andere für die Anwendung in die Warteschlange ein. Die Anwendung ruft sie ab, indem sie die [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) aufruft.

In den folgenden Abschnitten listet jeder Eintrag den Ereigniscode, die Bedeutung der Ereignisparameter und die Standardaktion des Filter Graph-Managers für das Ereignis auf( falls dies der Fall ist). Rufen Sie zum Überschreiben der Standardaktion [**IMediaEvent::CancelDefaultHandling auf.**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) Ereigniscodes werden in den Headerdateien Evcode.h und Audevcod.h definiert. Wenn keine Standardaktion ausgeführt wird, wird das Ereignis Graph Manager automatisch an die Anwendung (über die Ereigniswarteschlange) weitergeleitet.

**Benutzerdefinierte Ereignisse**

Filter können benutzerdefinierte Ereignisse mit Ereigniscodes im Bereich EC \_ USER und höher definieren. Der Filter Graph Manager platzieren diese direkt in der Ereigniswarteschlange. Es gelten jedoch die folgenden Einschränkungen:

-   Der Filter Graph Manager kann die Ereignisparameter nicht mithilfe der normalen [**IMediaEvent::FreeEventParams-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) frei geben. Die Anwendung muss alle Speicher- oder Verweiszähler, die den Ereignisparametern zugeordnet sind, frei geben.
-   Der Filter sollte das Ereignis nur aus einer Anwendung heraus senden, die für die Handhabung des Ereignisses vorbereitet ist. (Möglicherweise kann die Anwendung eine benutzerdefinierte Eigenschaft für den Filter festlegen, um anzugeben, dass es sicher ist, das Ereignis zu senden.)



| Ereignisbenachrichtigungscode                                                 | BESCHREIBUNG                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                                     | Ein Videofenster wird aktiviert oder deaktiviert.                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ BUFFERING \_ DATA**](ec-buffering-data.md)                        | Das Diagramm puffert Daten oder hat die Pufferung von Daten beendet.                                                               |
| [**EC \_ BUILT**](ec-built.md)                                           | Senden über das Videosteuersystem, wenn ein Diagramm erstellt wurde. Nicht an Anwendungen weitergeleitet.                                     |
| [**EC \_ CLOCK \_ CHANGED**](ec-clock-changed.md)                          | Die Referenzuhr wurde geändert.                                                                                          |
| [**EC \_ CLOCK \_ UNSET**](ec-clock-unset.md)                              | Die Verbindung mit dem Uhranbieter wurde getrennt.                                                                                      |
| [**EC \_ \_ CODECAPI-EREIGNIS**](ec-codecapi-event.md)                        | Wird von einem Encoder gesendet, um ein Codierungsereignis zu signalisieren.                                                                           |
| [**EC \_ COMPLETE**](ec-complete.md)                                     | Alle Daten aus einem bestimmten Stream wurden gerendert.                                                                      |
| [**EC \_ CONTENTPROPERTY \_ GEÄNDERT**](ec-contentproperty-changed.md)      | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ DEVICE LOST (EC-GERÄT \_ VERLOREN)**](ec-device-lost.md)                              | Ein Plug & Play gerät wurde entfernt oder ist wieder verfügbar.                                                         |
| [**\_EC-ANZEIGE \_ GEÄNDERT**](ec-display-changed.md)                      | Der Anzeigemodus wurde geändert.                                                                                             |
| [**EC \_ END \_ OF \_ SEGMENT**](ec-end-of-segment.md)                       | Das Ende eines Segments wurde erreicht.                                                                                    |
| [**EC \_ EOS \_ SOON**](ec-eos-soon.md)                                    | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ ERROR \_ STILLPLAYING**](ec-error-stillplaying.md)                | Fehler bei einem asynchronen Befehl zum Ausführen des Graphen.                                                                      |
| [**EC \_ ERRORABORT**](ec-errorabort.md)                                 | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**EC \_ ERRORABORTEX**](ec-errorabortex.md)                             | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**EC \_ EXTDEVICE \_ MODE \_ CHANGE**](ec-extdevice-mode-change.md)         | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ FILE \_ CLOSED**](ec-file-closed.md)                              | Die Quelldatei wurde aufgrund eines unerwarteten Ereignisses geschlossen.                                                                |
| [**EC \_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md)                      | Der Videorenderer wechselt aus dem Vollbildmodus.                                                                  |
| [**EC \_ GRAPH \_ CHANGED**](ec-graph-changed.md)                          | Das Filterdiagramm wurde geändert.                                                                                             |
| [**EC \_ LENGTH \_ CHANGED**](ec-length-changed.md)                        | Die Länge einer Quelle hat sich geändert.                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.                                                         |
| [**EC \_ MARKER \_ HIT**](ec-marker-hit.md)                                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ NEED \_ RESTART**](ec-need-restart.md)                            | Ein Filter fordert, dass der Graph neu gestartet wird.                                                                       |
| [**EC \_ NEW \_ PIN**](ec-new-pin.md)                                      | Wird nicht unterstützt.                                                                                                            |
| [**FENSTER "EC \_ NOTIFY" (EC \_ NOTIFY)**](ec-notify-window.md)                          | Benachrichtigt einen Filter über das Fenster des Videorenderers.                                                                         |
| [**EC \_ OLE \_ EVENT**](ec-ole-event.md)                                  | Ein Filter übergibt eine Textzeichenfolge an die Anwendung.                                                                     |
| [**EC \_ OPENING \_ FILE**](ec-opening-file.md)                            | Das Diagramm öffnet eine Datei oder hat das Öffnen einer Datei beendet.                                                              |
| [**EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md)                      | Die Videopalette wurde geändert.                                                                                            |
| [**EC \_ PAUSED**](ec-paused.md)                                         | Eine Anforderung zum Anhalten wurde abgeschlossen.                                                                                            |
| [**EC \_ PLEASE \_ REOPEN**](ec-please-reopen.md)                          | Die Quelldatei wurde geändert.                                                                                              |
| [**EC \_ PREPROCESS \_ COMPLETE**](ec-preprocess-complete.md)              | Wird vom [WM ASF Writer-Filter](wm-asf-writer-filter.md) gesendet, wenn die Vorverarbeitung für multipass-Codierung abgeschlossen ist. |
| [**\_ \_ EC-VERARBEITUNGSLATENZ**](ec-processing-latency.md)                | Gibt die Zeit an, die eine Komponente zum Verarbeiten der einzelnen Stichproben in Bearbeitung nimmt.                                           |
| [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md)                        | Das Diagramm verdringt Beispiele für die Qualitätskontrolle.                                                                       |
| [**EC \_ RENDER \_ FINISHED**](ec-render-finished.md)                      | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                                       | Ein Videorenderer erfordert einen Neupaint.                                                                                      |
| [**EC \_ SAMPLE \_ LATENCY**](ec-sample-latency.md)                        | Gibt an, wie weit der Zeitplan einer Komponente für die Verarbeitung von Beispielen zurück liegt.                                                  |
| [**EC \_ SAMPLE \_ NEEDED**](ec-sample-needed.md)                          | Fordert ein neues Eingabebeispiel vom EvR-Filter (Enhanced Video Renderer) an.                                                |
| [**\_ \_ EC-REINIGUNGSZEIT**](ec-scrub-time.md)                                | Gibt den Zeitstempel für den letzten Frameschritt an.                                                                  |
| [**\_EC-SEGMENT \_ GESTARTET**](ec-segment-started.md)                      | Ein neues Segment wurde gestartet.                                                                                                |
| [**EC \_ WIRD \_ HERUNTERGEFAHREN**](ec-shutting-down.md)                          | Das Filterdiagramm wird heruntergefahren, bevor es zerstört wird.                                                              |
| [**EC \_ SNDDEV \_ IN \_ ERROR**](ec-snddev-in-error.md)                     | In einem Audioaufnahmefilter ist ein Gerätefehler aufgetreten.                                                                   |
| [**\_EC-SNDDEV \_ \_ OUT-FEHLER**](ec-snddev-out-error.md)                   | In einem Audiorendererfilter ist ein Gerätefehler aufgetreten.                                                                  |
| [**EC \_ STARVATION**](ec-starvation.md)                                 | Ein Filter empfängt nicht genügend Daten.                                                                                    |
| [**EC \_ STATE \_ CHANGE**](ec-state-change.md)                            | Der Status des Filterdiagramms wurde geändert.                                                                                       |
| [**\_EC-STATUS**](ec-status.md)                                         | Enthält zwei beliebige Statuszeichenfolgen.                                                                                    |
| [**\_EC-SCHRITT \_ ABGESCHLOSSEN**](ec-step-complete.md)                          | Ein Filter, der die Frameschritte ausführt, hat die angegebene Anzahl von Frames abgestuft.                                            |
| [**EC \_ STREAM \_ CONTROL \_ STARTED**](ec-stream-control-started.md)       | Ein Stream-Control-Startbefehl wurde wirksam.                                                                          |
| [**EC \_ STREAM \_ CONTROL \_ STOPPED**](ec-stream-control-stopped.md)       | Ein Stream Control Stop-Befehl wurde wirksam.                                                                           |
| [**EC \_ STREAM \_ ERROR \_ STILLPLAYING**](ec-stream-error-stillplaying.md) | In einem Stream ist ein Fehler aufgetreten. Der Stream wird weiterhin wiedergegeben.                                                           |
| [**EC \_ STREAM \_ ERROR \_ STOPPED**](ec-stream-error-stopped.md)           | Ein Stream wurde aufgrund eines Fehlers beendet.                                                                                 |
| [**EC \_ TIMECODE \_ VERFÜGBAR**](ec-timecode-available.md)                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | Wird vom Videosteuerelement gesendet, wenn ein Diagramm abraufgelegt wurde. Nicht an Anwendungen weitergeleitet.                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | Der Benutzer hat die Wiedergabe beendet.                                                                                         |
| [**\_EC-VIDEOGRÖßE \_ \_ GEÄNDERT**](ec-video-size-changed.md)               | Die Größe des nativen Videos wurde geändert.                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | Ein Videoframe kann angezeigt werden.                                                                                       |
| [**\_FEHLER BEI DER WIEDERHERSTELLUNG DER EC-VMR-VERBINDUNG \_ \_**](ec-vmr-reconnection-failed.md)     | Wird von VMR-7 und VMR-9 gesendet, wenn eine Änderungsanforderung des dynamischen Formats vom Upstreamdecoder nicht akzeptiert werden konnte.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ SET**](ec-vmr-renderdevice-set.md)           | Wird gesendet, wenn die VMR ihren Renderingmechanismus ausgewählt hat.                                                                   |
| [**EC \_ VMR \_ SURFACE \_ FLIPPED**](ec-vmr-surface-flipped.md)             | Wird gesendet, wenn die Zuweisungs presenter von VMR-7 die DirectDraw Flip-Methode auf der dargestellten Oberfläche aufgerufen hat.           |
| [**\_EC-FENSTER \_ ZERSTÖRT**](ec-window-destroyed.md)                    | Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.                                                               |
| [**EC \_ WMT \_ EVENT**](ec-wmt-event.md)                                  | Wird vom WM-ASF-Readerfilter gesendet, wenn er DURCH DRM (Digital Rights Management) geschützte ASF-Dateien liest.                    |
| [**EC \_ WMT \_ INDEX \_ EVENT**](ec-wmt-index-event.md)                     | Wird gesendet, wenn eine Anwendung den WM ASF Writer verwendet, um Windows Media Video-Dateien zu indizierung.                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



