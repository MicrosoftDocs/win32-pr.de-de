---
title: Verhindern von clientseitigen Hängen
description: Es gibt zwei Möglichkeiten, wie Ihr Client die Netzwerkkonnektivität hängen lässt, die dazu führen kann, dass Serveranforderungen verloren gehen, oder der Server selbst stürzt ab. Bei Standardoptionen tritt für RPC nie ein Time out auf, und Ihr Clientthread wartet für immer auf eine Antwort.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- Remoteprozeduraufruf RPC , bewährte Methoden, verhindern, dass der Client hängt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da79573e59e30c58a7c236b35293b678c93dde6bf999b477de054d6f3c62971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927295"
---
# <a name="preventing-client-side-hangs"></a>Verhindern von clientseitigen Hängen

Es gibt zwei Möglichkeiten, wie Ihr Client hängen bleibt: Die Netzwerkkonnektivität kann dazu führen, dass Serveranforderungen verloren gehen, oder der Server selbst kann abstürzt. Bei Standardoptionen tritt für RPC nie ein Time out auf, und Ihr Clientthread wartet für immer auf eine Antwort.

Es gibt zwei Methoden, um dies zu verhindern: Keep Alives und Time outs.

## <a name="tcp-keep-alives"></a>TCP Keep Alives

Der Client kann so eingerichtet werden, dass er den Server regelmäßig pingt, um sicherzustellen, dass der Server aktiv ist und ausgeführt wird. Die Pings sind TCP-Keep-Alives für die [**ncacn \_ ip \_ tcp-**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn-HTTP-Protokollsequenzen. \_**](/windows/desktop/Midl/ncacn-http) Daher sind sie bei der CPU-Auslastung und Netzwerkbandbreite effizient. Um Keep Alives für einen bestimmten Remoteprozeduraufruf zu aktivieren, verwenden Sie die [**RpcMgmtSetComTimeout-Funktion,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) bevor der Aufruf initiiert wird. Diese Funktion verwendet ein Bindungshandle und ein Time out als Argumente. Jeder Remoteprozeduraufruf für dieses Bindungshandle, nachdem **RpcMgmtSetComTimeout** das angegebene Timeout verwendet hat.

Der Timeout-Parameter für die [**RpcMgmtSetComTimeout-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) gibt an, wie lange die RPC-Laufzeit wartet, bevor keep alive aktiviert wird. Das Time out ist ein Wert zwischen 0 und 10, wobei 0 das minimale Time out und 10 ein unendliches Time out (kein Time out) ist. Das Time out selbst liegt nicht in Sekunden. Die Übersetzung des Timeoutwerts, der für die **RpcMgmtSetComTimeout-Funktion** bereitgestellt wird, in Sekunden erfolgt durch die RPC-Laufzeit und ist implementierungsspezifisch.

Die folgende Tabelle enthält die Übersetzung in Sekunden für Windows 2000 und Windows XP. Zukünftige Versionen von Windows können die Zuordnung zwischen dem Timeoutparameter und dem Timeoutwert in Sekunden ändern:

| Timeoutparameter                       | Tatsächliches Time out in Sekunden |
|-----------------------------------------|----------------------------|
| 0 (RPC \_ C \_ BINDING MIN \_ \_ TIMEOUT)       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (RPC \_ C \_ BINDING DEFAULT \_ \_ TIMEOUT)   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 \_ (RPC C \_ BINDING MAX \_ \_ TIMEOUT)       | 1200                       |
| 10 \_ (RPC C \_ BINDING INFINITE \_ \_ TIMEOUT) | Unendliches Time out          |



 

Sobald die Keep Alives aktiviert sind, sendet der Client jede Sekunde ein Keep-Alive-Paket. Wenn vom Server keine Bestätigung für drei oder mehr Keep-Alive-Handlungen vorhanden ist, deklariert der Client die Verbindung als nicht aktiv und schlägt den Remoteprozeduraufruf fehl. Wenn der Server innerhalb des angegebenen Time outs eine Antwort sendet, werden Keep Alives nicht aktiviert. Wenn der Server auf Keep Alives antwortet, aber nicht auf den Remoteprozeduraufruf reagiert, sendet der Client weiterhin Keep-Alive-Nachrichten. Sobald der Server auf den RPC-Aufruf reagiert, werden die Keep-Alive-Funktionen deaktiviert. Für Windows 2000 sind Keep-Alive-Funktionen nur für synchrone RPC-Aufrufe aktiviert. Für Windows XP werden Keep-Alive-Vorgänge auch für asynchrone RPC-Aufrufe aktiviert.

Es ist verlockend, keep alives auf den niedrigsten Wert festzulegen, um sicherzustellen, dass die Clientanwendung rechtzeitig auf Netzwerkprobleme reagiert. Es sollte sorgfältig geprüft werden, ob ein aggressiver Wert gerechtfertigt ist, und es sollte sorgfältig geprüft werden, ob ein aggressiver Wert erforderlich ist. Ein Server, bei dem die Konnektivität vorübergehend verloren geht, wird möglicherweise von zahlreichen Clients überflutet, sobald die Konnektivität wiederhergestellt wurde. Darüber hinaus können lange Berechnungsaufgaben mehr als zwei Minuten dauern, und der Server kann mehr CPU-Zeit für die Beantwortung von Keep-Alive-Vorgängen aufwenden als für nützliche Aufgaben. Daher sollten Keep-Alive-Funktionen mit Moderation verwendet werden. Wenn der Client nicht tolerieren kann, dass sein Thread über längere Zeiträume gebunden ist, sollte ein asynchroner RPC berücksichtigt werden.

Andere Protokollsequenzen implementieren möglicherweise unterschiedliche Mechanismen zum Erkennen nicht reagierender Server, je nachdem, welcher Transport verwendet wird. Der [**ncalrpc-Transport**](/windows/desktop/Midl/ncalrpc) verwendet keine Keep Alives. Da die gesamte Kommunikation in **ncalrpc** lokal ist, schlägt die RPC-Laufzeit auf dem Client sofort fehl, wenn der Server während eines Aufrufs nicht mehr reagiert.

## <a name="call-time-outs"></a>Time outs für Aufrufe

TCP-Keep-Alives sind in Ordnung, wenn die Netzwerkkonnektivität unterbrochen wird oder der Server abstürzt. Wenn der Server jedoch im Benutzermodus deadlockt, wird TCP Keep Alive erfolgreich zurückgegeben, aber der Aufruf wird nie zurückgegeben. Für dieses Szenario wurde eine neue Laufzeitoption für Windows XP hinzugefügt: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT. Diese Option weist die RPC-Laufzeit an, bei jedem Senden einer Anforderung an den Server einen Timer einzurichten. Wenn der Timer abläuft, wird der Aufruf automatisch abgebrochen und mit RPC \_ S \_ CALL \_ CANCELLED abgeschlossen. Solange der Server innerhalb des angegebenen Zeitlimits antwortet, wird der Aufruf vom Client nicht abgebrochen. Dies bedeutet, dass ein Multifragmentaufruf mehr als die Zeit bis zum Abschluss dauern kann, da jede Antwort vom Server innerhalb des Time out-Zeitraums empfangen wird, auch wenn der Zeitraum für alle Antworten länger als der Time out-Zeitraum war.

Wenn ein Aufruf abgebrochen wird, wird der Server auch nicht über den Abbruch benachrichtigt. Der Server führt den Aufruf daher wahrscheinlich zu einem bestimmten Zeitpunkt aus, und der Client ignoriert einfach die Antwort des Servers.

Die gefährlichste Fallstricke bei Aufruftime outs ist das Einrichten eines kurzen Time outs und das Wiederholen des Aufrufs auf demselben Server. Das folgende Szenario veranschaulicht die Schädlichkeit dieses Ansatzes:

Imagine einen Server, der nahezu ausgelastet ist. Es gibt eine Reihe von Clients mit sehr kurzen Time outs, z. B. fünf Sekunden. Ein vorübergehender Verlust der Netzwerkkonnektivität oder Überlastung an einem Router führt dazu, dass die Serverantworten einige Sekunden lang ausfällt. In Ethernet-Netzwerken kann diese Situation leicht durch einen Aktivitätsspitzen auf einer Verbindung verursacht werden, die der Server mit einem anderen Computer teilt. Der Server kann nicht alle Antworten vor dem Fünf-Sekunden-Time out senden. Die Clients erhalten ihre Aufrufe abgebrochen und wiederholen sofort den Vorgang. Der Server weiß nicht, dass die Aufrufe Wiederholungen sind, und führt sie ebenfalls aus. Anstatt also die normale Arbeitsauslastung von Aufrufen auszuführen, werden 30-50 % mehr Aufrufe ausgeführt, je nachdem, wie viele Clients ein Time out haben. Wenn die Kapazität überschritten wird und der Server nicht innerhalb von fünf Sekunden auf alle Clients reagieren kann, werden weitere Aufrufe an den Server gesendet. Die Clients führen die gleichen Aufrufe erneut aus. Da der Server überlastet ist und vorherige Aufrufe verarbeitet, kann er innerhalb des Time outs nicht reagieren. Sobald die Antwort erfolgt ist, haben die Clients das Time out erreicht, einen neuen Aufruf ausgegeben und die Antwort verworfen. Im schlimmsten Fall wird der Server erst nach dem Neustart wiederhergestellt. Je nach Clientzugriffsmuster kann die Wiederherstellung erst erfolgen, wenn eine ausreichende Anzahl von Clients beendet wurde.

> [!Note]  
> Aufruftime outs funktionieren nur in den [**Protokollsequenzen ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_ http.**](/windows/desktop/Midl/ncacn-http)

 

 

 