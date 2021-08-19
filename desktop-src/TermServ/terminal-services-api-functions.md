---
title: Remotedesktopdienste-API-Funktionen
description: Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434f009d15bccc1db8279e576b71f079c8d73119a2d82bb8fd313dcc1837c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000250"
---
# <a name="remote-desktop-services-api-functions"></a>Remotedesktopdienste-API-Funktionen

Die folgenden Funktionen werden mit Remotedesktopdienste verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Ruft die Remotedesktopdienste Sitzung ab, die einem angegebenen Prozess zugeordnet ist.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Öffnet ein Handle für den angegebenen Remotedesktop Lizenzserver.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Schließt ein geöffnetes Handle für einen Remotedesktop Lizenzserver.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Beginnt die Enumeration durch alle Schlüsselpakete, die basierend auf Suchkriterien auf einem Remotedesktop Lizenzserver installiert sind.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Setzt einen vorherigen Aufruf der [**TLSKeyPackEnumBegin-Funktion**](tlskeypackenumbegin.md) fort und beendet die -Enumeration.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Setzt einen vorherigen Aufruf der [**TLSKeyPackEnumBegin-Funktion**](tlskeypackenumbegin.md) fort und gibt das nächste Schlüsselpaket zurück, das auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Setzt einen vorherigen Aufruf der [**TLSLicenseEnumBegin-Funktion**](tlslicenseenumbegin.md) fort und beendet die -Enumeration.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Setzt einen vorherigen Aufruf der [**TLSLicenseEnumBegin-Funktion**](tlslicenseenumbegin.md) fort und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Schließt das Clientende eines virtuellen Kanals.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Ein anwendungsdefinierter Einstiegspunkt für die clientseitige DLL einer Anwendung, die Remotedesktopdienste virtuellen Kanälen verwendet.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Initialisiert den Zugriff einer Client-DLL auf Remotedesktopdienste virtuelle Kanäle.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Eine anwendungsdefinierte Rückruffunktion, die Aufrufe Remotedesktopdienste, um die Client-DLL über Ereignisse des virtuellen Kanals zu benachrichtigen.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Öffnet das Clientende eines virtuellen Kanals.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Eine anwendungsdefinierte Rückruffunktion, die Aufrufe Remotedesktopdienste, um die Client-DLL über Ereignisse für einen bestimmten virtuellen Kanal zu benachrichtigen.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Sendet Daten vom Clientende eines virtuellen Kanals an eine Partneranwendung auf dem Serverende.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Schließt ein geöffnetes Handle für einen Remotedesktop-Sitzungshost -Server (RD-Sitzungshost).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Verbindet eine Remotedesktopdienste Sitzung mit einer vorhandenen Sitzung auf dem lokalen Computer.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Erstellt einen neuen Remotedesktopdienste Listener oder konfiguriert einen vorhandenen Listener.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Trennt den angemeldeten Benutzer von der angegebenen Remotedesktopdienste Sitzung, ohne die Sitzung zu schließen.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Aktiviert oder deaktiviert [untergeordnete Sitzungen.](child-sessions.md)

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Listet alle Remotedesktopdienste Listener auf einem RD-Sitzungshost Server auf.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Ruft Informationen zu den aktiven Prozessen auf einem angegebenen RD-Sitzungshost Server ab.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Ruft Informationen zu den aktiven Prozessen auf dem angegebenen RD-Sitzungshost server oder Remotedesktop Virtualization Host (RD Virtualization Host)-Server ab.

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Gibt eine Liste aller RD-Sitzungshost Server innerhalb der angegebenen Domäne zurück.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Ruft eine Liste von Sitzungen auf einem RD-Sitzungshost Server ab.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Ruft eine Liste von Sitzungen auf einem angegebenen RD-Sitzungshost Server oder RD-Virtualisierungshostserver ab.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Gibt von einer Remotedesktopdienste Funktion belegten Arbeitsspeicher frei.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Gibt Arbeitsspeicher frei, [**der WTS PROCESS INFO \_ \_ \_ EX-**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) oder [**WTS SESSION INFO \_ \_ \_ 1-Strukturen**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) enthält, die von einer Remotedesktopdienste-Funktion zugeordnet werden.

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Ruft den Sitzungsbezeichner der Konsolensitzung ab.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Ruft den bezeichner der untergeordneten Sitzung ab, sofern vorhanden.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Ruft die Sicherheitsbeschreibung eines Remotedesktopdienste Listeners ab.

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Bestimmt, ob untergeordnete Sitzungen aktiviert sind.

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Protokolliert eine angegebene Remotedesktopdienste Sitzung.

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Öffnet ein Handle für den angegebenen RD-Sitzungshost Server.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Öffnet ein Handle für den angegebenen RD-Sitzungshost Server oder RD-Virtualisierungshostserver.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Ruft Konfigurationsinformationen für einen Remotedesktopdienste Listener ab.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Ruft Sitzungsinformationen für die angegebene Sitzung auf dem angegebenen RD-Sitzungshost Server ab.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Ruft Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänencontroller oder RD-Sitzungshost Server ab.

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Ruft das primäre Zugriffstoken des angemeldeten Benutzers ab, der durch die Sitzungs-ID angegeben wird.

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Registriert das angegebene Fenster, um Sitzungsänderungsbenachrichtigungen zu empfangen.

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Registriert das angegebene Fenster, um Sitzungsänderungsbenachrichtigungen zu empfangen.

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Zeigt ein Meldungsfeld auf dem Clientdesktop einer angegebenen Remotedesktopdienste Sitzung an.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Konfiguriert die Sicherheitsbeschreibung eines Remotedesktopdienste Listeners.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Ändert Konfigurationsinformationen für den angegebenen Benutzer auf dem angegebenen Domänencontroller oder RD-Sitzungshost Server.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Fährt den angegebenen RD-Sitzungshost Server herunter (und startet optional neu).

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Startet die Remotesteuerung einer anderen Remotedesktopdienste Sitzung. Sie müssen diese Funktion aus einer Remotesitzung aufrufen.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Beendet eine Remotesteuerungssitzung.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Beendet den angegebenen Prozess auf dem angegebenen RD-Sitzungshost Server.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Aufheben der Registrierung des angegebenen Fensters, sodass keine weiteren Sitzungsänderungsbenachrichtigungen empfangen werden.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Aufheben der Registrierung des angegebenen Fensters, sodass keine weiteren Sitzungsänderungsbenachrichtigungen empfangen werden.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Schließt ein geöffnetes Handle für virtuelle Kanäle.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Öffnet ein Handle für das Serverende eines angegebenen virtuellen Kanals.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Erstellt einen virtuellen Kanal auf ähnliche Weise wie [**WTSVirtualChannelOpen.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Löscht alle Eingabedaten in der Warteschlange, die vom Client an den Server in einem angegebenen virtuellen Kanal gesendet werden.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Löscht alle Ausgabedaten in der Warteschlange, die vom Server an den Client in einem angegebenen virtuellen Kanal gesendet werden.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Liest Daten vom Serverende eines virtuellen Kanals.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Schreibt Daten in das Serverende eines virtuellen Kanals.

</dd> <dt>

[**Wtswaitsystemevent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Wartet auf ein Remotedesktopdienste Ereignis, bevor an den Aufrufer zurückgegeben wird.

</dd> </dl>

 

 