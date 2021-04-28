---
title: Bedarfsstart für Anforderungswarteschlangen der Version 2.0
description: Bedarfsstart für Anforderungswarteschlangen der Version 2.0
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6b14759e60fb69a47cda6975f6559c00771f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090928"
---
# <a name="demand-start-on-version-20-request-queues"></a>Bedarfsstart für Anforderungswarteschlangen der Version 2.0

Die Anforderungsstartfunktion der API-Anforderungswarteschlangen von HTTP Server Version 2.0 ermöglicht der Controlleranwendung, die Workerprozessinstanziierung zu verzögern, bis die erste Anforderung in der Anforderungswarteschlange eingeht. Daher können die Anwendungen vermeiden, Ressourcen zu verbrauchen, bis sie erforderlich sind. Weitere Informationen zur Controlleranwendung finden Sie im Thema [Benannte Anforderungswarteschlange.](named-request-queue.md)

## <a name="asynchronous-demand-start"></a>Asynchroner Bedarfsstart

Die Controlleranwendung ruft [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) mit dem Handle für die Anforderungswarteschlange auf, um eine Anforderungsstartbenachrichtigung zu initiieren. Für die asynchrone Vervollständigung stellt die Anwendung die überlappende Struktur im *pOverlapped-Parameter* zur Verfügung. Wenn **HttpWaitForDemandStart** asynchron aufgerufen wird, wird die Controlleranwendung benachrichtigt, wenn die erste Anforderung in der Anforderungswarteschlange eingeht. Nach Abschluss der Anforderungsstartbenachrichtigung kann sich die Controlleranwendung für eine andere Anforderungsstartbenachrichtigung in der Anforderungswarteschlange registrieren.

Die HTTP-Server-API lässt nicht mehr als eine gleichzeitige Anforderungsstartbenachrichtigung für eine Anforderungswarteschlange zu. Wenn jedoch die ausstehende Anforderungsstartbenachrichtigung abgeschlossen ist, ruft die Anwendung [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) erneut auf, um mehrere Workerprozesse in der Anforderungswarteschlange zu starten. HTTP erzwingt keine Einschränkungen hinsichtlich der Anzahl von Anforderungsstartbenachrichtigungen oder der Anzahl von Workerprozessen, die in der Anforderungswarteschlange arbeiten. Die Controlleranwendungen können jedoch die Anzahl von Workerprozessen erzwingen, die für eine Anforderungswarteschlange zulässig sind.

Die HTTP-Server-API unterstützt das Abbrechen asynchroner [**HttpWaitForDemandStart-Aufrufe.**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) Anwendungen können [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) mit der überlappenden Struktur verwenden, die in *pOverlapped* bereitgestellt wird, um einen ausstehenden **HttpWaitForDemandStart-Aufruf** abzubrechen.

## <a name="synchronous-demand-start"></a>Synchroner Bedarfsstart

Der synchrone Bedarfsstart wird nicht empfohlen, da die Anwendung blockiert wird, bis eine Anforderung in der Anforderungswarteschlange eintrifft.

 

 
