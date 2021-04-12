---
description: Ereignisse sind ein wesentlicher Bestandteil der Telefon Behandlung unter TAPI 3. Die Ereignis Behandlung umfasst vier Phasen.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Ereignisse (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529072"
---
# <a name="events-telephony-api"></a>Ereignisse (telefonieapi)

Ereignisse sind ein wesentlicher Bestandteil der Telefon Behandlung unter TAPI 3. Die Ereignis Behandlung umfasst vier Phasen.

**So registrieren Sie sich für und aktivieren den Empfang von Ereignissen**

1.  Implementieren Sie die [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) -Methode. (TAPI ruft diese Methode auf, wenn ein Ereignis auftritt.) Diese Implementierung übernimmt in der Regel nicht mehr als die **adressieren** des **IDispatch** -Schnittstellen Zeigers und sendet dann eine Post-Nachricht an die Meldungs Pumpe der Anwendung.
2.  Registrieren Sie die ausgehende [**ittapieventnotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) -Schnittstelle mithilfe der com-Standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle und der [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) -Schnittstelle, und übergeben Sie der [**IConnectionPoint:: Empfehlung**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) -Methode einen Zeiger auf [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Nennen Sie die " [**ittapi::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) "-Methode, um TAPI mitzuteilen, welche Ereignisse von der Anwendung behandelt werden. Der Ereignis Filter besteht aus **bzw**. Ed-Membern der [**TAPI- \_ ereignisenumeration**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > Sie müssen die Ereignis **\_ Filter-Methode ittapi::p UT** zum Festlegen der Ereignis Filtermaske und zum Aktivieren des Empfangs von Ereignissen aufruft. Wenn Sie **ittapi::p UT \_ EventFilter** nicht anrufen, empfängt Ihre Anwendung keine Ereignisse.

     

Sie müssen auch die [**ittapi:: registercallnotification**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) -Methode für jedes Adress Objekt aufrufen, für das die Anwendung Aufrufe verarbeitet.

Eine Liste aller Ereignis Schnittstellen finden Sie unter [Ereignis Schnittstellen](./event-interfaces.md) . Unter [Registrieren von Ereignissen](register-events.md) finden Sie Codebeispiele, die den Registrierungsprozess veranschaulichen und einen-Befehl für ein Codebeispiel [empfangen](receive-a-call.md) , das eine Verwendung von Ereignissen anzeigt.

 

 
