---
description: Ereignis Benachrichtigungs Codes
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Ereignis Benachrichtigungs Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c41abc3ffc7a93a39e7a97fb210b491ad4fc58
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346424"
---
# <a name="event-notification-codes"></a>Ereignis Benachrichtigungs Codes

In diesem Abschnitt sind die DirectShow-Ereignisse aufgeführt, die nicht spezifisch für DVD sind. Informationen zu Ereignissen für DVD finden Sie unter [DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md).

Filter senden Ereignisse an den Filter Graph-Manager, indem Sie die [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) -Methode aufrufen. Der Filter Graph-Manager verarbeitet einige Ereignisse und fügt andere für die Anwendung in die Warteschlange ein. Die Anwendung ruft Sie durch Aufrufen der [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode ab.

In den folgenden Abschnitten werden in jedem Eintrag der Ereignis Code, die Bedeutung der Ereignis Parameter und die Standardaktion des Filter Diagramm-Managers für das Ereignis, sofern vorhanden, aufgelistet. Um die Standardaktion zu überschreiben, rufen Sie [**imediaevent:: canceldefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling)auf. Ereignis Codes werden in den Header Dateien evcode. h und audevcod. h definiert. Wenn keine Standardaktion vorhanden ist, leitet der Filter Graph-Manager das Ereignis automatisch an die Anwendung weiter (durch die Ereignis Warteschlange).

**Benutzerdefinierte Ereignisse**

Filter können benutzerdefinierte Ereignisse mit Ereignis Codes im Bereich EC \_ -Benutzer und höher definieren. Der Filter Graph-Manager platziert diese direkt in der Ereignis Warteschlange. Es gelten jedoch die folgenden Einschränkungen:

-   Der Filter Graph-Manager kann die Ereignis Parameter nicht mit der normalen [**imediaevent:: freeeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) -Methode freigeben. Die Anwendung muss alle Arbeitsspeicher-oder Verweis Zähler freigeben, die den Ereignis Parametern zugeordnet sind.
-   Der Filter sollte das Ereignis nur aus einer Anwendung senden, die für die Behandlung des Ereignisses vorbereitet ist. (Möglicherweise kann die Anwendung eine benutzerdefinierte Eigenschaft für den Filter festlegen, um anzugeben, dass das Ereignis sicher gesendet werden kann.)



| Ereignis Benachrichtigungs Code                                                 | BESCHREIBUNG                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Aktivieren von EC \_**](ec-activate.md)                                     | Ein Videofenster wird aktiviert oder deaktiviert.                                                                         |
| [**EC \_ bandwidthchange**](ec-bandwidthchange.md)                       | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Puffer \_ Daten**](ec-buffering-data.md)                        | Im Diagramm werden Daten gepuffert, oder die Pufferung der Daten wurde beendet.                                                               |
| [**EC \_ erstellt**](ec-built.md)                                           | Wird vom Video-Steuerelement gesendet, wenn ein Diagramm erstellt wurde. Nicht an Anwendungen weitergeleitet.                                     |
| [**EC- \_ Uhr \_ geändert**](ec-clock-changed.md)                          | Die verweisuhr hat sich geändert.                                                                                          |
| [**\_ \_ nicht festgelegte EC-Uhr**](ec-clock-unset.md)                              | Der Takt Anbieter wurde getrennt.                                                                                      |
| [**EC \_ codecapi- \_ Ereignis**](ec-codecapi-event.md)                        | Wird von einem Encoder gesendet, um ein Codierungs Ereignis zu signalisieren.                                                                           |
| [**EC \_ Complete**](ec-complete.md)                                     | Alle Daten aus einem bestimmten Stream wurden gerendert.                                                                      |
| [**Änderung von "EC \_ ContentProperty" \_**](ec-contentproperty-changed.md)      | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Gerät \_ verloren**](ec-device-lost.md)                              | Ein Plug & Play Gerät wurde entfernt oder wieder verfügbar.                                                         |
| [**EC- \_ Anzeige \_ geändert**](ec-display-changed.md)                      | Der Anzeigemodus wurde geändert.                                                                                             |
| [**EC- \_ Ende \_ des \_ Segments**](ec-end-of-segment.md)                       | Das Ende eines Segments wurde erreicht.                                                                                    |
| [**EC \_ EOS in \_ Kürze**](ec-eos-soon.md)                                    | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Fehler \_ beim Stillen**](ec-error-stillplaying.md)                | Ein asynchroner Befehl zum Ausführen des Diagramms ist fehlgeschlagen.                                                                      |
| [**EC \_ errorabort**](ec-errorabort.md)                                 | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**EC \_ errorabortex**](ec-errorabortex.md)                             | Ein Vorgang wurde aufgrund eines Fehlers abgebrochen.                                                                             |
| [**Änderung des EC- \_ extdevice- \_ Modus \_**](ec-extdevice-mode-change.md)         | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Datei \_ geschlossen**](ec-file-closed.md)                              | Die Quelldatei wurde aufgrund eines unerwarteten Ereignisses geschlossen.                                                                |
| [**EC- \_ Vollbildschirm \_ Verlust**](ec-fullscreen-lost.md)                      | Der Videorenderer schaltet den Vollbildmodus aus.                                                                  |
| [**EC- \_ Diagramm \_ geändert**](ec-graph-changed.md)                          | Das Filter Diagramm wurde geändert.                                                                                             |
| [**EC- \_ Länge \_ geändert**](ec-length-changed.md)                        | Die Länge einer Quelle hat sich geändert.                                                                                       |
| [**EC- \_ loadstatus**](ec-loadstatus.md)                                 | Benachrichtigt die Anwendung über den Fortschritt beim Öffnen einer Netzwerkdatei.                                                         |
| [**EC- \_ Marker \_ Treffer**](ec-marker-hit.md)                                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ muss \_ neu gestartet werden**](ec-need-restart.md)                            | Ein Filter fordert an, dass das Diagramm neu gestartet wird.                                                                       |
| [**neue EC- \_ \_ PIN**](ec-new-pin.md)                                      | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Benachrichtigungs \_ Fenster**](ec-notify-window.md)                          | Benachrichtigt einen Filter über das Fenster des Video-Renderers.                                                                         |
| [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md)                                  | Ein Filter übergibt eine Text Zeichenfolge an die Anwendung.                                                                     |
| [**EC- \_ öffnende \_ Datei**](ec-opening-file.md)                            | Das Diagramm öffnet eine Datei, oder das Öffnen einer Datei ist abgeschlossen.                                                              |
| [**EC- \_ Palette \_ geändert**](ec-palette-changed.md)                      | Die Video Palette hat sich geändert.                                                                                            |
| [**EC \_ angehalten**](ec-paused.md)                                         | Eine Pause-Anforderung wurde abgeschlossen.                                                                                            |
| [**EC \_ Bitte \_ erneut öffnen**](ec-please-reopen.md)                          | Die Quelldatei wurde geändert.                                                                                              |
| [**EC- \_ Vorverarbeitung ist \_ beendet**](ec-preprocess-complete.md)              | Wird vom [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter gesendet, wenn die Vorverarbeitung für Multipass-Codierung abgeschlossen ist. |
| [**EC- \_ Verarbeitungs \_ Latenz**](ec-processing-latency.md)                | Gibt die Zeitspanne an, die eine Komponente zum Verarbeiten der einzelnen Stichproben einnimmt.                                           |
| [**EC- \_ Qualitäts \_ Änderung**](ec-quality-change.md)                        | Das Diagramm dient zum Verwerfen von Beispielen, um die Qualität zu steuern.                                                                       |
| [**EC- \_ Rendering \_ abgeschlossen**](ec-render-finished.md)                      | Wird nicht unterstützt.                                                                                                            |
| [**EC- \_ Repaint**](ec-repaint.md)                                       | Ein Videorenderer erfordert ein Repaint.                                                                                      |
| [**Wartezeit für EC- \_ Beispiel \_**](ec-sample-latency.md)                        | Gibt an, wie weit hinter dem Zeitplan eine Komponente für die Verarbeitung von Beispielen liegt.                                                  |
| [**EC- \_ Beispiel \_ erforderlich**](ec-sample-needed.md)                          | Fordert ein neues Eingabe Beispiel vom EVR-Filter (Enhanced Video Renderer) an.                                                |
| [**\_Zeit für \_ Zeit Bereinigung**](ec-scrub-time.md)                                | Gibt den Zeitstempel für den letzten Frame Schritt an.                                                                  |
| [**EC- \_ Segment \_ gestartet**](ec-segment-started.md)                      | Ein neues Segment wurde gestartet.                                                                                                |
| [**EC \_ wird \_ heruntergefahren**](ec-shutting-down.md)                          | Das Filter Diagramm wird vor dem zerstören heruntergefahren.                                                              |
| [**\_Fehler bei EC snddev. \_ \_**](ec-snddev-in-error.md)                     | Ein Gerätefehler ist in einem audioerfassungs Filter aufgetreten.                                                                   |
| [**EC \_ snddev \_ out- \_ Fehler**](ec-snddev-out-error.md)                   | Ein Gerätefehler ist in einem audiorendererfilter aufgetreten.                                                                  |
| [**EC- \_ Hunger**](ec-starvation.md)                                 | Ein Filter empfängt nicht genügend Daten.                                                                                    |
| [**Änderung des EC- \_ Zustands \_**](ec-state-change.md)                            | Der Zustand des Filter Diagramms wurde geändert.                                                                                       |
| [**EC- \_ Status**](ec-status.md)                                         | Enthält zwei beliebige Status Zeichenfolgen.                                                                                    |
| [**EC- \_ Schritt ist \_ beendet**](ec-step-complete.md)                          | Ein Filter, der die Frame Ausführung durchführt, hat die angegebene Anzahl von Frames abgestuft.                                            |
| [**EC- \_ Stream- \_ Steuerelement \_**](ec-stream-control-started.md)       | Der Startbefehl für die Stream-Steuerung wurde wirksam.                                                                          |
| [**EC- \_ Stream- \_ Steuerelement \_ beendet**](ec-stream-control-stopped.md)       | Ein Befehl zum Abbrechen der Stream-Steuerung wurde wirksam.                                                                           |
| [**\_ \_ Fehler \_ beim Wiedergeben des EC-Stream**](ec-stream-error-stillplaying.md) | In einem Stream ist ein Fehler aufgetreten. Der Stream wird immer noch abgespielt.                                                           |
| [**Fehler beim EC- \_ Stream. \_ \_**](ec-stream-error-stopped.md)           | Ein Datenstrom wurde aufgrund eines Fehlers beendet.                                                                                 |
| [**EC- \_ Zeit Leitzahl \_ verfügbar**](ec-timecode-available.md)                | Wird nicht unterstützt.                                                                                                            |
| [**EC \_ wurde nicht erstellt.**](ec-unbuilt.md)                                       | Wird vom Video-Steuerelement gesendet, wenn ein Diagramm abgebrochen wurde. Nicht an Anwendungen weitergeleitet.                                 |
| [**EC \_ userabort**](ec-userabort.md)                                   | Der Benutzer hat die Wiedergabe beendet.                                                                                         |
| [**Größe des EC- \_ Videos \_ \_ geändert**](ec-video-size-changed.md)               | Die Größe des nativen Videos wurde geändert.                                                                                        |
| [**EC \_ videoframeready**](ec-videoframeready.md)                       | Ein Videoframe ist bereit für die Anzeige.                                                                                       |
| [**Fehler beim \_ \_ erneuten Herstellen der Verbindung mit EC VMR \_**](ec-vmr-reconnection-failed.md)     | Wird von VMR-7 und VMR-9 gesendet, wenn es nicht möglich war, ein dynamisches Format Change Request aus dem upstreamdecoder zu akzeptieren.   |
| [**auf EC \_ VMR \_ renderdevice \_ festgelegt**](ec-vmr-renderdevice-set.md)           | Wird gesendet, wenn der VMR seinen renderingmechanismus ausgewählt hat.                                                                   |
| [**EC- \_ VMR- \_ Oberfläche \_ gekippt**](ec-vmr-surface-flipped.md)             | Wird gesendet, wenn der zuordnerpräsentator von VMR-7Die DirectDraw-Flip-Methode auf der dargestellten Oberfläche aufgerufen hat.           |
| [**EC- \_ Fenster \_ zerstört**](ec-window-destroyed.md)                    | Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.                                                               |
| [**\_WMT- \_ Ereignis für EC**](ec-wmt-event.md)                                  | Wird vom WM-ASF-Reader-Filter gesendet, wenn die von Digital Rights Management (DRM) geschützten ASF-Dateien gelesen werden.                    |
| [**EC \_ WMT- \_ Index \_ Ereignis**](ec-wmt-index-event.md)                     | Wird gesendet, wenn eine Anwendung den WM-ASF-Writer zum Indizieren Windows Media Video Dateien verwendet.                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



