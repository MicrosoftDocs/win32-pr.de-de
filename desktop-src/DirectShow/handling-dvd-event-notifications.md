---
description: Behandeln von DVD-Ereignis Benachrichtigungen
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Behandeln von DVD-Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958067"
---
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="9ca1a-103">Behandeln von DVD-Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9ca1a-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="9ca1a-104">Der DVD-Navigator sendet Benachrichtigungen an ein von der Anwendung angegebenes Fenster, wenn bestimmte Ereignisse stattfinden, z. b. wenn sich die DVD-Domäne ändert, wenn eine neue Jugend Verwaltungsebene festgelegt wird und der DVD-Navigator im Begriff ist, einen Winkel Block einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="9ca1a-105">Die Ereignis Parameter können zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="9ca1a-106">Außerdem werden Fehlermeldungen und Warnungen auf diese Weise gesendet.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="9ca1a-107">Die Anwendung gibt das Fenster an, in dem die Ereignis Benachrichtigungen behandelt werden, indem der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger zum Aufrufen von [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)wie folgt verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="9ca1a-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="9ca1a-108">Im vorherigen Beispiel \_ ist m HWND das HWND des Fensters, um die Nachrichten zu empfangen, und \_ \_ das WM-DVD-Ereignis ist die Anwendungs definierte Meldung (größer als WM- \_ Benutzer), die signalisiert, dass ein DVD-Ereignis stattfindet.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="9ca1a-109">Das Ereignis selbst wird von der Anwendung durch einen [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)-Befehl abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="9ca1a-110">Da zu einem beliebigen Zeitpunkt mehrere Ereignisse in der Ereignis Warteschlange vorhanden sein können, muss die Anwendung **GetEvent** innerhalb einer Schleife abrufen, die sich wiederholt, bis alle Ereignisse in der Warteschlange abgerufen wurden, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



<span data-ttu-id="9ca1a-111">DVD-Ereignisse können zusätzliche Informationen in den *lParam1* -oder *lParam2* -Parametern enthalten, wie oben gezeigt, wobei die aktuelle Zeit in *lParam1* enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="9ca1a-112">Das vorangehende Codebeispiel basiert auf der DVD-Beispielanwendung in dvdcore. cpp.</span><span class="sxs-lookup"><span data-stu-id="9ca1a-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="9ca1a-113">Eine vollständige Liste aller DVD-Ereignisse und ihrer Parameter finden Sie unter [DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9ca1a-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ca1a-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ca1a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ca1a-115">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9ca1a-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



