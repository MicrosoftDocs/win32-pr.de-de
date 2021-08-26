---
title: Ereignisse
description: Ein gehosteter Dienst muss die IUPnPEventSource-Schnittstelle implementieren, wenn er über Ereigniszustandsvariablen verfügt.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008080"
---
# <a name="eventing"></a>Ereignisse

Ein gehosteter Dienst muss die [**IUPnPEventSource-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) implementieren, wenn er über Ereigniszustandsvariablen verfügt. Diese Schnittstelle verfügt über zwei Methoden: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) und [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Diese Schnittstelle stellt einen Mechanismus bereit, mit dem der Gerätehost Ereignisbenachrichtigungen abonnieren kann, die vom gehosteten Dienst generiert werden. Es werden nicht mehr als eine Ereignissenke gleichzeitig registriert.

Ein gehosteter Dienst muss die [**Advise-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) implementieren, indem er einen Verweis auf die [**IUPnPEventSink-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) hält, die als Parameter übergeben wurde. Wenn die Schnittstelle gefunden wird, enthält die **Advise-Methode** einen Verweis auf diese Schnittstelle, bis [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) aufgerufen oder das gehostete Dienstobjekt entfernt wird. **Advise** wird nur einmal aufgerufen.

Um das Abonnement zu entfernen, ruft der Gerätehost [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) auf und übergibt den Objektzeiger, der beim Aufruf von [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)verwendet wurde. Der gehostete Dienst entfernt das Abonnement, wenn der Zeiger mit dem an **Advise** übergebenen Zeiger identisch ist.

Wenn sich der Wert einer Zustandsvariablen ändert, muss der gehostete Dienst signalisieren, dass ein Ereignis aufgetreten ist. Die Dienste verwenden dazu die [**IUPnPEventSink::OnStateChanged-Methode.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged)

Wenn der Gerätehost keine Benachrichtigungen mehr vom gehosteten Dienst empfangen muss, ruft er [**IUPnPEventSource::Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise)auf und übergibt denselben Objektzeiger, den er von [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)erhalten hat. Der Gerätehost ruft diese Methode auf, wenn sich das Gerät nicht mehr im Netzwerk befindet.

 

 




