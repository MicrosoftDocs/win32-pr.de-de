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
# <a name="receive-a-call"></a>Empfangen eines Aufrufes

Im folgenden Codebeispiel wird die Behandlung von neuen Rückruf Benachrichtigungen veranschaulicht, z. b. das Suchen oder erstellen geeigneter Terminals zum Rendering der Medien. Dieses Beispiel ist ein Teil der Switch-Anweisung, die eine Anwendung für die Ereignis Behandlung implementieren muss. Der Code selbst kann in der Implementierung von [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)enthalten sein, oder die **Ereignis** Methode sendet eine Nachricht an einen Arbeits Thread, der den Schalter enthält.

Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md)ausführen, [eine Adresse auswählen](select-an-address.md)und [Ereignisse registrieren](register-events.md).

Außerdem müssen Sie die in [Auswählen eines Terminals](select-a-terminal.md) dargestellten Vorgänge nach dem Abrufen der Schnittstellen Zeiger [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) und [**itaddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) ausführen.

> [!Note]  
> Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.

 

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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignisse](events.md)
</dt> <dt>

[**Ittapieventnotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**Ittapi:: registercallbenachrichtigungen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**Itcallnotificationevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**Itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**Itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
