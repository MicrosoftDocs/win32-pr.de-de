---
title: Clientpersonation (RPC)
description: Identitätswechsel ist in einer verteilten Computingumgebung nützlich, wenn Server Clientanforderungen an andere Serverprozesse oder das Betriebssystem übergeben müssen.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022824"
---
# <a name="client-impersonation"></a>Clientidentitätswechsel

Identitätswechsel ist in einer verteilten Computingumgebung nützlich, wenn Server Clientanforderungen an andere Serverprozesse oder das Betriebssystem übergeben müssen. In diesem Fall wird von einem Server die Identität des Sicherheitskontexts des Clients angenommen. Andere Serverprozesse können die Anforderung dann so verarbeiten, als würde sie vom ursprünglichen Client gestellt.

![server imitiert die Identität eines aufrufenden Clients, wenn er nachfolgende Aufrufe im Namen des Clients sendet.](images/impr.png)

Beispielsweise sendet ein Client eine Anforderung an Server A. Wenn Server A Server B abfragen muss, um die Anforderung auszuführen, wird von Server A die Identität des Clientsicherheitskontexts angenommen und die Anforderung im Namen des Clients an Server B gesendet. Server B verwendet den Sicherheitskontext des ursprünglichen Clients anstelle der Sicherheitsidentität für Server A, um zu bestimmen, ob die Aufgabe abgeschlossen werden soll.

Der Server ruft [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, um die Sicherheit für den Serverthread mit dem Clientsicherheitskontext zu überschreiben. Nach Abschluss der Aufgabe ruft der Server [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) oder [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) auf, um den für den Serverthread definierten Sicherheitskontext wiederherzustellen.

Bei der Bindung kann der Client Quality-of-Service-Informationen zur Sicherheit angeben, die angeben, wie der Server die Identität des Clients imitieren kann. Mit einer der Einstellungen kann der Client z. B. angeben, dass der Server die Identität nicht angenommen haben darf. Weitere Informationen finden Sie unter [Quality of Service](quality-of-service.md).

Die Funktion zum Aufrufen anderer Server beim Identitätswechsel des ursprünglichen Clients wird delegierung *genannt.* Wenn die Delegierung verwendet wird, kann ein Server, der die Identität eines Clients anspricht, einen anderen Server aufrufen und Netzwerkaufrufe mit den Anmeldeinformationen des Clients ausführen. Aus Sicht des zweiten Servers sind Anforderungen, die vom ersten Server gesendet werden, nicht von Anforderungen vom Client zu unterscheiden. Nicht alle Sicherheitsanbieter unterstützen die Delegierung. Microsoft stellt nur einen Sicherheitsanbieter zur Verfügung, der die Delegierung unterstützt: Kerberos.

Die Delegierung kann aufgrund der Berechtigungen, die der Client dem Server während eines Remoteprozeduraufrufs gewährt, eine gefährliche Funktion sein. Aus diesem Grund lässt Kerberos Aufrufe mit der Identitätswechselebene der Delegierung nur zu, wenn gegenseitige Authentifizierung angefordert wird. Domänenadministratoren können die Computer einschränken, auf die Aufrufe mit Delegierungswechselebene ausgeführt werden, um zu verhindern, dass unsichere Clients Aufrufe an Server senden, die ihre Anmeldeinformationen missbrauchen könnten.

Eine Ausnahme von der Delegierungsregel besteht: Aufrufe mit [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Wenn diese Aufrufe ausgeführt werden, erhält der Server Delegierungsrechte, auch wenn eine Identitätswechselebene des Identitätswechsels angegeben ist. Das heißt, ein Server kann andere Server im Namen des Clients aufrufen. Dies funktioniert nur für einen Remoteaufruf. Wenn Client A beispielsweise den lokalen Server LB mithilfe des **lokalen ncalrpc-Servers** aufruft, kann LB die Identität des Remoteservers RB imitieren und aufrufen. RB kann im Auftrag von Client A agieren, jedoch nur auf dem Remotecomputer, auf dem RB ausgeführt wird. Ein weiterer Netzwerkaufruf an Den Remotecomputer C ist nur möglich, wenn LB beim Aufruf von RB eine Identitätswechselebene des Delegaten angegeben hat.

> [!Note]  
> Der Begriff *Identitätswechsel stellt* zwei überlappende Bedeutungen dar. Die erste Bedeutung des Identitätswechsels ist der allgemeine Prozess des Handelns im Auftrag eines Clients. Die zweite Bedeutung ist die spezifische Identitätswechselebene namens Identitätswechsel. Der Kontext des Texts verdeutlicht im Allgemeinen die Bedeutung.

 

 

 