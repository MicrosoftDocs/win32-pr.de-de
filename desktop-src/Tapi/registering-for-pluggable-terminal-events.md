---
description: Der Ereignis Registrierungsvorgang findet statt, wenn das Terminal von einem Stream ausgewählt wird.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrieren für austauschbare Terminal Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869196"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registrieren für austauschbare Terminal Ereignisse

Der Ereignis Registrierungsvorgang findet statt, wenn das Terminal von einem Stream ausgewählt wird. In der Implementierung der [**selectterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) -Methode der Terminalanwendung können wir die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle des Terminals verwenden, das an den Stream angefügt wurde, und **QueryInterface** aufzurufen, um [**itpluggableterminaleventsink Registration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)zu suchen.

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Wenn der **QueryInterface** -Befehl erfolgreich ausgeführt wurde, können wir die [**registersink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) -Methode aufrufen. Zu diesem Zweck sollten Sie ein Objekt erstellen, das die [**itpluggableterminaleventsink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) -Schnittstelle implementiert. Diese Schnittstelle wird als Parameter der **registersink** -Methode übergeben.

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

Das Terminal, das den [**itpluggableterminaleventsink Registration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) -Befehl implementiert, speichert die-Schnittstelle. Der-Zeiger wird verwendet, wenn das Terminal ein Ereignis auslöst.

Die Registrierung der Ereignis Senke kann mithilfe von [**unregistersink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink)aufgehoben werden.

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
