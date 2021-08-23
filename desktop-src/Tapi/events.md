---
description: Ereignisse sind ein entscheidender Bestandteil der Anrufverarbeitung unter TAPI 3. Die Ereignisbehandlung umfasst vier Phasen.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Ereignisse (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b2cf181f10373505a0fe50d3c9efa7358b3ccb749acb723d8314dee27ff9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660860"
---
# <a name="events-telephony-api"></a>Ereignisse (Telefonie-API)

Ereignisse sind ein entscheidender Bestandteil der Anrufverarbeitung unter TAPI 3. Die Ereignisbehandlung umfasst vier Phasen.

**So registrieren Sie sich für den Empfang von Ereignissen und aktivieren diesen.**

1.  Implementieren Sie die [**ITTAPIEventNotification::Event-Methode.**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) (TAPI ruft diese Methode auf, wenn ein Ereignis auftritt.) In der Regel führt diese Implementierung nicht mehr als **AddRef** für den **IDispatch-Schnittstellenzeiger** aus und postt dann an die Nachrichtenpump der Anwendung.
2.  Registrieren Sie die ausgehende [**ITTAPIEventNotification-Schnittstelle**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) mithilfe der COM-Standardschnittstellen [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) und [**IConnectionPoint,**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) und übergeben Sie der [**IConnectionPoint::Advise-Methode**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) einen Zeiger auf [**ITTAPIEventNotification::Event.**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
3.  Rufen Sie die [**ITTAPI::p ut \_ EventFilter-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) auf, um TAPI mitzuteilen, welche Ereignisse von der Anwendung behandelt werden. Der Ereignisfilter besteht aus OR-ed-Membern der [**TAPI \_ EVENT-Enumeration.**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
    > [!Note]  
    > Sie müssen die **\_ EventFilter-Methode ITTAPI::p ut** aufrufen, um die Ereignisfiltermaske festzulegen und den Empfang von Ereignissen zu aktivieren. Wenn Sie **ITTAPI::p ut \_ EventFilter** nicht aufrufen, empfängt Ihre Anwendung keine Ereignisse.

     

Sie müssen auch die [**ITTAPI::RegisterCallNotifications-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) für jedes Adressobjekt aufrufen, für das die Anwendung Aufrufe verarbeitet.

Eine [](./event-interfaces.md) Liste aller Ereignisschnittstellen finden Sie unter Ereignisschnittstellen. Codebeispiele zur Veranschaulichung des Registrierungsprozesses und [Zum Empfangen eines Aufrufs](receive-a-call.md) finden Sie unter Registrieren von [Ereignissen](register-events.md) für ein Codebeispiel, das eine Verwendung von Ereignissen zeigt.

 

 
