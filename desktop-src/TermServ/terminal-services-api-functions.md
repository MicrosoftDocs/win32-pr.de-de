---
title: Remotedesktopdienste API-Funktionen
description: Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727977"
---
# <a name="remote-desktop-services-api-functions"></a>Remotedesktopdienste API-Funktionen

Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Processidtosessionid**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Ruft die Remotedesktopdienste Sitzung ab, die einem angegebenen Prozess zugeordnet ist.

</dd> <dt>

[**Tlsconnecttolsserver**](tlsconnecttolsserver.md)
</dt> <dd>

Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.

</dd> <dt>

[**Tlsdisconnectfromserver**](tlsdisconnectfromserver.md)
</dt> <dd>

Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.

</dd> <dt>

[**Tlsgetservercertificate**](tlsgetservercertificate.md)
</dt> <dd>

Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.

</dd> <dt>

[**Tlskeypackenumbegin**](tlskeypackenumbegin.md)
</dt> <dd>

Beginnt die Enumeration über alle auf einem Remotedesktop Lizenzserver installierten Schlüsselpakete auf der Grundlage von Suchkriterien.

</dd> <dt>

[**Tlskeypackenumend**](tlskeypackenumend.md)
</dt> <dd>

Wird von einem vorherigen-Befehl der [**tlskeypackenumbegin**](tlskeypackenumbegin.md) -Funktion fortgesetzt und beendet die-Enumeration.

</dd> <dt>

[**Tlskeypackenumnext**](tlskeypackenumnext.md)
</dt> <dd>

Wird von einem vorherigen-Befehl der [**tlskeypackenumbegin**](tlskeypackenumbegin.md) -Funktion fortgesetzt und gibt das nächste Key Pack zurück, das auf einem Remotedesktop-Lizenzserver installiert ist, der den Suchkriterien entspricht.

</dd> <dt>

[**Tlslicenseenumbegin**](tlslicenseenumbegin.md)
</dt> <dd>

Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.

</dd> <dt>

[**Tlslicenabenumend**](tlslicenseenumend.md)
</dt> <dd>

Wird von einem vorherigen-Befehl der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und beendet die-Enumeration.

</dd> <dt>

[**Tlslicensitztenenumnext**](tlslicenseenumnext.md)
</dt> <dd>

Wird von einem vorherigen aufrufsvorgang der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.

</dd> <dt>

[**Virtualchannelclose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Schließt das Client Ende eines virtuellen Kanals.

</dd> <dt>

[**Virtualchannelentry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Ein Anwendungs definierter Einstiegspunkt für die Client seitige dll einer Anwendung, die Remotedesktopdienste virtuellen Kanälen verwendet.

</dd> <dt>

[**Virtualchannelinit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Initialisiert den Zugriff einer Client-DLL auf Remotedesktopdienste virtuellen Channels.

</dd> <dt>

[*Virtualchannelinitevent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Eine von der Anwendung definierte Rückruffunktion, Remotedesktopdienste die aufruft, um die Client-DLL von virtuellen Kanal Ereignissen zu benachrichtigen.

</dd> <dt>

[**Virtualchannelopen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Öffnet das Client Ende eines virtuellen Kanals.

</dd> <dt>

[*Virtualchannelopenevent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Eine von der Anwendung definierte Rückruffunktion, mit der aufgerufen wird Remotedesktopdienste, um die Client-DLL über Ereignisse für einen bestimmten virtuellen Kanal zu benachrichtigen.

</dd> <dt>

[**Virtualchannelwrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Sendet Daten vom Client Ende eines virtuellen Kanals an eine Partner Anwendung auf dem Server Ende.

</dd> <dt>

[**Wtscloseserver**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Schließt ein geöffnetes Handle für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost).

</dd> <dt>

[**Wzconneczession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Verbindet eine Remotedesktopdienste Sitzung mit einer vorhandenen Sitzung auf dem lokalen Computer.

</dd> <dt>

[**Wtscreatelistener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Erstellt einen neuen Remotedesktopdienste Listener oder konfiguriert einen vorhandenen Listener.

</dd> <dt>

[**Wzdisconneczession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Trennt den angemeldeten Benutzer von der angegebenen Remotedesktopdienste Sitzung, ohne die Sitzung zu schließen.

</dd> <dt>

[**Wtsenablechildsessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Aktiviert oder deaktiviert untergeordnete [Sitzungen](child-sessions.md).

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Listet alle Remotedesktopdienste Listener auf einem RD-Sitzungshost Server auf.

</dd> <dt>

[**Wtsenum erateprocesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Ruft Informationen zu den aktiven Prozessen auf einem angegebenen RD-Sitzungshost Server ab.

</dd> <dt>

[**Wtsenenerateprocessesex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Ruft Informationen zu den aktiven Prozessen auf dem angegebenen RD-Sitzungshost Server oder Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) ab.

</dd> <dt>

[**Wtsenum erateservers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Gibt eine Liste aller RD-Sitzungshost Server innerhalb der angegebenen Domäne zurück.

</dd> <dt>

[**Wtseneneratesessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Ruft eine Liste von Sitzungen auf einem RD-Sitzungshost Server ab.

</dd> <dt>

[**Wtseneneratesessionsex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Ruft eine Liste von Sitzungen auf einem angegebenen RD-Sitzungshost Server oder Remote Desktop-Virtualisierungshostserver ab.

</dd> <dt>

[**Wout-Speicher**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Gibt durch eine Remotedesktopdienste Funktion zugeordnete Arbeitsspeicher frei.

</dd> <dt>

[**Wout-memoryex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Gibt Arbeitsspeicher frei, der die von einer Remotedesktopdienste Funktion zugeordneten Strukturen der [**WTS \_ Process \_ Info \_ Ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) oder der [**WTS \_ Session \_ Info \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) enthält.

</dd> <dt>

[**Wout getactiveconsolesessionid**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Ruft den Sitzungs Bezeichner der Konsolen Sitzung ab.

</dd> <dt>

[**Wout getchildsessionid**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Ruft den Bezeichner der untergeordneten Sitzung ab, falls vorhanden.

</dd> <dt>

[**Wtgetlistenersecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Ruft die Sicherheits Beschreibung eines Remotedesktopdienste Listener ab.

</dd> <dt>

[**Wtsischildsessionsenabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Bestimmt, ob untergeordnete Sitzungen aktiviert sind.

</dd> <dt>

[**Wunglogoffsession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Protokolliert eine angegebene Remotedesktopdienste Sitzung ab.

</dd> <dt>

[**Wout OpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Öffnet ein Handle für den angegebenen RD-Sitzungshost Server.

</dd> <dt>

[**Wout openserverex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Öffnet ein Handle für den angegebenen RD-Sitzungshost Server oder Remote Desktop-Virtualisierungshostserver.

</dd> <dt>

[**Wout querylistenerconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Ruft Konfigurationsinformationen für einen Remotedesktopdienste Listener ab.

</dd> <dt>

[**Wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Ruft Sitzungsinformationen für die angegebene Sitzung auf dem angegebenen RD-Sitzungshost Server ab.

</dd> <dt>

[**Wout queryuserconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Ruft Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänen Controller oder RD-Sitzungshost Server ab.

</dd> <dt>

[**Wtqueryusertoken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Ruft das primäre Zugriffs Token des angemeldeten Benutzers ab, der von der Sitzungs-ID angegeben wird.

</dd> <dt>

[**Wwahrheits registersessionnotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Registriert das angegebene Fenster für den Empfang von Sitzungs Änderungs Benachrichtigungen.

</dd> <dt>

[**Wzregistersessionnotificationex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Registriert das angegebene Fenster für den Empfang von Sitzungs Änderungs Benachrichtigungen.

</dd> <dt>

[**Wtssendmessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Zeigt ein Meldungs Feld auf dem Client Desktop einer angegebenen Remotedesktopdienste Sitzung an.

</dd> <dt>

[**Wtsetlistenersecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Konfiguriert die Sicherheits Beschreibung eines Remotedesktopdienste Listener.

</dd> <dt>

[**Wout-tuserconfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Ändert die Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänen Controller oder RD-Sitzungshost Server.

</dd> <dt>

[**Wungshutdownsystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Fährt den angegebenen RD-Sitzungshost Server herunter (und startet ihn optional neu).

</dd> <dt>

[**Wout startremotecontrolsession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Startet die Remote Steuerung einer anderen Remotedesktopdienste Sitzung. Diese Funktion muss von einer Remote Sitzung aus aufgerufen werden.

</dd> <dt>

[**Wout stopremotecontrolsession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Beendet eine Remote Steuerungs Sitzung.

</dd> <dt>

[**Wtsterminateprocess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Beendet den angegebenen Prozess auf dem angegebenen RD-Sitzungshost Server.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Hebt die Registrierung des angegebenen Fensters auf, sodass keine weiteren Sitzungs Änderungs Benachrichtigungen empfangen werden.

</dd> <dt>

[**Wtsunregistersessionnotificationex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Hebt die Registrierung des angegebenen Fensters auf, sodass keine weiteren Sitzungs Änderungs Benachrichtigungen empfangen werden.

</dd> <dt>

[**Wout virtualchannelclose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Schließt einen geöffneten virtuellen Kanal handle.

</dd> <dt>

[**Wout virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Öffnet ein Handle für das Server Ende eines angegebenen virtuellen Kanals.

</dd> <dt>

[**Wout virtualchannelopenex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Erstellt einen virtuellen Kanal auf eine Weise, die dem [**Wout-virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)ähnelt.

</dd> <dt>

[**WGs virtualchannelpurgeinput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Löscht alle in die Warteschlange eingereihten Eingabedaten, die vom Client an den Server auf einem angegebenen virtuellen Kanal gesendet werden.

</dd> <dt>

[**Wzvirtualchannelpurgeoutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Löscht alle in die Warteschlange eingereihten Ausgabedaten, die vom Server an den Client auf einem angegebenen virtuellen Kanal gesendet werden.

</dd> <dt>

[**Wout virtualchannelquery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.

</dd> <dt>

[**Wout virtualchannelread**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Liest Daten vom Server Ende eines virtuellen Kanals.

</dd> <dt>

[**Wout virtualchannelwrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Schreibt Daten auf das Server Ende eines virtuellen Kanals.

</dd> <dt>

[**Wout waitsystemevent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Wartet auf ein Remotedesktopdienste Ereignis, bevor es zum Aufrufer zurückkehrt.

</dd> </dl>

 

 