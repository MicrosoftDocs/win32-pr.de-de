---
description: Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein-Objekt erstellen, die dem-Befehl zugeordneten Streams ermitteln, entsprechende Terminals auswählen und erstellen, die Terminals auf den Streams auswählen und die Verbindung beenden.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Ausführen eines Aufrufes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348529"
---
# <a name="make-a-call"></a>Ausführen eines Aufrufes

Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein-Objekt erstellen, die dem-Befehl zugeordneten Streams ermitteln, entsprechende Terminals auswählen und erstellen, die Terminals auf den Streams auswählen und die Verbindung beenden.

Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md) ausführen und [eine Adresse auswählen](select-an-address.md).

Außerdem müssen Sie die unter [Wählen Sie ein Terminal](select-a-terminal.md) dargestellten Vorgänge durchführen, indem Sie den Aufrufen von " [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)" befolgen.

> [!Note]  
> Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**Itbasiccallcontrol:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



