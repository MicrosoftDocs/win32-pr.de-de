---
description: Der Ereignisregistrierungsprozess findet statt, wenn das Terminal durch einen Stream ausgewählt wird.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrieren für pluggable-Terminalereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060458"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registrieren für pluggable-Terminalereignisse

Der Ereignisregistrierungsprozess findet statt, wenn das Terminal durch einen Stream ausgewählt wird. In der Implementierung der [**SelectTerminal-Methode**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) der Terminalanwendung können wir die [**ITTerminal-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) des Terminals verwenden, das an den Stream angefügt wurde, und **QueryInterface** aufrufen, um [**ITPluggableTerminalEventSinkRegistration zu finden.**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Wenn der **QueryInterface-Aufruf** erfolgreich ist, können wir die [**RegisterSink-Methode**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) aufrufen. Zu diesem Zweck sollten wir ein Objekt erstellen, das die [**ITPluggableTerminalEventSink-Schnittstelle**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) implementiert. Wir übergeben diese Schnittstelle als Parameter der **RegisterSink-Methode.**

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

Im Terminal, das den [**ITPluggableTerminalEventSinkRegistration-Aufruf**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) implementiert, wird die Schnittstelle gespeichert. Der -Zeiger wird verwendet, wenn das Terminal ein Ereignis auslagert.

Die Registrierung der Ereignissenke kann mithilfe von [**UnregisterSink aufgehoben werden.**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink)

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
