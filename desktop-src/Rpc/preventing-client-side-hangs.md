---
title: Verhindern von clientseitigen Hängen
description: Es gibt zwei Möglichkeiten, wie Ihr Client die Netzwerkkonnektivität abstürzen kann. Dies kann dazu führen, dass Serveranforderungen verloren gehen, oder der Server selbst kann abstürzen. Bei Standardoptionen kommt es bei RPC nie zu einem Time out eines Aufrufs, und Ihr Clientthread wartet für immer auf eine Antwort.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- Remoteprozeduraufruf-RPC , bewährte Methoden, Verhindern von Clienthängen
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

Es gibt zwei Möglichkeiten, wie Ihr Client hängen bleibt: Die Netzwerkkonnektivität kann dazu führen, dass Serveranforderungen verloren gehen, oder der Server selbst stürzt ab. Bei Standardoptionen kommt es bei RPC nie zu einem Time out eines Aufrufs, und Ihr Clientthread wartet für immer auf eine Antwort.

Es gibt zwei Methoden, um dies zu verhindern: Keep Alives und Time outs.

## <a name="tcp-keep-alives"></a>TCP Keep Alives

Der Client kann so eingerichtet werden, dass er den Server regelmäßig pingt, um sicherzustellen, dass der Server ausgeführt wird. Die Pings sind TCP-Keep-Alives für die PROTOKOLLsequenzen [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http) und sind daher effizient in cpu-Auslastung und Netzwerkbandbreite. Um Keep Alives für einen bestimmten Remoteprozeduraufruf zu aktivieren, verwenden Sie die [**RpcMgmtSetComTimeout-Funktion,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) bevor der Aufruf initiiert wird. Diese Funktion verwendet ein Bindungshand handle und ein Time out als Argumente. Jeder Remoteprozeduraufruf für dieses Bindungshand handle, **nachdem RpcMgmtSetComTimeout** das angegebene Timeout verwendet hat.

Der Timeout-Parameter für die [**RpcMgmtSetComTimeout-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) gibt an, wie lange die RPC-Laufzeit wartet, bevor keep alive aktiviert wird. Das Time out ist ein Wert zwischen 0 und 10, wobei 0 das minimale Time out und 10 ein unendliches Time out (kein Time out) ist. Das Time out selbst liegt nicht in Sekunden. Die Übersetzung vom Timeoutwert, der der **RpcMgmtSetComTimeout-Funktion** bereitgestellt wird, in Sekunden erfolgt durch die RPC-Laufzeit und ist implementierungsspezifisch.

Die folgende Tabelle enthält die Übersetzung in Sekunden für Windows 2000 und Windows XP. Zukünftige Versionen von Windows ändern möglicherweise die Zuordnung zwischen dem Timeout-Parameter und dem Timeoutwert in Sekunden:

| Timeoutparameter                       | Tatsächlicher Time out in Sekunden |
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
| 9 (MAXIMALES TIMEOUT FÜR RPC \_ \_ \_ \_ C-BINDUNG)       | 1200                       |
| 10 (RPC \_ C \_ BINDING INFINITE \_ \_ TIMEOUT) | Unendliches Time out          |



 

Sobald die Keep-Alive-Pakete aktiviert sind, sendet der Client jede Sekunde ein Keep-Alive-Paket. Wenn vom Server keine Bestätigung für drei oder mehr Keep-Alive-Daten verfügbar ist, deklariert der Client die Verbindung als nicht mehr, und der Remoteprozeduraufruf schlägt fehl. Wenn der Server innerhalb des angegebenen Time outs eine Antwort sendet, werden Keep Alives nicht aktiviert. Wenn der Server auf Keep Alive reagiert, aber nicht auf den Remoteprozeduraufruf reagiert, sendet der Client weiterhin Keep-Alive-Nachrichten. Sobald der Server auf den RPC-Aufruf reagiert, werden die Keep-Alive-Aufrufe deaktiviert. Für Windows 2000 werden Keep Alives nur für synchrone RPC-Aufrufe aktiviert. Für Windows XP werden Keep-Alive-Vorgänge auch für asynchrone RPC-Aufrufe aktiviert.

Es ist verlockend, Keep Alives auf den niedrigsten Wert zu setzen, um sicherzustellen, dass die Clientanwendung rechtzeitig auf Netzwerkprobleme reagiert. Diese Berücksichtigung sollte sorgfältig geprüft werden, und es sollte sorgfältig geprüft werden, ob ein aggressiver Wert gerechtfertigt ist. Ein Server, der vorübergehend die Konnektivität verliert, wird möglicherweise mit Keep-Alive-Daten von zahlreichen Clients überflutet, sobald die Konnektivität wiederhergestellt wurde. Darüber hinaus können lange Berechnungsaufgaben mehr als zwei Minuten dauern, und der Server wird möglicherweise mehr CPU-Zeit für die Beantwortung von Keep-Alive-Vorgängen ausgeben, als nützliche Aufgaben auszuführen. Aus diesem Grund sollten Keep-Alives mit Moderation verwendet werden. Wenn der Client nicht tolerieren kann, dass sein Thread über einen längeren Zeitraum gebunden ist, sollte der asynchrone RPC berücksichtigt werden.

Andere Protokollsequenzen können unterschiedliche Mechanismen zum Erkennen nicht reagierender Server implementieren, je nachdem, welcher Transport verwendet wird. Der [**ncalrpc-Transport**](/windows/desktop/Midl/ncalrpc) verwendet keine Keep-Alive-Daten. Da alle Kommunikationen in **ncalrpc** lokal sind, schlägt die RPC-Laufzeit auf dem Client sofort fehl, wenn der Server nicht mehr reagiert, während ein Aufruf ausgeführt wird.

## <a name="call-time-outs"></a>Time outs für Aufrufe

TCP-Keep-Alives sind in Ordnung, wenn die Netzwerkkonnektivität verloren geht oder der Server abstürzt. Wenn der Server jedoch im Benutzermodus deadlocks ist, gibt TCP Keep Alive erfolgreich zurück, aber der Aufruf wird nie zurückgeben. Um dieses Szenario zu behandeln, wurde eine neue Laufzeitoption für Windows XP: RPC \_ C \_ OPT CALL \_ \_ TIMEOUT hinzugefügt. Diese Option weist die RPC-Laufzeit an, bei jedem Senden einer Anforderung an den Server einen Timer zu erstellen. Wenn der Timer abläuft, wird der Aufruf automatisch abgebrochen und mit RPC \_ S \_ CALL CANCELLED \_ abgeschlossen. Solange der Server innerhalb des angegebenen Zeitlimits antwortet, bricht der Client den Aufruf nicht ab. Dies bedeutet, dass ein Multifragmentaufruf länger als der Time outzeitraum dauern kann, da jede Antwort vom Server innerhalb des Time outzeitraums empfangen wird, obwohl der Zeitraum für alle Antworten über dem Time out-Zeitraum lag.

Wenn ein Aufruf abgebrochen wird, wird der Server außerdem nicht über den Abbruch benachrichtigt. Daher führt der Server den Aufruf wahrscheinlich zu einem bestimmten Zeitpunkt aus, und der Client ignoriert einfach die Antwort vom Server.

Die gefährlichste Falle bei Time outs für Aufrufe ist die Einrichtung eines kurzen Time out und das Wiederholen des Aufrufs auf demselben Server. Das folgende Szenario veranschaulicht die Herangehensweise:

Imagine server, der nahezu kapazitätsnah betrieben wird. Es verfügt über eine Reihe von Clients mit sehr kurzen Time outs, z. B. fünf Sekunden. Ein vorübergehender Verlust der Netzwerkkonnektivität oder Überlastung an einem Router führt zu einem Ausfall der Serverantworten für einige Sekunden. In Ethernet-Netzwerken kann diese Situation leicht durch einen Aktivitätss burst an einer Verbindung verursacht werden, die der Server mit einem anderen Computer teilt. Der Server kann nicht alle Antworten vor dem Time out von fünf Sekunden senden. Die Clients erhalten ihre Aufrufe abgebrochen, und wiederholen sofort den Vorgang. Der Server weiß nicht, dass es sich bei Denkaufrufen um Erneutentrufe handelt, und führt sie auch aus. Anstatt also die normale Arbeitsauslastung von Aufrufen auszuführen, werden 30 bis 50 % mehr Aufrufe ausgeführt, je nachdem, wie viele Clients ein Time out auft haben. Wenn dies die Kapazität überschreitet und der Server nicht innerhalb von fünf Sekunden auf alle Clients antworten kann, werden weitere Aufrufe an den Server gesendet. Die Clients führen weiterhin die gleichen Aufrufe aus, und da der Server bei der Verarbeitung vorheriger Aufrufe überlastet ist, kann er nicht innerhalb des Time outs antworten. Nach der Antwort haben die Clients das Time out getroffen, einen neuen Aufruf ausgegeben und die Antwort verworfen. Im schlimmsten Fall wird der Server erst nach dem Neustart wiederhergestellt, und je nach Clientzugriffsmuster wird er möglicherweise erst wiederhergestellt, wenn eine ausreichende Anzahl von Clients beendet wurde.

> [!Note]  
> Time outs für Aufrufe funktionieren nur für die [**ncacn \_ ip \_ tcp-**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn-HTTP-Protokollsequenzen. \_**](/windows/desktop/Midl/ncacn-http)

 

 

 