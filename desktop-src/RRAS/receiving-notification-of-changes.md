---
title: Empfangen von Benachrichtigungen über Änderungen
description: Viele Clients können die Routingtabelle gleichzeitig aktualisieren, und Clients müssen benachrichtigt werden, wenn Änderungen an Routinginformationen auftreten.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788710"
---
# <a name="receiving-notification-of-changes"></a>Empfangen von Benachrichtigungen über Änderungen

Viele Clients können die Routingtabelle gleichzeitig aktualisieren, und Clients müssen benachrichtigt werden, wenn Änderungen an Routinginformationen auftreten. Beispielsweise kann ein Client, der nicht über die Änderungen eines anderen Clients an der Routingtabelle benachrichtigt wird, veraltete Routeninformationen ankündigen. Dies kann verhindert werden, indem Clients so programmiert werden, dass sie sich beim Routingtabellen-Manager registrieren, um über Änderungen in der Routingtabelle benachrichtigt zu werden. Der Routingtabellen-Manager sendet Benachrichtigungen über Änderungen an alle Clients, die sich registrieren, um sie zu empfangen.

Die Änderungsbenachrichtigung gilt nur für Ziele. Es gibt keine Möglichkeit, den Routingtabellen-Manager nach Änderungen an einer bestimmten Route abzufragen.

Wenn eine Änderung an einer der Routen zu einem Ziel vorgenommen wird, sendet der Routingtabellen-Manager eine Benachrichtigung, dass eine Änderung aufgetreten ist. Diese Benachrichtigung wird nur an die Clients weitergeleitet, die sich beim Routingtabellen-Manager für den Typ der aufgetretenen Änderung registriert haben. Alle Änderungen an Routinginformationen im Routingtabellen-Manager erfolgen in einer oder mehreren Ansichten, und Änderungsbenachrichtigungsmeldungen können in jeder Teilmenge der unterstützten Sichten angefordert werden.

Derzeit gibt es drei Arten von Änderungsbenachrichtigungen, für die sich ein Client registrieren kann:

-   Benachrichtigung über änderungen an den Routen für das Ziel. Diese Anforderung wird mithilfe des \_ RTM CHANGE \_ TYPE \_ ALL-Flags ausgeführt.
-   Benachrichtigung, wenn sich die beste Route zum Ziel ändert, oder eine der folgenden Informationen für die aktuellen Änderungen der besten Route:

    -   Einstellung
    -   Nächste Hops
    -   Routenflags

    Diese Anforderung wird mit dem RTM \_ CHANGE \_ TYPE \_ BEST-Flag ausgeführt.

-   Benachrichtigung über alle Änderungen des Typs RTM CHANGE TYPE BEST, mit Ausnahme von \_ Änderungen an \_ \_ Flags ohne Weiterleitung in der besten Route. Beispielsweise wartet der Router-Manager auf Änderungen dieses Typs in der Unicastansicht und aktualisiert Informationen in der Unicast-Weiterleitung. Diese Anforderung wird mithilfe des \_ RTM CHANGE \_ TYPE \_ FORWARDING-Flags ausgeführt.

Anforderungen für Benachrichtigungen über Änderungen können auch auf eine Teilmenge von Zielen beschränkt werden, indem nur für Benachrichtigungen von Änderungen an "markierte" Ziele registriert wird. Der Client kann ein Ziel für Änderungsbenachrichtigungen markieren, indem [**er RtmMarkDestForChangeNotification aufruft.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

Wenn eine Änderung auftritt, überprüft der Routingtabellen-Manager, ob Clients vorhanden sind, die über diese Änderung benachrichtigt werden müssen. Ein Client muss über eine Änderung benachrichtigt werden, wenn alle der folgenden Bedingungen erfüllt sind:

-   Der Typ der aufgetretenen Änderung ist ein Typ, für den sich der Client für Benachrichtigungen registriert hat.
-   Änderungen an einem ziel, das der Client als markiert hat, sind aufgetreten, oder ein beliebiges Ziel, wenn der Client Änderungen für alle Ziele angefordert hat
-   Der Client hat eine Änderungsbenachrichtigung für die Ansicht angefordert, in der diese Änderung aufgetreten ist.

Wenn die Änderung alle oben genannten Kriterien erfüllt, wird die Änderung zwischengespeichert, und der Client wird benachrichtigt.

Die Benachrichtigung gibt nicht an, was die tatsächlichen Änderungen sind, sondern nur, dass sie aufgetreten sind. Der Client muss die Änderungen abrufen, indem [**er RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) mithilfe des Benachrichtigungshandle aufruft, das aus einem vorherigen Aufruf von [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)abgerufen wurde.

 

 




