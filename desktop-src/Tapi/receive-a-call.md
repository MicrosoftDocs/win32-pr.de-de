---
description: Im folgenden Codebeispiel wird die Behandlung neuer Aufrufbenachrichtigungen veranschaulicht, z. B. das Suchen oder Erstellen geeigneter Terminals zum Rendern der Medien.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Empfangen eines Anrufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e4ce02ec11a1373d16b9b9ebd0fba29313b1d532175894c6fd1b12a38e2bf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060468"
---
# <a name="receive-a-call"></a>Empfangen eines Anrufs

Im folgenden Codebeispiel wird die Behandlung neuer Aufrufbenachrichtigungen veranschaulicht, z. B. das Suchen oder Erstellen geeigneter Terminals zum Rendern der Medien. Dieses Beispiel ist ein Teil der switch-Anweisung, den eine Anwendung für die Ereignisbehandlung implementieren muss. Der Code selbst kann in der Implementierung von [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)enthalten sein, oder die **Event-Methode** kann eine Nachricht an einen Arbeitsthread senden, der den Schalter enthält.

Bevor Sie dieses Codebeispiel verwenden können, müssen Sie die Vorgänge in Initialisieren von [TAPI,](initialize-tapi.md) [Auswählen einer Adresse](select-an-address.md)und Registrieren von Ereignissen [ausführen.](register-events.md)

Außerdem müssen Sie die vorgänge ausführen, die unter Auswählen eines [Terminals](select-a-terminal.md) nach dem Abrufen der [**Schnittstellenzeige ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) und [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) veranschaulicht werden.

> [!Note]  
> In diesem Beispiel sind die Fehlerüberprüfung und die für Produktionscode geeigneten Releases nicht enthalten.

 

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

[**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
