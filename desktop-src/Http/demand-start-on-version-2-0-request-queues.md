---
title: Bedarfsstart für Anforderungswarteschlangen der Version 2.0
description: Bedarfsstart für Anforderungswarteschlangen der Version 2.0
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ec5f0d2d973cfb7d4d0a3f23a5d1f6b6c6055dd9aff19521ed9ff100879c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050790"
---
# <a name="demand-start-on-version-20-request-queues"></a>Bedarfsstart für Anforderungswarteschlangen der Version 2.0

Mit der Anforderungsstartfunktion der API-Anforderungswarteschlangen für HTTP Server Version 2.0 kann die Controlleranwendung die Workerprozessinstanziierung verzögern, bis die erste Anforderung in der Anforderungswarteschlange eingeht. Daher können die Anwendungen die Ressourcen nicht verbrauchen, bis sie benötigt werden. Weitere Informationen zur Controlleranwendung finden Sie im Thema [Benannte Anforderungswarteschlange.](named-request-queue.md)

## <a name="asynchronous-demand-start"></a>Asynchroner Anforderungsstart

Die Controlleranwendung ruft [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) mit dem Handle für die Anforderungswarteschlange auf, um eine Anforderungsstartbenachrichtigung zu initiieren. Für die asynchrone Vervollständigung stellt die Anwendung die überlappende Struktur im *pOverlapped-Parameter* zur Verfügung. Wenn **HttpWaitForDemandStart** asynchron aufgerufen wird, wird die Controlleranwendung benachrichtigt, wenn die erste Anforderung in der Anforderungswarteschlange eintrifft. Nach Abschluss der Anforderungsstartbenachrichtigung kann sich die Controlleranwendung für eine andere Anforderungsstartbenachrichtigung in der Anforderungswarteschlange registrieren.

Die HTTP-Server-API lässt nicht mehr als eine gleichzeitige Anforderungsstartbenachrichtigung für eine Anforderungswarteschlange zu. Wenn jedoch die ausstehende Anforderungsstartbenachrichtigung abgeschlossen ist, ruft die Anwendung [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) erneut auf, um mehrere Workerprozesse in der Anforderungswarteschlange zu starten. HTTP erzwingt keine Einschränkungen hinsichtlich der Anzahl der Bedarfsstartbenachrichtigungen oder der Anzahl von Workerprozessen, die in der Anforderungswarteschlange arbeiten. Die Controlleranwendungen können jedoch die Anzahl von Workerprozessen erzwingen, die für eine Anforderungswarteschlange zulässig sind.

Die HTTP-Server-API unterstützt das Abbrechen asynchroner [**HttpWaitForDemandStart-Aufrufe.**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) Anwendungen können [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) mit der überlappenden Struktur verwenden, die in *pOverlapped* bereitgestellt wird, um einen ausstehenden **HttpWaitForDemandStart-Aufruf** abzubrechen.

## <a name="synchronous-demand-start"></a>Synchroner Bedarfsstart

Ein synchroner Bedarfsstart wird nicht empfohlen, da die Anwendung blockiert wird, bis eine Anforderung in der Anforderungswarteschlange eingeht.

 

 
