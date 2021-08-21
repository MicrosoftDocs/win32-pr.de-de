---
description: Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein Aufrufobjekt erstellen, die dem Aufruf zugeordneten Streams entdecken, geeignete Terminals auswählen und erstellen, die Terminals in den Streams auswählen und die Verbindung abschließen.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Anruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb83f42bb4219cd47d38ddf98331b7889efb89efeddd040d614b4f601325aa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863246"
---
# <a name="make-a-call"></a>Anruf

Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein Aufrufobjekt erstellen, die dem Aufruf zugeordneten Streams entdecken, geeignete Terminals auswählen und erstellen, die Terminals in den Streams auswählen und die Verbindung abschließen.

Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in Initialisieren von [TAPI und](initialize-tapi.md) [Auswählen einer Adresse ausführen.](select-an-address.md)

Darüber hinaus müssen Sie die vorgänge ausführen, die unter Auswählen eines [Terminals](select-a-terminal.md) nach dem Aufruf von [**ITAddress::CreateCall dargestellt sind.**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)

> [!Note]  
> In diesem Beispiel sind die Fehlerüberprüfung und die für Produktionscode geeigneten Releases nicht enthalten.

 

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

[**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITBasicCallControl::Verbinden**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



