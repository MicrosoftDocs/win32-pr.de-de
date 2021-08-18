---
title: Angeben von Protokollsequenzen
description: Serveranwendungen müssen eine oder mehrere Protokollsequenzen auswählen, die bei der Kommunikation mit dem Client über das Netzwerk verwendet werden sollen. Die Auswahl der Protokollsequenzen ist netzwerkabhängig. Weitere Informationen finden Sie unter Interpretieren von Bindungsinformationen und Auswählen einer Protokollsequenz.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f43b8dc7b21fc2a6bebe98010b80dbf369ac96bb185cc75afa3b0a4f1acbba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925150"
---
# <a name="specifying-protocol-sequences"></a>Angeben von Protokollsequenzen

Serveranwendungen müssen eine oder mehrere Protokollsequenzen auswählen, die bei der Kommunikation mit dem Client über das Netzwerk verwendet werden sollen. Die Auswahl der Protokollsequenzen ist netzwerkabhängig. Weitere Informationen finden Sie unter [Interpretieren von Bindungsinformationen](interpreting-binding-information.md) und [Auswählen einer Protokollsequenz.](selecting-a-protocol-sequence.md)

Ihr Serverprogramm ermöglicht Clients möglicherweise das Herstellen einer Verbindung mithilfe einer beliebigen Protokollsequenz, die vom Netzwerk unterstützt wird. Rufen Sie hierzu [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) auf, und übergeben Sie RPC \_ C \_ PROTSEQ \_ MAX \_ REQS DEFAULT als ersten \_ Parameter. Dies ist jedoch nicht der empfohlene Ansatz. Stattdessen ist die Verwendung von **ncalrpc** für lokale Aufrufe und **ncacn \_ ip \_ tcp** oder **ncacn \_ http** für Remoteaufrufe in der Regel ausreichend. Heterogene Netzwerke sind ungewöhnlich, und praktisch alle Netzwerke unterstützen TCP/IP.

Wenn Ihr Client die Portzuordnung für dynamische Endpunkte auf einen bestimmten Portbereich beschränken soll, rufen Sie stattdessen [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) auf. Diese Funktion ist spezifisch für Microsoft RPC und äußerst nützlich für Remoteprozeduraufrufe, die eine Firewall passieren. Er verwendet einen zusätzlichen Parameter, um Portzuordnungssteuerungsflags an die Funktion zu übergeben. Weitere Informationen finden Sie unter [Konfigurieren der Registrierung für Portzuordnungen und selektive Bindung.](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md)

Sie können Protokollsequenzen und Endpunktinformationen in Ihrer MIDL-Datei angeben, wenn Sie die Schnittstellen des Servers entwickeln. Wenn Sie dies tun, sollte Ihr Server [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) verwenden, um alle Protokollsequenzen und zugehörigen Endpunktinformationen zu registrieren, die in der IDL-Datei bereitgestellt werden. Darüber hinaus gibt es eine entsprechende [**RpcServerUseAllProtseqsIfEx-Funktion,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) mit der der Server auch Portzuordnungs-Steuerungsflags übergeben kann.

Wenn Sie Ihre Client- und Serverprogramme für die Kommunikation mit einer angegebenen Protokollsequenz konfigurieren möchten, sollte die Serveranwendung [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)aufrufen. Eine vollständige Liste der Microsoft RPC-Protokollsequenzen finden Sie unter [Protokollsequenzkonstanten.](protocol-sequence-constants.md)

Microsoft RPC stellt außerdem [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) bereit, damit Anwendungen bestimmte Protokollsequenzen auswählen und die dynamische Portzuordnung steuern können.

Zusätzlich zu verbindungsorientierten Protokollen unterstützt Microsoft RPC auch Datagrammprotokolle (verbindungslos). Verbindungsorientierte Protokolle werden empfohlen. Datagrammprotokolle verfügen über andere Featuresätze als verbindungsorientierte Protokolle und sollten nur verwendet werden, wenn ein Entwickler eines verteilten Systems ein Feature benötigt, das nur in Datagrammprotokollen verfügbar ist. Folgende Features sind verfügbar, wenn Datagrammprotokolle verwendet werden:

-   Datagramme unterstützen die verbindungslosen UDP- und IPX-Transportprotokolle.
-   Da es nicht erforderlich ist, eine Verbindung herzustellen und zu verwalten, erfordert das RPC-Protokoll des Datagramms weniger Ressourcenaufwand.
-   Datagramme ermöglichen eine schnellere Bindung.
-   Wie beim verbindungsorientierten RPC sind Datagramm-RPC-Aufrufe standardmäßig *nichtidempotent.* Dies bedeutet, dass der Aufruf garantiert nicht mehr als einmal ausgeführt wird. Eine Funktion kann jedoch in der IDL-Datei als idempotent markiert werden, um RPC mitzuteilen, dass es unschädlich ist, die Funktion als Reaktion auf eine einzelne Clientanforderung mehr als einmal auszuführen. Dies ermöglicht es der Laufzeit, einen geringeren Zustand auf dem Server beizubehalten. Beachten Sie, dass ein idempotenter Aufruf nur in seltenen Fällen in einem instabilen Netzwerk erneut ausgeführt wird.
-   Datagram RPC [](/windows/desktop/Midl/broadcast) unterstützt das Broadcast-IDL-Attribut. Broadcast ermöglicht es einem Client, Nachrichten gleichzeitig an mehrere Server auszugeben. Dadurch kann der Client einen von mehreren verfügbaren Servern im Netzwerk suchen oder mehrere Server gleichzeitig steuern. Beachten Sie, dass die Datagrammübertragung nur innerhalb des lokalen Links gültig ist und in der Regel keine Router kreuzt. Broadcastaufrufe sind implizit idempotent. Wenn der Aufruf \[  \] Out-Parameter enthält, wird nur die erste Serverantwort zurückgegeben. Sobald ein Server antwortet, werden alle zukünftigen RPCs über dieses Bindungshandle nur an diesen Server gesendet, einschließlich Aufrufe mit dem Broadcastattribut. Um eine weitere Übertragung zu senden, erstellen Sie ein neues Bindungshandle, oder rufen [**Sie RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) für das vorhandene Handle auf.
-   Datagram RPC unterstützt das [maybe](/windows/desktop/Midl/maybe) IDL-Attribut. Dadurch kann der Client einen Aufruf an den Server senden, ohne auf eine Antwort oder Bestätigung zu warten. Der Aufruf darf keine \[ **out-Parameter** \] enthalten. Aufrufe, die die **\[ \] maybe-Aufrufe** verwenden, sind implizit idempotent.

 

 