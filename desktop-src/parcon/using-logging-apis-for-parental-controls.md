---
description: Verwenden von Protokollierungs-APIs für Jugendschutz
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Verwenden von Protokollierungs-APIs für Jugendschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 571a24f8bdbf687f8c1975cfc29057035ac56747edc0459682512531194c55a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869062"
---
# <a name="using-logging-apis-for-parental-controls"></a>Verwenden von Protokollierungs-APIs für Jugendschutz

### <a name="activity-reporting-logging"></a>Aktivitätsberichterstattung (Protokollierung)

Die WpcEvent.h-Headerdatei enthält Definitionen der Felder für jeden vordefinierten Aktivitätsereignistyp und den benutzerdefinierten Typ. Dieser Beispielcode zeigt die Schritte zum Protokollieren eines Chat-Konversationseinladungsereignis mithilfe der ETW-Veröffentlichungs-API:


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a>Benutzerdefinierte Protokollierung

Damit eine Anwendung die Ereignisse erweitert, die außerhalb der vordefinierten Ereignisse oder des benutzerdefinierten Typs protokolliert werden, müssen Sie einen Anbieter für diesen im Anwendungsmanifest definieren. Der WPC-Standardkanal kann dann importiert werden, und anwendungsdefinierte Ereignisse können dann protokolliert werden.

### <a name="logging-rights"></a>Protokollierungsrechte

Der WPC-Protokollierungskanal wird über die [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) (Access Control List, ACL) gesteuert, um nur Administratoren Vollzugriff zu bieten. Konten ohne Administratorrechte schreiben möglicherweise in den Kanal, haben aber keinen Lese- oder Löschzugriff. Der Zugriff auf den Kanal wird über die ETW-API ermöglicht.

### <a name="parental-controls-logging-provider-details"></a>Details des Protokollierungsanbieters für Die Jugendschutzkontrollen

Der WPC-Anbieter heißt Microsoft.com/Windows/ParentalControls mit GUID {01090065-B467-4503-9B28-533766761087}. Der lokale Standardprotokollierungskanal ist Microsoft.com/Windows/ParentalControls/LocalEvents.

Protokolldateien werden im Windows \\ System32 \\ \\ Wpc-Protokollordner gespeichert.

### <a name="notification-of-impending-time-limits-logout"></a>Benachrichtigung über bevorstehende Abmeldung von Zeitlimits

Das System für die Jugendkontrolle gibt ein Warnereignis nach 15 Minuten und erneut um 1 Minute vor der Abmelde eines kontrollierten Benutzers basierend auf Zeitbeschränkungen aus. Anwendungen können diese Ereignisse abonnieren, insbesondere wenn sie im DirectX-Vollbildmodus ausgeführt werden, in dem Windows Standardbenachrichtigungen nicht angezeigt werden. Beispielcode wird bereitgestellt, der zeigt, wie die Ereignisse abonniert, eine Rückruffunktion registriert und die Ereignisse empfangen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Erweiterbarkeitsfunktionen für Jugendschutz](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**\_ \_ EREIGNISDATENDESKRIPTOR**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
