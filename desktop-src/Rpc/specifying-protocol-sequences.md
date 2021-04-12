---
title: Angeben von Protokoll Sequenzen
description: Server Anwendungen müssen mindestens eine Protokoll Sequenz auswählen, die bei der Kommunikation mit dem Client über das Netzwerk verwendet werden soll. Die Auswahl der Protokoll Sequenzen ist vom Netzwerk abhängig. Weitere Informationen finden Sie unter Interpretieren von Bindungs Informationen und Auswählen einer Protokoll Sequenz.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a700299e3d2bd98fa5fb0aaebea25e907d85afb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315891"
---
# <a name="specifying-protocol-sequences"></a>Angeben von Protokoll Sequenzen

Server Anwendungen müssen mindestens eine Protokoll Sequenz auswählen, die bei der Kommunikation mit dem Client über das Netzwerk verwendet werden soll. Die Auswahl der Protokoll Sequenzen ist vom Netzwerk abhängig. Weitere Informationen finden Sie unter [Interpretieren von Bindungs Informationen](interpreting-binding-information.md) und [Auswählen einer Protokoll Sequenz](selecting-a-protocol-sequence.md).

Mit dem Serverprogramm können Clients eine Verbindung mithilfe einer beliebigen Protokoll Sequenz herstellen, die vom Netzwerk unterstützt wird. Rufen Sie hierzu [**rpcserveruseallprottqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) auf, und übergeben Sie RPC \_ C \_ protcq \_ Max \_ reqs \_ Default als ersten Parameter. Dies ist jedoch nicht die empfohlene Vorgehensweise. Stattdessen ist die Verwendung von **Ncalrpc** für lokale Aufrufe und **ncacn \_ IP \_ TCP** oder **ncacn \_ http** für Remote Aufrufe in der Regel ausreichend. Heterogene Netzwerke sind nicht üblich, und praktisch alle Netzwerke unterstützen TCP/IP.

Wenn Sie möchten, dass der Client die Port Zuordnung für dynamische Endpunkte zu einem bestimmten Port Bereich einschränkt, müssen Sie stattdessen [**rpcserveruseallprotmenqsex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) aufrufen. Diese Funktion ist spezifisch für Microsoft RPC und ist für Remote Prozedur Aufrufe, die eine Firewall durchlaufen, äußerst nützlich. Er verwendet einen zusätzlichen Parameter, um Port Zuweisungs Steuerungs Flags an die Funktion zu übergeben. Weitere Informationen finden Sie [unter Konfigurieren der Registrierung für Port Belegungen und selektive Bindung](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

Wenn Sie die Schnittstellen des Servers entwickeln, können Sie Protokoll Sequenzen und Endpunkt Informationen in der mittleren l-Datei angeben. Wenn Sie dies tun, sollte der Server [**rpcserveruseallprotabqsif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) verwenden, um alle Protokoll Sequenzen und zugehörigen Endpunkt Informationen zu registrieren, die in der IDL-Datei bereitgestellt werden. Außerdem gibt es eine entsprechende [**rpcserveruseallprotabqsifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) -Funktion, die es dem Server ermöglicht, Port Zuordnung – steuerungflags zu übergeben.

Wenn Sie die Client-und Serverprogramme für die Kommunikation mit einer bestimmten Protokoll Sequenz konfigurieren möchten, sollte die Serveranwendung [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)anrufen. Eine komplette Liste der RPC-Protokoll Sequenzen von Microsoft finden Sie unter [Protokoll Sequenz Konstanten](protocol-sequence-constants.md).

Microsoft RPC bietet auch [**rpcserveruseprotabqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) , damit Anwendungen bestimmte Protokoll Sequenzen auswählen und die dynamische Port Zuordnung steuern können.

Zusätzlich zu Verbindungs orientierten Protokollen unterstützt Microsoft RPC auch Datagramm-Protokolle (verbindungslose Protokolle). Verbindungs orientierte Protokolle werden empfohlen. datagrammprotokolle verfügen über unterschiedliche Funktions Sätze als Verbindungs orientierte Protokolle und sollten nur verwendet werden, wenn ein verteilter Systementwickler ein Feature benötigt, das nur in Datagramm-Protokollen verfügbar ist. Bei der Verwendung von Datagramm-Protokollen sind folgende Features verfügbar:

-   Datagramme unterstützen UDP-und IPX-Transportprotokolle ohne Verbindung.
-   Da es nicht erforderlich ist, eine Verbindung einzurichten und zu verwalten, erfordert das Datagramm-RPC-Protokoll weniger Ressourcen Mehraufwand.
-   Datagramme ermöglichen eine schnellere Bindung.
-   Wie bei Verbindungs orientiertem RPC sind Datagramm-RPC-Aufrufe standardmäßig *nonidempotent*. Dies bedeutet, dass der-Rückruf garantiert nicht mehr als einmal ausgeführt wird. Eine Funktion kann jedoch in der IDL-Datei als idempotent gekennzeichnet werden, um RPC zu informieren, dass die Funktion nicht mehr als einmal als Antwort auf eine einzelne Client Anforderung ausgeführt werden kann. Auf diese Weise kann die Laufzeit weniger Status auf dem Server beibehalten. Beachten Sie, dass ein idempotenter Aufruf nur in seltenen Fällen in einem instabilen Netzwerk erneut ausgeführt werden würde.
-   Datagramm-RPC unterstützt das [Broadcast](/windows/desktop/Midl/broadcast) -IDL-Attribut. Mithilfe von Broadcast kann ein Client Nachrichten gleichzeitig an mehrere Server ausgeben. Dadurch kann der Client einen von mehreren verfügbaren Servern im Netzwerk finden oder mehrere Server gleichzeitig steuern. Beachten Sie, dass der Datagramm-Broadcast nur innerhalb des lokalen Links gültig ist und in der Regel nicht Kreuz Router ist. Broadcast Aufrufe sind implizit idempotent. Wenn der-Befehl \[ **out** - \] Parameter enthält, wird nur die erste Serverantwort zurückgegeben. Sobald ein Server antwortet, werden alle zukünftigen RPCs über diesem Bindungs Handle nur an diesen Server gesendet, einschließlich der Aufrufe mit dem Broadcast-Attribut. Um eine andere Broadcast-Übertragung zu senden, erstellen Sie ein neues Bindungs handle, oder rufen Sie [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) für das vorhandene Handle auf.
-   Datagramm RPC unterstützt das [vielleicht](/windows/desktop/Midl/maybe) IDL-Attribut. Dies ermöglicht es dem Client, einen Server Server zu senden, ohne auf eine Antwort oder Bestätigung zu warten. Der-Befehl darf keine \[ **out** - \] Parameter enthalten. Aufrufe, die die **\[ vielleicht \]** aufrufen, sind implizit idempotent.

 

 