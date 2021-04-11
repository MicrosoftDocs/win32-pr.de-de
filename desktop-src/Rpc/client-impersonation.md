---
title: Client Identitätswechsel (RPC)
description: Der Identitätswechsel ist in einer verteilten Computerumgebung hilfreich, wenn Server Client Anforderungen an andere Server Prozesse oder an das Betriebssystem übergeben müssen.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03ad3b4d9e2984708e8b274ab9bc57c3235808b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102126"
---
# <a name="client-impersonation"></a>Clientidentitätswechsel

Der Identitätswechsel ist in einer verteilten Computerumgebung hilfreich, wenn Server Client Anforderungen an andere Server Prozesse oder an das Betriebssystem übergeben müssen. In diesem Fall nimmt ein Server einen Identitätswechsel für den Sicherheitskontext des Clients vor. Andere Server Prozesse können dann die Anforderung so verarbeiten, als ob Sie vom ursprünglichen Client erstellt wurde.

![der Server nimmt die Identität eines aufrufenden Clients an, wenn er im Auftrag des Clients nachfolgende Aufrufe ausführt.](images/impr.png)

Beispielsweise sendet ein Client eine Anforderung an Server a. Wenn Server a Server b Abfragen muss, um die Anforderung abzuschließen, nimmt Server a die Identität des Client Sicherheits Kontexts an und sendet die Anforderung an Server b im Auftrag des Clients. Server B verwendet den Sicherheitskontext des ursprünglichen Clients anstelle der Sicherheitsidentität für Server A, um zu bestimmen, ob die Aufgabe ausgeführt werden soll.

Der Server ruft [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) auf, um die Sicherheit für den Server Thread mit dem Client Sicherheitskontext zu überschreiben. Nachdem die Aufgabe abgeschlossen ist, ruft der Server [**rpkrevertstoself**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) oder [**rpkrevertstarselfex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) auf, um den für den Server Thread definierten Sicherheitskontext wiederherzustellen.

Bei der Bindung kann der Client Quality of Service-Informationen zur Sicherheit angeben, die angibt, wie der Server die Identität des Clients annehmen kann. Beispielsweise kann der Client mit einer der-Einstellungen angeben, dass der Server die Identität des Servers nicht annehmen darf. Weitere Informationen finden Sie unter [Quality of Service](quality-of-service.md).

Die Funktion, andere Server beim Annehmen der Identität des ursprünglichen Clients aufzurufen, wird als *Delegierung* bezeichnet. Bei Verwendung der Delegierung kann ein Server, der die Identität eines Clients annimmt, einen anderen Server aufrufen und Netzwerk Aufrufe mit den Anmelde Informationen des Clients durchführen. Das heißt aus der Perspektive des zweiten Servers, dass Anforderungen vom ersten Server nicht von den Anforderungen des Clients unterschieden werden können. Die Delegierung wird nicht von allen Sicherheitsanbietern unterstützt. Microsoft umfasst nur einen Sicherheitsanbieter, der die Delegierung unterstützt: Kerberos.

Die Delegierung kann aufgrund der Berechtigungen, die der Client während eines Remote Prozedur Aufrufes dem Server erteilt, eine gefährliche Möglichkeit darstellen. Der Grund hierfür ist, dass Kerberos Aufrufe mit der Identitätswechsel Ebene nur dann zulässt, wenn eine gegenseitige Authentifizierung angefordert wird. Domänen Administratoren können die Computer einschränken, auf die Aufrufe mit Delegierungs Identitätswechsel Ebene vorgenommen werden, um zu verhindern, dass ahnungslose Clients Aufrufe an Server durchführen, die ihre Anmelde Informationen missbrauchen.

Eine Ausnahme von der Delegierungs Regel besteht: Aufrufe mit [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Wenn diese Aufrufe durchgeführt werden, erhält der Server Delegierungs Rechte, auch wenn eine Identitätswechsel Ebene mit Identitätswechsel angegeben wird. Das heißt, ein Server kann andere Server im Namen des Clients anrufen. Dies funktioniert nur für einen Remote-Rückruf. Wenn der Client A z. b. den lokalen Server-lb mithilfe des lokalen **Ncalrpc** -Servers aufruft, kann er einen Identitätswechsel durchgeführt und Remote Server RB aufrufen RB kann im Auftrag von Client A agieren, aber nur auf dem Remote Computer, auf dem RB ausgeführt wird. Es kann keinen weiteren Netzwerk Aufruf an den Remote Computer C ausführen, es sei denn, der Lastenausgleich hat beim Aufruf von RB eine Identitätswechsel Ebene angegeben.

> [!Note]  
> Der Begriff *Identitäts* Wechsel stellt zwei überlappende Bedeutungen dar. Die erste Bedeutung des Identitäts Wechsels ist der allgemeine Prozess der Durchsetzung von im Auftrag eines Clients. Die zweite Bedeutung ist die spezifische Identitätswechsel Ebene, die als Identitätswechsel bezeichnet wird. Im allgemeinen verdeutlicht der Kontext des Texts die Bedeutung.

 

 

 