---
description: DVD-Ereignis Benachrichtigungs Codes
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: DVD-Ereignis Benachrichtigungs Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15172e8eba3da048e7c7704a90d7992fa21714a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346400"
---
# <a name="dvd-event-notification-codes"></a>DVD-Ereignis Benachrichtigungs Codes

In diesem Abschnitt werden die Ereignis Benachrichtigungs Codes für die DVD-Wiedergabe und-Navigation in DirectShow aufgelistet.

Informationen zum Empfangen von Ereignissen in DirectShow finden Sie unter [Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md).

Informationen zu anderen nicht-DVD-Ereignis Codes finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).



| Ereignis Benachrichtigungs Code                                                        | BESCHREIBUNG                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Änderung des EC- \_ DVD- \_ Winkels \_**](ec-dvd-angle-change.md)                          | Signalisiert, dass entweder die Anzahl der verfügbaren Winkel geändert wurde oder die aktuelle Winkel Zahl geändert wurde.                                                                      |
| [**EC- \_ DVD- \_ Winkel \_ verfügbar**](ec-dvd-angles-available.md)                  | Gibt an, ob ein Winkel Block wiedergegeben und Winkel Änderungen durchgeführt werden können.                                                                                      |
| [**Änderung des EC \_ \_ -DVD- \_ Audiostreams \_**](ec-dvd-audio-stream-change.md)           | Signalisiert, dass die aktuelle audiostreamnummer für den Haupttitel geändert wurde.                                                                                                  |
| [**EC- \_ DVD \_ beginnavigationcommands**](ec-dvd-beginnavigationcommands.md)     | Wird gesendet, wenn ein Satz von DVD-Navigations Befehlen gestartet wird.                                                                                                                  |
| [**EC- \_ DVD- \_ Schaltfläche \_ automatisch \_ aktiviert**](ec-dvd-button-auto-activated.md)       | Signalisiert, dass eine Menü Schaltfläche automatisch gemäß den Anweisungen auf der Festplatte aktiviert wurde.                                                                                 |
| [**EC- \_ DVD- \_ Schaltflächen \_ Änderung**](ec-dvd-button-change.md)                        | Signalisiert, dass entweder die Anzahl der verfügbaren Schaltflächen geändert wurde oder die aktuell ausgewählte Schaltflächen Nummer geändert wurde.                                                         |
| [**EC- \_ DVD- \_ Kapitel \_ autostopps**](ec-dvd-chapter-autostop.md)                  | Gibt an, dass die Wiedergabe aufgrund eines Aufrufes der [**IDvdControl2::P laychaptersaudestopp**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) -Methode beendet wurde.                    |
| [**EC- \_ DVD- \_ Kapitel \_ Start**](ec-dvd-chapter-start.md)                        | Signalisiert, dass der DVD-Navigator die Wiedergabe eines neuen Kapitels im aktuellen Titel gestartet hat.                                                                                    |
| [**Start der EC- \_ DVD- \_ cmd \_**](ec-dvd-cmd-start.md)                                | Signalisiert, dass ein bestimmter Befehl begonnen hat.                                                                                                                              |
| [**EC- \_ DVD- \_ cmd- \_ Ende**](ec-dvd-cmd-end.md)                                    | Signalisiert, dass ein bestimmter Befehl abgeschlossen wurde.                                                                                                                          |
| [**EC- \_ DVD \_ aktuelle \_ hmsf- \_ Zeit**](ec-dvd-current-hmsf-time.md)               | Signalisiert die aktuelle Uhrzeit im [**DVD- \_ hmsf- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) Format am Anfang jeder Video Object Unit (vobu).                                   |
| [**\_ \_ aktuelle \_ Uhrzeit der EC-DVD**](ec-dvd-current-time.md)                          | Signalisiert den Anfang jeder vobu.                                                                                                                                      |
| [**EC- \_ DVD- \_ CD- \_ aussteht**](ec-dvd-disc-ejected.md)                          | Signalisiert, dass ein Laufwerk vom Laufwerk entfernt wurde.                                                                                                                      |
| [**EC- \_ DVD- \_ CD \_ eingefügt**](ec-dvd-disc-inserted.md)                        | Signalisiert, dass eine CD in das Laufwerk eingefügt wurde.                                                                                                                     |
| [**Änderung der EC- \_ DVD- \_ Domäne \_**](ec-dvd-domain-change.md)                        | Gibt die neue Domäne des DVD-Navigators an.                                                                                                                                 |
| [**EC- \_ DVD- \_ Fehler**](ec-dvd-error.md)                                         | Signalisiert eine DVD-Fehlerbedingung.                                                                                                                                            |
| [**Änderungen an der EC- \_ DVD- \_ GPRM \_**](ec-dvd-gprm-change.md)                            | Wird gesendet, wenn sich der Wert eines allgemeinen Parameter Registers (GPRM) ändert.                                                                                                       |
| [**EC- \_ DVD- \_ Karaoke- \_ Modus**](ec-dvd-karaoke-mode.md)                          | Gibt an, dass der Navigator entweder mit der Wiedergabe begonnen hat oder mit der Wiedergabe von Karaoke                                                                                   |
| [**EC \_ DVD \_ navigationcommand**](ec-dvd-navigationcommand.md)                 | Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) einen DVD-Navigations Befehl verarbeitet.                                                                               |
| [**EC- \_ DVD \_ keine FP- \_ \_ PGC**](ec-dvd-no-fp-pgc.md)                               | Gibt an, dass die DVD-Diskette keine FP \_ PGC (First Play Program Chain) enthält.                                                                                           |
| [**Änderung der EC-DVD-Jugend \_ \_ \_ Ebene \_**](ec-dvd-parental-level-change.md)       | Signalisiert, dass die Jugend Stufe des verfassten Inhalts geändert wird.                                                                                               |
| [**Änderung der EC- \_ DVD- \_ Wiedergabe \_ Rate \_**](ec-dvd-playback-rate-change.md)         | Gibt an, dass eine Wiedergabe Raten Änderung initiiert wurde und die neue Rate im-Parameter liegt.                                                                            |
| [**EC- \_ DVD- \_ Wiedergabe \_ beendet**](ec-dvd-playback-stopped.md)                  | Gibt an, dass die Wiedergabe beendet wurde. Der DVD-Navigator hat die Wiedergabe des Titels abgeschlossen und hat keine andere Verzweigungs Anweisung für die nachfolgende Wiedergabe gefunden. |
| [**EC- \_ DVD- \_ playperiod \_ autostopps**](ec-dvd-playperiod-autostop.md)            | Gibt an, dass der Navigator die Wiedergabe des Segments abgeschlossen hat, das in einem-Befehl von playperiodintitleautoend angegeben wurde.                                                           |
| [**Änderung des EC- \_ DVD- \_ Programms \_ \_**](ec-dvd-program-cell-change.md)           | Wird gesendet, wenn sich die Nummer oder Zellnummer des DVD-Programms ändert.                                                                                                                  |
| [**Änderung der EC- \_ DVD- \_ Programm \_ Kette \_**](ec-dvd-program-chain-change.md)         | Wird gesendet, wenn sich die aktuelle Programm Kette (PGC) ändert.                                                                                                                            |
| [**EC- \_ DVD- \_ SPRM- \_ Änderung**](ec-dvd-sprm-change.md)                            | Wird gesendet, wenn sich der Wert eines Systemparameter Registers (SPRM) ändert.                                                                                                        |
| [**EC- \_ DVD ist \_ noch deaktiviert. \_**](ec-dvd-still-off.md)                                | Signalisiert das Ende eines noch immer.                                                                                                                                             |
| [**EC- \_ DVD \_ weiterhin \_ on**](ec-dvd-still-on.md)                                  | Signalisiert den Anfang eines beliebigen noch.                                                                                                                                       |
| [**Datenstrom Änderung des EC-DVD- \_ \_ subbildes \_ \_**](ec-dvd-subpicture-stream-change.md) | Signalisiert, dass die aktuelle Teilbild-streamnummer für den Haupttitel geändert wurde.                                                                                             |
| [**\_Änderung der \_ Titel \_ Gruppe \_ für EC-DVD**](ec-dvd-title-set-change.md)                 | Wird gesendet, wenn sich der aktuelle Video Titel Satz (VTS) ändert.                                                                                                                          |
| [**Änderung des EC- \_ DVD- \_ Titels \_**](ec-dvd-title-change.md)                          | Gibt an, wann sich die aktuelle Titel Nummer ändert.                                                                                                                          |
| [**\_ \_ gültige \_ UOPs- \_ Änderung für EC-DVD**](ec-dvd-valid-uops-change.md)               | Signalisiert, dass sich der verfügbare Satz von [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstellen Methoden geändert hat.                                                                     |
| [**EC- \_ DVD- \_ vobu- \_ Offset**](ec-dvd-vobu-offset.md)                            | Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.                                                                                              |
| [**Zeitstempel für EC- \_ DVD- \_ vobu \_**](ec-dvd-vobu-timestamp.md)                      | Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.                                                                                              |
| [**EC- \_ DVD- \_ Warnung**](ec-dvd-warning.md)                                     | Signalisiert eine DVD-Warnungs Bedingung.                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> </dl>

 

 



