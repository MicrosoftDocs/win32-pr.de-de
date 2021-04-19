---
description: In den folgenden Codebeispielen wird die Implementierung eines einfachen Ereignis Handlers, die Registrierung der Haupt-TAPI-Ereignis Schnittstelle, das Festlegen des Ereignis Filters und die Registrierung für-Rückruf Benachrichtigungen veranschaulicht.
ms.assetid: e7662a26-d7b2-4bff-aa72-e38b58bc15df
title: Registrieren von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0a554c2e1ea5c226aa4a3c432f3430a30a978e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364257"
---
# <a name="register-events"></a>Registrieren von Ereignissen

In den folgenden Codebeispielen wird die Implementierung eines einfachen Ereignis Handlers, die Registrierung der Haupt-TAPI-Ereignis Schnittstelle, das Festlegen des Ereignis Filters und die Registrierung für-Rückruf Benachrichtigungen veranschaulicht.

Der angezeigte Ereignishandler ist ein Beispiel und keine Anforderung. Das primäre Ziel besteht darin sicherzustellen, dass der Thread, der Ereignisse empfängt, eine minimale Verarbeitung durchführt, bevor Arbeit an einen anderen Thread übergeben wird Dadurch wird verhindert, dass der Ereignishandler in Situationen mit hoher Ereignis Auslastung zu einem Leistungsproblem wird.

Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md) ausführen und [eine Adresse auswählen](select-an-address.md).

> [!Note]  
> Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.

 

``` syntax
//
// Example 1: Implement a simple event handler.
//
HRESULT STDMETHODCALLTYPE
CTAPIEventNotification::Event(
    TAPI_EVENT  TapiEvent,
    IDispatch * pEvent
    )
{
    // AddRef the event so it does not go away.
    pEvent->AddRef();

    // Post a message to our own UI thread.
    BOOL bMessage;
    bMessage = PostMessage( 
                           ghDlg,
                           WM_PRIVATETAPIEVENT,
                           (WPARAM) TapiEvent,
                           (LPARAM) pEvent
                           );
    // If (bMessage == 0) process the error here. 
    return S_OK;
}
```

``` syntax
//
// Example 2: Register the event interface.
//
long                         gulAdvise;  // Globally declared
IConnectionPointContainer   * pCPC;
IConnectionPoint            * pCP;
IUnknown                    * pUnk;

// Get the connection point container interface pointer from the TAPI object.
hr = gpTapi->QueryInterface(
      IID_IConnectionPointContainer,
      (void **)&pCPC
);
// If ( hr != S_OK O) process the error here. 

// Get the ITTAPIEventNotification interface pointer from the container.
hr = pCPC->FindConnectionPoint(
      IID_ITTAPIEventNotification,
      &pCP
     );
// If ( hr != S_OK O) process the error here. 

pCPC->Release();

// Create a private event notification object.
CTAPIEventNotification* pTapiEventNotification = new CTAPIEventNotification;

hr = pTapiEventNotification->QueryInterface(
      IID_IUnknown,
      (void **)&pUnk
     );
// If ( hr != S_OK O) process the error here. 

// Call the advise method to give TAPI the IUnknown pointer for the event handler.
hr = pCP->Advise(
      pUnk,
      (ULONG *)&gulAdvise
     );
// If ( hr != S_OK O) process the error here. 

pCP->Release();
```

``` syntax
//
// Example 3: Set the event filter.
//
// Assume we are interested only in call-related events.
hr = gpTapi->put_EventFilter(
    TE_CALLNOTIFICATION | TE_CALLSTATE | TE_CALLMEDIA
    );
// If ( hr != S_OK O) process the error here. 
```

``` syntax
//
// Example 4: Register an address with TAPI
// for call notifications. Assume we are interested
// in video and audio calls, and that pAddress
// is a pointer to the ITAddress interface of
// an address that can handle both media types.

long glRegister; // Globally declared

hr = gpTapi->RegisterCallNotifications(
      pAddress,
      VARIANT_TRUE,   // monitor privileges
      VARIANT_TRUE,   // owner privileges
      TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
      gulAdvise,      // As returned by Advise
      &glRegister
      );
// If ( hr != S_OK O) process the error here.
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**TAPI- \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[**Ittapi::p UT- \_ Ereignis Filter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)
</dt> <dt>

[Tapimediatype- \_ Konstanten](tapimediatype--constants.md)
</dt> <dt>

[**Ittapi:: registercallbenachrichtigungen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> </dl>

 

 



