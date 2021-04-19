---
description: Das folgende Codebeispiel veranschaulicht die Erstellung eines einfachen Konferenz Aufrufes. Informationen zu IP-Multicast-Multimedia-Videokonferenzen finden Sie unter Informationen zu Rendezvous-IP-telefoniekonferenzen.
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: Erstellen einer einfachen Konferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa0bfd8fede9fa61aedb6b630a2451803e2257d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360663"
---
# <a name="create-a-simple-conference"></a>Erstellen einer einfachen Konferenz

Das folgende Codebeispiel veranschaulicht die Erstellung eines einfachen Konferenz Aufrufes. Informationen zu IP-Multicast-Multimedia-Videokonferenzen finden Sie unter Informationen [zu Rendezvous-IP-telefoniekonferenzen](about-rendezvous-ip-telephony-conferencing.md).

Bevor Sie dieses Codebeispiel verwenden, muss ein-Vorgang ausgeführt werden, und Sie müssen die Vorgänge ausführen, indem Sie [einen-Rückruf](make-a-call.md) ausführen oder [einen-Rückruf empfangen](receive-a-call.md) .

> [!Note]  
> Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**Itcallhub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



