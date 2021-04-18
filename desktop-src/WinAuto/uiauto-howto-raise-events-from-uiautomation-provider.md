---
title: So rufen Sie Ereignisse von einem Benutzeroberflächenautomatisierungs-Anbieter auf
description: Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft-Benutzeroberflächenautomatisierungs-Anbieter ein Ereignis auslöst.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337609"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>So rufen Sie Ereignisse von einem Benutzeroberflächenautomatisierungs-Anbieter auf

Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft-Benutzeroberflächenautomatisierungs-Anbieter ein Ereignis auslöst.

Der folgende Beispielcode zeigt eine-Methode aus einer Anwendung, die eine benutzerdefinierte Schaltfläche implementiert. Die Anwendung ruft die-Methode auf, wenn die benutzerdefinierte Schaltfläche aufgerufen wird. Die-Methode überprüft, ob Clients Ereignisse überwachen, und löst, wenn dies der Fall ist, das [**UIA- \_ aufrufen \_ invokedeventid-**](uiauto-event-ids.md) Ereignis aus, um die Clients zu benachrichtigen, dass die Schaltfläche aufgerufen wurde.


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

**Licher**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




