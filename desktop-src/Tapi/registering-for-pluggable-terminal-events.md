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
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="9a2f1-103">Registrieren für austauschbare Terminal Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9a2f1-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="9a2f1-104">Der Ereignis Registrierungsvorgang findet statt, wenn das Terminal von einem Stream ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="9a2f1-105">In der Implementierung der [**selectterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) -Methode der Terminalanwendung können wir die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle des Terminals verwenden, das an den Stream angefügt wurde, und **QueryInterface** aufzurufen, um [**itpluggableterminaleventsink Registration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="9a2f1-106">Wenn der **QueryInterface** -Befehl erfolgreich ausgeführt wurde, können wir die [**registersink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="9a2f1-107">Zu diesem Zweck sollten Sie ein Objekt erstellen, das die [**itpluggableterminaleventsink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="9a2f1-108">Diese Schnittstelle wird als Parameter der **registersink** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="9a2f1-109">Das Terminal, das den [**itpluggableterminaleventsink Registration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) -Befehl implementiert, speichert die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="9a2f1-110">Der-Zeiger wird verwendet, wenn das Terminal ein Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="9a2f1-111">Die Registrierung der Ereignis Senke kann mithilfe von [**unregistersink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink)aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
