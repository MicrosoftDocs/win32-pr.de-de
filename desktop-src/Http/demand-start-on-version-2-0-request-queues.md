---
title: Anforderungs Start in Anforderungs Warteschlangen der Version 2,0
description: .
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d618ea3fa38a856eba743d2bf60bfbfec9a633
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948753"
---
# <a name="demand-start-on-version-20-request-queues"></a>Anforderungs Start in Anforderungs Warteschlangen der Version 2,0

Mit dem Feature "Start Start" der HTTP-Server Version 2,0-API-Anforderungs Warteschlangen kann die Verarbeitung von Arbeitsprozessen durch die Controller Anwendung verzögert werden, bis die erste Anforderung in der Warteschlange eingeht. Folglich können die Anwendungen die Nutzung von Ressourcen so lange vermeiden, bis Sie benötigt werden. Weitere Informationen zur Controller Anwendung finden Sie im Thema [benannte Anforderungs Warteschlange](named-request-queue.md) .

## <a name="asynchronous-demand-start"></a>Asynchroner Bedarfs Start

Die Controller Anwendung ruft [**httpwaitfordemandstart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) mit dem Handle für die Anforderungs Warteschlange auf, um eine Start Benachrichtigung für die Anforderung zu initiieren. Für den asynchronen Abschluss stellt die Anwendung die überlappende Struktur im *poverllapp* -Parameter bereit. Wenn **httpwaitfordemandstart** asynchron aufgerufen wird, wird die Controller Anwendung benachrichtigt, wenn die erste Anforderung in der Anforderungs Warteschlange eintrifft. Nachdem die Anforderung zum Starten des Starts abgeschlossen ist, kann sich die Controller Anwendung für eine andere Anforderungs Start Benachrichtigung in der Anforderungs Warteschlange registrieren.

Die HTTP-Server-API lässt nicht mehr als eine gleichzeitige Start Benachrichtigung für eine Anforderungs Warteschlange zu. Wenn jedoch die ausstehende Start Benachrichtigung für die Anforderung abgeschlossen ist, ruft die Anwendung [**httpwaitfordemandstart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) erneut auf, um mehrere Arbeitsprozesse in der Anforderungs Warteschlange zu starten. HTTP erzwingt keine Einschränkungen hinsichtlich der Anzahl der Anforderungs Start Benachrichtigungen oder der Anzahl von Arbeitsprozessen, die in der Anforderungs Warteschlange ausgeführt werden. Die Controller Anwendungen können jedoch die Anzahl der für eine Anforderungs Warteschlange zulässigen Arbeitsprozesse erzwingen.

Die HTTP-Server-API unterstützt das Abbrechen von asynchronen [**httpwaitfordemandstart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) -aufrufen. Anwendungen können [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) mit der überlappenden Struktur verwenden, die in *poverlgetauscht* bereitgestellt wurde, um einen ausstehenden **httpwaitfordemandstart** -Befehl abzubrechen.

## <a name="synchronous-demand-start"></a>Start synchroner Anforderungen

Der Start des synchronen Bedarfs ist nicht empfehlenswert, da die Anwendung blockiert wird, bis eine Anforderung in der Anforderungs Warteschlange eintrifft.

 

 