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
# <a name="make-a-call"></a><span data-ttu-id="49837-103">Ausführen eines Aufrufes</span><span class="sxs-lookup"><span data-stu-id="49837-103">Make a Call</span></span>

<span data-ttu-id="49837-104">Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein-Objekt erstellen, die dem-Befehl zugeordneten Streams ermitteln, entsprechende Terminals auswählen und erstellen, die Terminals auf den Streams auswählen und die Verbindung beenden.</span><span class="sxs-lookup"><span data-stu-id="49837-104">The following code example demonstrates how to create a call object, discover the streams associated with the call, select and create appropriate terminals, select the terminals onto the streams, and complete the connection.</span></span>

<span data-ttu-id="49837-105">Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md) ausführen und [eine Adresse auswählen](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="49837-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="49837-106">Außerdem müssen Sie die unter [Wählen Sie ein Terminal](select-a-terminal.md) dargestellten Vorgänge durchführen, indem Sie den Aufrufen von " [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)" befolgen.</span><span class="sxs-lookup"><span data-stu-id="49837-106">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the call to [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span></span>

> [!Note]  
> <span data-ttu-id="49837-107">Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="49837-107">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="49837-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49837-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49837-109">**Itaddress:: anatecall**</span><span class="sxs-lookup"><span data-stu-id="49837-109">**ITAddress::CreateCall**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[<span data-ttu-id="49837-110">**Itbasiccallcontrol**</span><span class="sxs-lookup"><span data-stu-id="49837-110">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="49837-111">**Itbasiccallcontrol:: Connect**</span><span class="sxs-lookup"><span data-stu-id="49837-111">**ITBasicCallControl::Connect**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



