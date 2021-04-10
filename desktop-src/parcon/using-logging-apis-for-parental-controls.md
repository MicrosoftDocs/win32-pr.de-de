---
description: Verwenden von Protokollierungs-APIs für Eltern Steuerelemente
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Verwenden von Protokollierungs-APIs für Eltern Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865568"
---
# <a name="using-logging-apis-for-parental-controls"></a>Verwenden von Protokollierungs-APIs für Eltern Steuerelemente

### <a name="activity-reporting-logging"></a>Aktivitäts Berichterstattung (Protokollierung)

Die Header Datei "wpcevent. h" enthält Definitionen der Felder für jeden vordefinierten Aktivitäts Ereignistyp und den benutzerdefinierten Typ. Dieser Beispielcode zeigt die Schritte zum Protokollieren eines Einladungs Ereignisses für die Instant Messaging-Konversation mithilfe der etw-Veröffentlichungs-API:


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

Damit eine Anwendung die Ereignisse erweitert, die außerhalb des Satzes von vordefinierten Ereignissen oder eines benutzerdefinierten Typs protokolliert wurden, müssen Sie im Anwendungs Manifest einen Anbieter dafür definieren. Anschließend kann der WPC-Standard Kanal importiert und Anwendungs definierte Ereignisse protokolliert werden.

### <a name="logging-rights"></a>Protokollierungs Rechte

Der WPC-Protokollierungs Kanal wird von der [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) gesteuert, um nur Administratoren vollständigen Zugriff zu gewähren. Nicht-Administrator Konten können auf den Kanal schreiben, haben aber keinen Lese-oder Lösch Zugriff. Der Zugriff auf den Kanal erfolgt mithilfe der ETW-API.

### <a name="parental-controls-logging-provider-details"></a>Details zur Protokollierung des Eltern Steuer Elements

Der WPC-Anbieter hat den Namen "Microsoft.com/Windows/parentalcontrols" mit der GUID {01090065-B467-4503-9b28-533766761087}. Der standardmäßige lokale Protokollierungs Kanal ist Microsoft.com/Windows/parentalcontrols/LocalEvents.

Protokolldateien werden im Ordner "Windows \\ system32 \\ WPC \\ Logs" gespeichert.

### <a name="notification-of-impending-time-limits-logout"></a>Benachrichtigung über bevorstehende Zeit Limits bei der Abmeldung

Das Jugend Steuerungssystem gibt ein Warn Ereignis innerhalb von 15 Minuten und erneut in 1 Minute vor der Abmeldung eines kontrollierten Benutzers auf der Grundlage von Zeitbeschränkungen aus. Anwendungen können diese Ereignisse abonnieren, insbesondere dann, wenn Sie im Vollbildmodus von DirectX ausgeführt werden, in dem keine standardmäßigen Windows-Benachrichtigungen angezeigt werden. Der Beispielcode zeigt, wie Sie die-Ereignisse abonnieren, eine Rückruffunktion registrieren und die-Ereignisse empfangen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Erweiterbarkeits Features für Eltern Steuerelemente](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**Ereignis \_ Daten \_ Deskriptor**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ args \_ Conversation ationinitevent**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
