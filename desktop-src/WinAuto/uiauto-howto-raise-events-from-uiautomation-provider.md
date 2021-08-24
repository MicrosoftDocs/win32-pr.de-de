---
title: Auslösen von Ereignissen von einem Benutzeroberflächenautomatisierung-Anbieter
description: Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter ein Ereignis auslöst.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75717dfcccaca5f62ac3431f9b3decb01842ce9bc696d07bfff54f35ffc13640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133293"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Auslösen von Ereignissen von einem Benutzeroberflächenautomatisierung-Anbieter

Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft Benutzeroberflächenautomatisierung-Anbieter ein Ereignis auslöst.

Der folgende Beispielcode zeigt eine Methode aus einer Anwendung, die eine benutzerdefinierte Schaltfläche implementiert. Die Anwendung ruft die -Methode auf, wenn die benutzerdefinierte Schaltfläche aufgerufen wird. Die -Methode überprüft, ob Clients auf Ereignisse lauschen, und löst in diesem Fall das [**UIA \_ \_ InvokedEventId-Ereignis**](uiauto-event-ids.md) aus, um die Clients zu benachrichtigen, dass die Schaltfläche aufgerufen wurde.


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Anleitungsthemen für Benutzeroberflächenautomatisierung-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




