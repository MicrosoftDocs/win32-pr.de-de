---
title: Empfangen von Benachrichtigungen über Änderungen
description: Viele Clients können die Routing Tabelle gleichzeitig aktualisieren, und Clients müssen benachrichtigt werden, wenn Änderungen an den Routing Informationen auftreten.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacd8d1d0329cf29be82a890be30b602b9330249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388195"
---
# <a name="receiving-notification-of-changes"></a>Empfangen von Benachrichtigungen über Änderungen

Viele Clients können die Routing Tabelle gleichzeitig aktualisieren, und Clients müssen benachrichtigt werden, wenn Änderungen an den Routing Informationen auftreten. Beispielsweise könnte ein Client, der nicht über Änderungen eines anderen Clients an der Routing Tabelle benachrichtigt wird, veraltete Routeninformationen ankündigen. Dies kann verhindert werden, wenn die Programmier Clients sich beim Routing Tabellen-Manager registrieren, um über Änderungen in der Routing Tabelle benachrichtigt zu werden. Der Routing Tabellen-Manager sendet Benachrichtigungen zu Änderungen an alle Clients, die sich für den Empfang registrieren.

Die Änderungs Benachrichtigung gilt nur für Ziele. Es gibt keine Möglichkeit, den Routing Tabellen-Manager nach Änderungen an einer bestimmten Route abzufragen.

Wenn eine Änderung an einer der Routen zu einem Ziel vorgenommen wird, sendet der Routing Tabellen-Manager eine Benachrichtigung, dass eine Änderung aufgetreten ist. Diese Benachrichtigung gilt nur für die Clients, die für den Typ der aufgetretenen Änderung beim Routing Tabellen-Manager registriert wurden. Alle Änderungen an den Routing Informationen im Routing Tabellen-Manager erfolgen in mindestens einer Ansicht, und Änderungs Benachrichtigungs Meldungen können in jeder Teilmenge unterstützter Ansichten angefordert werden.

Es gibt derzeit drei Typen von Änderungs Benachrichtigungen, für die ein Client registriert werden kann:

-   Benachrichtigung über alle Änderungen an den Routen für das Ziel. Diese Anforderung wird mit dem Flag "RTM- \_ \_ Änderungstyp alle" durchgeführt \_ .
-   Benachrichtigung, wenn sich die beste Route zum Ziel ändert, oder eine der folgenden Informationen zu den aktuellen Routenänderungen:

    -   Bevorzu
    -   Nächste Hops
    -   Weiterleitungs Flags

    Diese Anforderung wird mithilfe des Kennzeichens "RTM- \_ \_ Änderungstyp" durchgeführt \_ .

-   Die Benachrichtigung über alle Änderungen des Typs RTM \_ - \_ Änderungstyp \_ ist am besten, außer Änderungen an nicht Weiterleitungs Flags in der besten Route. Der routermanager wartet z. b. auf Änderungen dieses Typs in der unicastansicht und aktualisiert die Informationen in der Unicastweiterleitung. Diese Anforderung erfolgt über das Flag für die RTM- \_ \_ Änderungstyp \_ Weiterleitung.

Anforderungen für Benachrichtigungen über Änderungen können auch auf eine Teilmenge der Ziele beschränkt werden, indem für Benachrichtigungen über Änderungen nur an markierten Zielen registriert wird. Der Client kann durch Aufrufen von [**rtmmarkdestforchangenotifiein**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)Ziel für die Änderungs Benachrichtigung markieren.

Wenn eine Änderung auftritt, prüft der Routing Tabellen-Manager, ob Clients vorhanden sind, die über diese Änderung benachrichtigt werden müssen. Ein Client muss über eine Änderung benachrichtigt werden, wenn alle der folgenden Bedingungen erfüllt sind:

-   Der Typ der aufgetretenen Änderung ist ein Typ, für den der Client eine Benachrichtigung registriert hat.
-   Änderungen an einem Ziel, das vom Client als markiert wurde, oder ein beliebiges Ziel, wenn der Client Änderungen für alle Ziele angefordert hat
-   Der Client hat eine Änderungs Benachrichtigung für die Sicht angefordert, in der die Änderung aufgetreten ist.

Wenn die Änderung alle oben aufgeführten Kriterien erfüllt, wird die Änderung zwischengespeichert, und der Client wird benachrichtigt.

In der Benachrichtigung wird nicht angegeben, was die eigentlichen Änderungen sind, sondern nur, dass Sie aufgetreten sind. Der Client muss die Änderungen abrufen, indem er mithilfe des Benachrichtigungs Handles, das bei einem vorherigen Aufruf von [**rtmregisterforchangenotifice**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)abgerufen wurde, [**rtmgetchangeddests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) aufruft.

 

 




