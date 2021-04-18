---
description: Im folgenden Codebeispiel wird die Behandlung von neuen Rückruf Benachrichtigungen veranschaulicht, z. b. das Suchen oder erstellen geeigneter Terminals zum Rendering der Medien.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Empfangen eines Aufrufes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352697"
---
# <a name="receive-a-call"></a><span data-ttu-id="2a8a4-103">Empfangen eines Aufrufes</span><span class="sxs-lookup"><span data-stu-id="2a8a4-103">Receive a Call</span></span>

<span data-ttu-id="2a8a4-104">Im folgenden Codebeispiel wird die Behandlung von neuen Rückruf Benachrichtigungen veranschaulicht, z. b. das Suchen oder erstellen geeigneter Terminals zum Rendering der Medien.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-104">The following code example demonstrates handling of new call notifications, such as finding or creating appropriate terminals to render the media.</span></span> <span data-ttu-id="2a8a4-105">Dieses Beispiel ist ein Teil der Switch-Anweisung, die eine Anwendung für die Ereignis Behandlung implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-105">This example is a portion of the switch statement an application must implement for event handling.</span></span> <span data-ttu-id="2a8a4-106">Der Code selbst kann in der Implementierung von [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)enthalten sein, oder die **Ereignis** Methode sendet eine Nachricht an einen Arbeits Thread, der den Schalter enthält.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-106">The code itself may be contained in the implementation of [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), or the **Event** method may post a message to a worker thread that contains the switch.</span></span>

<span data-ttu-id="2a8a4-107">Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md)ausführen, [eine Adresse auswählen](select-an-address.md)und [Ereignisse registrieren](register-events.md).</span><span class="sxs-lookup"><span data-stu-id="2a8a4-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md), [Select an Address](select-an-address.md), and [Register Events](register-events.md).</span></span>

<span data-ttu-id="2a8a4-108">Außerdem müssen Sie die in [Auswählen eines Terminals](select-a-terminal.md) dargestellten Vorgänge nach dem Abrufen der Schnittstellen Zeiger [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) und [**itaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-108">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the retrieval of the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) interface pointers.</span></span>

> [!Note]  
> <span data-ttu-id="2a8a4-109">Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="2a8a4-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="2a8a4-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a8a4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a8a4-111">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2a8a4-111">Events</span></span>](events.md)
</dt> <dt>

[<span data-ttu-id="2a8a4-112">**Ittapieventnotification**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[<span data-ttu-id="2a8a4-113">**Ittapi:: registercallbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-113">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[<span data-ttu-id="2a8a4-114">**Itcallnotificationevent**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-114">**ITCallNotificationEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[<span data-ttu-id="2a8a4-115">**Itcallinfo**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-115">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="2a8a4-116">**Itbasiccallcontrol**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-116">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="2a8a4-117">**Itterminalsupport**</span><span class="sxs-lookup"><span data-stu-id="2a8a4-117">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
