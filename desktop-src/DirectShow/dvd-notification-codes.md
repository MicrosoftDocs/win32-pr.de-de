---
description: DVD-Ereignisbenachrichtigungscodes
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: DVD-Ereignisbenachrichtigungscodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717c260c84a1038860ee04f46db6224025b7709c3ad039e7625a48ae6359cc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686450"
---
# <a name="dvd-event-notification-codes"></a>DVD-Ereignisbenachrichtigungscodes

In diesem Abschnitt werden die Ereignisbenachrichtigungscodes für die DVD-Wiedergabe und -Navigation in DirectShow aufgeführt.

Informationen zum Empfangen von Ereignissen in DirectShow finden Sie unter [Ereignisbenachrichtigung in DirectShow.](event-notification-in-directshow.md)

Informationen zu anderen Nicht-DVD-Ereigniscodes finden Sie unter [Ereignisbenachrichtigungscodes](event-notification-codes.md).



| Ereignisbenachrichtigungscode                                                        | Beschreibung                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ DVD \_ ANGLE \_ CHANGE**](ec-dvd-angle-change.md)                          | Signalisiert, dass sich entweder die Anzahl der verfügbaren Winkel geändert hat oder dass sich die aktuelle Winkelnummer geändert hat.                                                                      |
| [**EC \_ DVD \_ ANGLES \_ AVAILABLE**](ec-dvd-angles-available.md)                  | Gibt an, ob ein Winkelblock abgespielt wird und Winkeländerungen durchgeführt werden können.                                                                                      |
| [**ÄNDERUNG DES \_ \_ EC-DVD-AUDIOSTREAMS \_ \_**](ec-dvd-audio-stream-change.md)           | Signalisiert, dass sich die aktuelle Audiostreamnummer für den Haupttitel geändert hat.                                                                                                  |
| [**EC \_ DVD \_ BeginNavigationCommands**](ec-dvd-beginnavigationcommands.md)     | Wird gesendet, wenn eine Reihe von DVD-Navigationsbefehlen gestartet wird.                                                                                                                  |
| [**EC \_ DVD BUTTON AUTO \_ \_ ACTIVATED (EC-DVD-SCHALTFLÄCHE \_ AUTOMATISCH AKTIVIERT)**](ec-dvd-button-auto-activated.md)       | Signalisiert, dass eine Menüschaltfläche automatisch aktiviert wurde, wie in den Anweisungen auf dem Datenträger angegeben.                                                                                 |
| [**EC \_ DVD \_ BUTTON \_ CHANGE**](ec-dvd-button-change.md)                        | Signalisiert, dass sich entweder die Anzahl der verfügbaren Schaltflächen geändert hat oder dass sich die aktuell ausgewählte Schaltflächennummer geändert hat.                                                         |
| [**EC \_ DVD \_ CHAPTER \_ AUTOTOP**](ec-dvd-chapter-autostop.md)                  | Gibt an, dass die Wiedergabe als Ergebnis eines Aufrufs der [**IDvdControl2::P layChaptersAutoStop-Methode beendet**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) wurde.                    |
| [**EC \_ DVD \_ CHAPTER \_ START**](ec-dvd-chapter-start.md)                        | Signalisiert, dass der DVD-Navigator die Wiedergabe eines neuen Kapitels im aktuellen Titel gestartet hat.                                                                                    |
| [**EC \_ DVD \_ CMD \_ START**](ec-dvd-cmd-start.md)                                | Signalisiert, dass ein bestimmter Befehl begonnen hat.                                                                                                                              |
| [**EC \_ DVD \_ CMD \_ END**](ec-dvd-cmd-end.md)                                    | Signalisiert, dass ein bestimmter Befehl abgeschlossen wurde.                                                                                                                          |
| [**EC \_ DVD \_ CURRENT \_ HMSF \_ TIME**](ec-dvd-current-hmsf-time.md)               | Signalisiert die aktuelle Zeit im [**DVD \_ HMSF \_ TIMECODE-Format**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) am Anfang jeder Videoobjekteinheit (VIDEO Object Unit, VOBU).                                   |
| [**AKTUELLE \_ UHRZEIT DER \_ EC-DVD \_**](ec-dvd-current-time.md)                          | Signalisiert den Anfang jedes VOBU.                                                                                                                                      |
| [**EC \_ DVD \_ DISC \_ EJECTED**](ec-dvd-disc-ejected.md)                          | Signalisiert, dass ein Datenträger vom Laufwerk ausjiziert wurde.                                                                                                                      |
| [**EC \_ DVD \_ DISC \_ INSERTED**](ec-dvd-disc-inserted.md)                        | Signalisiert, dass ein Datenträger in das Laufwerk eingefügt wurde.                                                                                                                     |
| [**EC \_ DVD \_ DOMAIN \_ CHANGE**](ec-dvd-domain-change.md)                        | Gibt die neue Domäne des DVD-Navigators an.                                                                                                                                 |
| [**\_ \_ EC-DVD-FEHLER**](ec-dvd-error.md)                                         | Signalisiert eine DVD-Fehlerbedingung.                                                                                                                                            |
| [**EC \_ DVD \_ GPRM \_ Change**](ec-dvd-gprm-change.md)                            | Wird gesendet, wenn sich der Wert eines allgemeinen Parameterregisters (GPRM) ändert.                                                                                                       |
| [**EC \_ DVD \_ \_ DVD-MODUS**](ec-dvd-karaoke-mode.md)                          | Gibt an, dass der Navigator entweder mit der Wiedergabe begonnen oder die Wiedergabe von Daten beendet hat.                                                                                   |
| [**EC \_ DVD \_ NavigationCommand**](ec-dvd-navigationcommand.md)                 | Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) einen DVD-Navigationsbefehl verarbeitet.                                                                               |
| [**EC \_ DVD \_ NO \_ FP \_ PGC**](ec-dvd-no-fp-pgc.md)                               | Gibt an, dass der DVD-Datenträger über keine \_ FP-PGC (First Play Program Chain) verfügt.                                                                                           |
| [**ÄNDERUNG DER \_ \_ JUGENDSTUFE \_ DER \_ EC-DVD**](ec-dvd-parental-level-change.md)       | Signalisiert, dass sich die Ebene der Eltern des inhaltser erstellenden Inhalts ändert.                                                                                               |
| [**ÄNDERUNG DER \_ \_ WIEDERGABERATE DER \_ \_ EC-DVD**](ec-dvd-playback-rate-change.md)         | Gibt an, dass eine Änderung der Wiedergaberate initiiert wurde und sich die neue Rate im -Parameter befindet.                                                                            |
| [**EC \_ DVD PLAYBACK STOPPED (EC-DVD-WIEDERGABE \_ \_ BEENDET)**](ec-dvd-playback-stopped.md)                  | Gibt an, dass die Wiedergabe beendet wurde. Der DVD-Navigator hat die Wiedergabe des Titels abgeschlossen und keine andere Verzweigungsanweisung für die nachfolgende Wiedergabe finden. |
| [**EC \_ DVD \_ PLAYPERIOD \_ AUTOTOP**](ec-dvd-playperiod-autostop.md)            | Gibt an, dass der Navigator die Wiedergabe des in einem Aufruf von PlayPeriodInTitleAutoStop angegebenen Segments beendet hat.                                                           |
| [**EC \_ DVD \_ PROGRAM \_ CELL \_ CHANGE**](ec-dvd-program-cell-change.md)           | Wird gesendet, wenn sich die DVD-Programmnummer oder Zellnummer ändert.                                                                                                                  |
| [**EC \_ DVD \_ PROGRAM \_ CHAIN \_ CHANGE**](ec-dvd-program-chain-change.md)         | Wird gesendet, wenn sich die aktuelle Programmkette (PGC) ändert.                                                                                                                            |
| [**EC \_ DVD \_ SPRM \_ Change**](ec-dvd-sprm-change.md)                            | Wird gesendet, wenn sich der Wert eines Systemparameterregisters (SPRM) ändert.                                                                                                        |
| [**EC \_ DVD \_ STILL \_ OFF**](ec-dvd-still-off.md)                                | Signalisiert das Ende einer noch.                                                                                                                                             |
| [**EC \_ DVD \_ STILL \_ ON**](ec-dvd-still-on.md)                                  | Signalisiert den Anfang einer beliebigen noch.                                                                                                                                       |
| [**EC \_ DVD \_ SUBPICTURE \_ STREAM \_ CHANGE**](ec-dvd-subpicture-stream-change.md) | Signalisiert, dass sich die aktuelle Unterbilddatenstromnummer für den Haupttitel geändert hat.                                                                                             |
| [**EC \_ DVD \_ TITLE \_ SET \_ CHANGE**](ec-dvd-title-set-change.md)                 | Wird gesendet, wenn sich der aktuelle Videotitelsatz (Video Title Set, VTS) ändert.                                                                                                                          |
| [**ÄNDERUNG DES \_ \_ EC-DVD-TITELS \_**](ec-dvd-title-change.md)                          | Gibt an, wann sich die aktuelle Titelnummer ändert.                                                                                                                          |
| [**EC \_ DVD \_ VALID \_ UOPS \_ CHANGE**](ec-dvd-valid-uops-change.md)               | Signalisiert, dass sich der verfügbare Satz von [**IDvdControl2-Schnittstellenmethoden**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) geändert hat.                                                                     |
| [**EC \_ DVD \_ VOBU \_ Offset**](ec-dvd-vobu-offset.md)                            | Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.                                                                                              |
| [**EC \_ DVD \_ VOBU \_ Timestamp**](ec-dvd-vobu-timestamp.md)                      | Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.                                                                                              |
| [**\_ \_ EC-DVD-WARNUNG**](ec-dvd-warning.md)                                     | Signalisiert eine DVD-Warnungsbedingung.                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> </dl>

 

 



