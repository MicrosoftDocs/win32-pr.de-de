---
title: Ereignisse
description: Ein gehosteter Dienst muss die iupnpeer-Source-Schnittstelle implementieren, wenn er Zustandsvariablen aussteht.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a6382ee88d2ca5168c94eac20727bbfee4a598
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856271"
---
# <a name="eventing"></a>Ereignisse

Ein gehosteter Dienst muss die [**iupnpeer-Source**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) -Schnittstelle implementieren, wenn er Zustandsvariablen aussteht. Diese Schnittstelle verfügt über zwei Methoden: [**Rat**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) und [**nicht Empfehlung**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Diese Schnittstelle bietet einen Mechanismus für den Geräte Host zum Abonnieren von Ereignis Benachrichtigungen, die vom gehosteten Dienst generiert werden. Es werden nicht mehr als eine Ereignis Senke gleichzeitig registriert.

Ein gehosteter Dienst muss die Methode " [**Empfehlung**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) " implementieren, indem er einen Verweis auf die [**iupnetventsink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) -Schnittstelle enthält, die als Parameter übergeben wurde. Wenn die-Schnittstelle gefunden wird, enthält die-Methode " **Empfehlung** " einen Verweis auf diese Schnittstelle, bis " [**Unrat**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) " aufgerufen wird, oder bis das gehostete Dienst Objekt entfernt wird. Die **Empfehlung** wird nur einmal aufgerufen.

Um das Abonnement zu entfernen, ruft der Geräte Host [**nicht Empfehlung**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) auf und übergibt den Objekt Zeiger, der beim Aufrufen von " [**Empfehlung**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)" verwendet wurde. Der gehostete Dienst entfernt das Abonnement, wenn der Zeiger mit dem übereinstimmt, der an die **Empfehlung** übermittelt wurde.

Wenn sich der Wert einer Zustandsvariablen ändert, muss der gehostete Dienst signalisieren, dass ein Ereignis aufgetreten ist. Dies erfolgt durch Aufrufen der [**iupnpeer ventsink:: OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) -Methode.

Wenn der Geräte Host keine Benachrichtigungen mehr vom gehosteten Dienst empfangen muss, ruft er [**iupnpeer-Source:: Unrat**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise)auf und übergibt denselben Objekt Zeiger, den er von der [**Empfehlung**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise)erhalten hat. Der Geräte Host ruft diese Methode auf, wenn sich das Gerät nicht mehr im Netzwerk befindet.

 

 




