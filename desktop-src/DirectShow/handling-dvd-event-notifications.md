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
# <a name="handling-dvd-event-notifications"></a>Behandeln von DVD-Ereignis Benachrichtigungen

Der DVD-Navigator sendet Benachrichtigungen an ein von der Anwendung angegebenes Fenster, wenn bestimmte Ereignisse stattfinden, z. b. wenn sich die DVD-Domäne ändert, wenn eine neue Jugend Verwaltungsebene festgelegt wird und der DVD-Navigator im Begriff ist, einen Winkel Block einzugeben. Die Ereignis Parameter können zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen. Außerdem werden Fehlermeldungen und Warnungen auf diese Weise gesendet. Die Anwendung gibt das Fenster an, in dem die Ereignis Benachrichtigungen behandelt werden, indem der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Zeiger zum Aufrufen von [**setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)wie folgt verwendet wird:


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



Im vorherigen Beispiel \_ ist m HWND das HWND des Fensters, um die Nachrichten zu empfangen, und \_ \_ das WM-DVD-Ereignis ist die Anwendungs definierte Meldung (größer als WM- \_ Benutzer), die signalisiert, dass ein DVD-Ereignis stattfindet. Das Ereignis selbst wird von der Anwendung durch einen [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)-Befehl abgerufen. Da zu einem beliebigen Zeitpunkt mehrere Ereignisse in der Ereignis Warteschlange vorhanden sein können, muss die Anwendung **GetEvent** innerhalb einer Schleife abrufen, die sich wiederholt, bis alle Ereignisse in der Warteschlange abgerufen wurden, wie im folgenden Codebeispiel gezeigt.


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



DVD-Ereignisse können zusätzliche Informationen in den *lParam1* -oder *lParam2* -Parametern enthalten, wie oben gezeigt, wobei die aktuelle Zeit in *lParam1* enthalten ist. Das vorangehende Codebeispiel basiert auf der DVD-Beispielanwendung in dvdcore. cpp. Eine vollständige Liste aller DVD-Ereignisse und ihrer Parameter finden Sie unter [DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



