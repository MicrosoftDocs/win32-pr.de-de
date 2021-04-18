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
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="82b56-103">So rufen Sie Ereignisse von einem Benutzeroberflächenautomatisierungs-Anbieter auf</span><span class="sxs-lookup"><span data-stu-id="82b56-103">How to Raise Events from a UI Automation Provider</span></span>

<span data-ttu-id="82b56-104">Dieses Thema enthält Beispielcode, der zeigt, wie ein Microsoft-Benutzeroberflächenautomatisierungs-Anbieter ein Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="82b56-104">This topic contains example code that shows how a Microsoft UI Automation provider raises an event.</span></span>

<span data-ttu-id="82b56-105">Der folgende Beispielcode zeigt eine-Methode aus einer Anwendung, die eine benutzerdefinierte Schaltfläche implementiert.</span><span class="sxs-lookup"><span data-stu-id="82b56-105">The following example code shows a method from an application that implements a custom button.</span></span> <span data-ttu-id="82b56-106">Die Anwendung ruft die-Methode auf, wenn die benutzerdefinierte Schaltfläche aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="82b56-106">The application calls the method whenever the custom button is invoked.</span></span> <span data-ttu-id="82b56-107">Die-Methode überprüft, ob Clients Ereignisse überwachen, und löst, wenn dies der Fall ist, das [**UIA- \_ aufrufen \_ invokedeventid-**](uiauto-event-ids.md) Ereignis aus, um die Clients zu benachrichtigen, dass die Schaltfläche aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="82b56-107">The method checks whether any clients are listening for events and, if so, raises the [**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md) event to notify the clients that the button was invoked.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82b56-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82b56-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82b56-109">**Licher**</span><span class="sxs-lookup"><span data-stu-id="82b56-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82b56-110">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="82b56-110">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="82b56-111">Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="82b56-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




