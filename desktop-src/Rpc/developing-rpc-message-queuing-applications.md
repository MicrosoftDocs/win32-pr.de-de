---
title: Entwickeln von RPC-Message Queuinganwendungen
description: Es ist nur sehr wenig Aufwand erforderlich, um den MSMQ-Transport in der RPC-Anwendung zu nutzen.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- Remote Prozedur Aufruf RPC, Tasks, entwickeln von Message Queuinganwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e51707c0a6903200e51dd35e50e998430c8eae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039496"
---
# <a name="developing-rpc-message-queuing-applications"></a>Entwickeln von RPC-Message Queuinganwendungen

Es ist nur sehr wenig Aufwand erforderlich, um den MSMQ-Transport in der RPC-Anwendung zu nutzen. Für synchrones Messaging müssen Sie nur den Nachrichten Warteschlangen Transport ([**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq)) als Protokoll Sequenz angeben. Das **ncadg \_ MQ** -Protokoll unterstützt alle standardmäßigen Datagramm-Features mit Ausnahme von Broadcast aufrufen. Beachten Sie außerdem, dass der Nachrichten Warteschlangen-Transport derzeit keine dynamischen Endpunkte unterstützt.

Wenn Sie das \[ [**Message**](/windows/desktop/Midl/message) - \] Attribut auf Remote Prozedur Deklarationen in der IDL-Datei anwenden, implementieren Sie Message Queueing für diese Aufrufe automatisch im asynchronen Modus. Dies ermöglicht es den Client-und Server Anwendungen, viele der Eigenschaften zu steuern, die mit Nachrichten und Nachrichten Warteschlangen verknüpft sind. dazu gehören:

-   Quality of Service
-   Bestätigung der Bestätigung
-   Journaling
-   Rückruf Priorität
-   Persistenz der Server Prozess Warteschlange

Quality of Service ist der Aufwand, den der Transport durchführt, um den Server Prozess aufzurufen. Eine Express-Übermittlung wird im Arbeitsspeicher in die Warteschlange eingereiht, sodass Sie recht schnell ist, aber der Aufruf geht verloren, wenn eine Computer-oder Netzwerkverbindung zum falschen Zeitpunkt ausfällt. Eine wiederherstellbare Übermittlung wird an eine Datenträger Datei gesendet, bis Sie übermittelt wird, sodass der Aufruf nicht verloren geht, selbst bei einem Computerabsturz. Dadurch erhalten Sie eine garantierte Bereitstellung, Kosten in der Leistung, während die einzelnen Aufrufe auf den Datenträger geschrieben werden.

Sie können auch den MSMQ-Transport anweisen, auf die Bestätigung zu warten, dass der-Befehl die Ziel Warteschlange (Server) vor der Rückgabe erreicht hat. Wenn Sie diese Option auswählen, wird der Client so lange blockiert, bis der Server den-Befehl bestätigt; andernfalls wird die Steuerung sofort an den Client zurückgegeben.

Durch die Verwendung von Journalen können Aufrufe auf dem Datenträger protokolliert werden. Wenn Journal Vorgänge aktiviert ist, wird jeder-Vorgang auf dem Datenträger protokolliert, da er an den nächsten Hop auf seine Weise an den Server Prozess übertragen wird.

Die Aufruf Priorität kann in Verbindung mit dem RPC- \[ [**Nachrichten**](/windows/desktop/Midl/message) \] Funktions Attribut verwendet werden, um Aufrufe mit höherer Priorität zu ermöglichen, die Vorrang vor Aufrufen mit niedrigerer Priorität haben, selbst wenn die Aufrufe mit hoher Priorität später eingehen. Die Aufruf Priorität funktioniert auch in begrenztem Umfang mit synchronem RPC, aber synchrone RPC-Aufrufe können nicht auf die gleiche Weise wie asynchrone Aufrufe gestapelt werden.

Der Client Prozess steuert alle oben genannten Eigenschaften durch Aufrufen von [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Nach der Festlegung bleiben diese Eigenschaften wirksam, bis Sie in einem anderen Aufrufen von **rpcbindingsetoption** geändert werden.

Der RPC-Server Prozess kann die Lebensdauer der Empfangs Warteschlange steuern. Standardmäßig wird die Warteschlange gelöscht, wenn der Server Prozess beendet wird. Der Server Prozess kann jedoch beim Einrichten des Endpunkts [**rpcserveruseprotonqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) verwenden, um dem Transport mitzuteilen, dass die Warteschlange weiterhin vorhanden sein kann, und auch dann, wenn der Server Prozess nicht ausgeführt wird, auch wenn der Server Prozess nicht ausgeführt wird. In diesem Fall werden die Aufrufe später in die Warteschlange eingereiht und ausgeführt, wenn der Server Prozess wieder online geschaltet wird.

> [!Note]  
> Wenn Sie asynchrone \[ [**Nachrichten**](/windows/desktop/Midl/message) \] Aufrufe in einer Schnittstelle verwenden, müssen Sie die Schnittstelle registrieren, indem Sie [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) oder [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) aufrufen, bevor Sie [**rpcserveruseprotsetqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ mq)** aufrufen. Wenn Sie die Protokoll Sequenz aktivieren, werden alle Aufrufe, die bereits auf die Warteschlange für den Server warten, von der Warteschlange gelesen. Wenn die entsprechende RPC-Schnittstelle nicht registriert wurde, können die Aufrufe nicht ausgeführt werden. Diese Situation kann eintreten, wenn Sie einen permanenten Endpunkt für Remote Prozedur Aufrufe eingerichtet haben, der Server heruntergefahren wurde und Clients weiterhin Aufrufe an den Server senden. Diese Aufrufe werden in der Warteschlange gestapelt und warten darauf, gelesen zu werden, sobald der Server wieder online ist.

 

Weitere Informationen finden Sie unter [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**rpcserveruseprotseqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)und \[ [**Message**](/windows/desktop/Midl/message) \] , [**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq).

 

 