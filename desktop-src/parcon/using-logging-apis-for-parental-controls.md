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
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="97efb-103">Verwenden von Protokollierungs-APIs für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="97efb-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="97efb-104">Aktivitäts Berichterstattung (Protokollierung)</span><span class="sxs-lookup"><span data-stu-id="97efb-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="97efb-105">Die Header Datei "wpcevent. h" enthält Definitionen der Felder für jeden vordefinierten Aktivitäts Ereignistyp und den benutzerdefinierten Typ.</span><span class="sxs-lookup"><span data-stu-id="97efb-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="97efb-106">Dieser Beispielcode zeigt die Schritte zum Protokollieren eines Einladungs Ereignisses für die Instant Messaging-Konversation mithilfe der etw-Veröffentlichungs-API:</span><span class="sxs-lookup"><span data-stu-id="97efb-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


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



### <a name="custom-logging"></a><span data-ttu-id="97efb-107">Benutzerdefinierte Protokollierung</span><span class="sxs-lookup"><span data-stu-id="97efb-107">Custom Logging</span></span>

<span data-ttu-id="97efb-108">Damit eine Anwendung die Ereignisse erweitert, die außerhalb des Satzes von vordefinierten Ereignissen oder eines benutzerdefinierten Typs protokolliert wurden, müssen Sie im Anwendungs Manifest einen Anbieter dafür definieren.</span><span class="sxs-lookup"><span data-stu-id="97efb-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="97efb-109">Anschließend kann der WPC-Standard Kanal importiert und Anwendungs definierte Ereignisse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="97efb-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="97efb-110">Protokollierungs Rechte</span><span class="sxs-lookup"><span data-stu-id="97efb-110">Logging Rights</span></span>

<span data-ttu-id="97efb-111">Der WPC-Protokollierungs Kanal wird von der [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) gesteuert, um nur Administratoren vollständigen Zugriff zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="97efb-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="97efb-112">Nicht-Administrator Konten können auf den Kanal schreiben, haben aber keinen Lese-oder Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="97efb-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="97efb-113">Der Zugriff auf den Kanal erfolgt mithilfe der ETW-API.</span><span class="sxs-lookup"><span data-stu-id="97efb-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="97efb-114">Details zur Protokollierung des Eltern Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="97efb-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="97efb-115">Der WPC-Anbieter hat den Namen "Microsoft.com/Windows/parentalcontrols" mit der GUID {01090065-B467-4503-9b28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="97efb-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="97efb-116">Der standardmäßige lokale Protokollierungs Kanal ist Microsoft.com/Windows/parentalcontrols/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="97efb-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="97efb-117">Protokolldateien werden im Ordner "Windows \\ system32 \\ WPC \\ Logs" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="97efb-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="97efb-118">Benachrichtigung über bevorstehende Zeit Limits bei der Abmeldung</span><span class="sxs-lookup"><span data-stu-id="97efb-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="97efb-119">Das Jugend Steuerungssystem gibt ein Warn Ereignis innerhalb von 15 Minuten und erneut in 1 Minute vor der Abmeldung eines kontrollierten Benutzers auf der Grundlage von Zeitbeschränkungen aus.</span><span class="sxs-lookup"><span data-stu-id="97efb-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="97efb-120">Anwendungen können diese Ereignisse abonnieren, insbesondere dann, wenn Sie im Vollbildmodus von DirectX ausgeführt werden, in dem keine standardmäßigen Windows-Benachrichtigungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="97efb-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="97efb-121">Der Beispielcode zeigt, wie Sie die-Ereignisse abonnieren, eine Rückruffunktion registrieren und die-Ereignisse empfangen.</span><span class="sxs-lookup"><span data-stu-id="97efb-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97efb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97efb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97efb-123">Übersicht über die Erweiterbarkeits Features für Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="97efb-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="97efb-124">**Ereignis \_ Daten \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="97efb-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="97efb-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="97efb-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="97efb-126">**WPC \_ args \_ Conversation ationinitevent**</span><span class="sxs-lookup"><span data-stu-id="97efb-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
