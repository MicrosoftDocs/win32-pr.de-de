---
title: Verhindern von Client seitigen hängen
description: Es gibt zwei Möglichkeiten, wie der Client die Netzwerk Konnektivität beeinträchtigen kann, kann dazu führen, dass Serveranforderungen verloren gehen oder der Server selbst abstürzen kann. Mit den Standardoptionen führt RPC nie einen Timeout aus, und Ihr Client Thread wartet immer auf eine Antwort.
ms.assetid: 2c201e29-9d9c-48e6-b0b5-68e4b25c3fb7
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, verhindern von Client hängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d4b5fc92ca18b575d081cd7b5abf90929e7df5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727785"
---
# <a name="preventing-client-side-hangs"></a>Verhindern von Client seitigen hängen

Der Client kann auf zwei Arten hängen: die Netzwerk Konnektivität kann dazu führen, dass Serveranforderungen verloren gehen oder der Server selbst abstürzen kann. Mit den Standardoptionen führt RPC nie einen Timeout aus, und Ihr Client Thread wartet immer auf eine Antwort.

Es gibt zwei Methoden, um dies zu verhindern: Speichern Sie Alives und Timeouts.

## <a name="tcp-keep-alives"></a>TCP-Keep-Alives

Der Client kann so eingerichtet werden, dass er regelmäßig einen Ping-Befehl für den Server durchführt, um sicherzustellen, dass der Server Bei den Pings handelt es sich um TCP-Keep-Alives für die HTTP-Protokoll Sequenzen [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_**](/windows/desktop/Midl/ncacn-http) . Daher sind Sie in der CPU-Auslastung und der Netzwerkbandbreite effizient. Um Keep-Alives für einen bestimmten Remote Prozedur aufzurufen, verwenden Sie die [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion vor dem Initiieren des Aufrufes. Diese Funktion nimmt ein Bindungs Handle und ein Timeout als Argumente an. Jeder Remote Prozedur Aufruf für dieses Bindungs Handle nach **RpcMgmtSetComTimeout** verwendet das angegebene Timeout.

Der Timeout-Parameter für die [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion gibt an, wie lange die RPC-Laufzeit wartet, bevor Sie die Keep-Alives einschaltet. Der Timeout Wert ist ein Wert zwischen 0 und 10, wobei 0 für das minimale Timeout und 10 für das unbegrenzte Zeit Limit (kein Timeout) steht. Das einmalige Timeout ist nicht in Sekunden angegeben. die Übersetzung vom Timeout Wert, der an die **RpcMgmtSetComTimeout** -Funktion in Sekunden angegeben wird, erfolgt über die RPC-Laufzeit und ist Implementierungs spezifisch.

In der folgenden Tabelle sind die Übersetzungen für Windows 2000 und Windows XP in Sekunden angegeben. In zukünftigen Versionen von Windows kann die Zuordnung zwischen dem Timeout Parameter und dem Timeout Wert in Sekunden geändert werden:

| Timeout Parameter                       | Tatsächlicher Timeout in Sekunden |
|-----------------------------------------|----------------------------|
| 0 (Minuten Timeout für RPC- \_ C- \_ Bindung \_ \_ )       | 120                        |
| 1                                       | 240                        |
| 2                                       | 360                        |
| 3                                       | 480                        |
| 4                                       | 600                        |
| 5 (Standard Timeout für RPC- \_ C- \_ Bindung \_ \_ )   | 720                        |
| 6                                       | 840                        |
| 7                                       | 960                        |
| 8                                       | 1080                       |
| 9 (max. RPC- \_ C- \_ Bindungs \_ \_ Timeout)       | 1200                       |
| 10 ( \_ unbegrenztes RPC-C- \_ Bindungs \_ \_ Timeout) | Unbegrenzte Zeitüberschreitung          |



 

Sobald die Keep-Alives aktiviert sind, sendet der Client jede Sekunde ein Keep-Alive-Paket. Wenn auf dem Server keine Bestätigung für drei oder mehr Keep-Alives vorhanden ist, deklariert der Client die Verbindung, und der Remote Prozedur Rückruf schlägt fehl. Wenn der Server innerhalb des angegebenen Timeouts eine Antwort sendet, werden die "Alives" nicht aktiviert. Wenn der Server auf die Beibehaltung von Alives reagiert, aber nicht auf den Remote Prozedur aufzurufen antwortet, setzt der Client die Übermittlung von "Keep-Alives" fort. Nachdem der Server auf den RPC-Aufruf reagiert hat, sind die Keep-Alives deaktiviert. Für Windows 2000 sind Keep-Alives nur bei synchronen RPC-Aufrufen aktiviert. Für Windows XP sind Keep-Alives auch für asynchrone RPC-Aufrufe aktiviert.

Es ist verlockend, Keep-Alives auf den niedrigsten Wert festzulegen, um sicherzustellen, dass die Client Anwendung rechtzeitig auf Netzwerkprobleme antwortet. Diese Versuchung sollte sorgfältig beachtet werden, und es wird geprüft, ob ein aggressiver Wert gewährleistet ist. Ein Server, der vorübergehend die Konnektivität verliert, ist möglicherweise nach dem Wiederherstellen der Konnektivität von zahlreichen Clients überflutet. Darüber hinaus kann es länger als zwei Minuten dauern, bis der Server mehr als zwei Minuten benötigt, und der Server kann sich mehr CPU-Zeit ausgeben, als die Ausführung nützlicher arbeiten. Daher sollten Keep-Alives mit Moderation verwendet werden. Wenn der Client nicht tolerieren kann, dass sein Thread über lange Zeiträume hinweg gebunden ist, sollte der asynchrone RPC berücksichtigt werden.

Andere Protokoll Sequenzen können unterschiedliche Mechanismen zum erkennen nicht reagierender Server implementieren, je nachdem, welcher Transport verwendet wird. Der [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) -Transport verwendet keine Keep-Alives. Da die gesamte Kommunikation in **Ncalrpc** lokal ist und der Server nicht reagiert, während ein Aufruf ausgeführt wird, kann die RPC-Laufzeit auf dem Client den Aufruf sofort nicht durchführen.

## <a name="call-time-outs"></a>Timeout bei Aufrufen

TCP-Keep-Alives sind in Ordnung, wenn die Netzwerk Konnektivität unterbrochen wird oder der Server abstürzt. Wenn der Server jedoch in den Benutzermodus wechselt, werden die TCP-Keep-Alives erfolgreich zurückgegeben, aber der-Befehl wird nie zurückgegeben. Zur Bewältigung dieses Szenarios wurde für Windows XP eine neue Lauf Zeit Option hinzugefügt: Timeout für RPC- \_ C- \_ opt- \_ Aufruf \_ . Diese Option weist die RPC-Laufzeit an, bei jedem Senden einer Anforderung an den Server einen Timer einzurichten. Wenn der Timer abläuft, wird der Aufruf automatisch abgebrochen und abgeschlossen, wenn der RPC- \_ S- \_ Aufruf \_ abgebrochen wurde. Solange der Server innerhalb des angegebenen Zeitraums antwortet, wird der Aufruf vom Client nicht abgebrochen. Dies bedeutet, dass ein multifragmentaufruf mehr Zeit in Anspruch nehmen kann als das Timeout, da jede Antwort vom Server innerhalb des Timeout Zeitraums empfangen wird, auch wenn der Zeitraum für alle eingehenden Antworten über dem Timeout Zeitraum liegt.

Wenn ein-Befehl abgebrochen wird, wird der Server außerdem nicht über den Abbruch benachrichtigt. Der Server führt den-Vorgang daher wahrscheinlich zu einem beliebigen Zeitpunkt aus, und der Client ignoriert einfach die Antwort vom Server.

Der gefährlichste Fall bei Aufruf Zeiten ist das Einrichten eines kurzen Timeouts und wiederholen des Aufrufes auf demselben Server. Das folgende Szenario veranschaulicht die Gefahren dieses Ansatzes:

Stellen Sie sich einen Server vor, der die Kapazität fast erreicht Es verfügt über eine Reihe von Clients mit sehr kurzen Zeit Ausfällen, z. b. fünf Sekunden. Ein vorübergehender Verlust von Netzwerk Konnektivität oder Überlastung bei einem Router führt zu einem Ausfall der Server Antworten für einige Sekunden. In Ethernet-Netzwerken kann diese Situation problemlos durch einen Aktivitäts Anstieg bei einem Link verursacht werden, der vom Server mit einem anderen Computer gemeinsam verwendet wird. Der Server verwaltet nicht, um alle Antworten vor dem fünf-Sekunden-Timeout zu senden. Die Aufrufe der Clients werden abgebrochen, und Sie werden sofort wiederholt. Der Server weiß nicht, dass die Aufrufe Wiederholungen ausführen, und führt Sie auch aus. Daher führt Sie anstelle der normalen Arbeitsauslastung von Aufrufen 30-50% weitere Aufrufe aus, je nachdem, wie viele Clients ein Timeout feststellten. Wenn diese Kapazität überschritten wird und der Server nicht innerhalb von fünf Sekunden auf alle Clients antworten kann, wird eine weitere Runde von Aufrufen an den Server gesendet. Die Clients werden immer wieder mit denselben aufrufen fortgeführt. da der Server bei der Verarbeitung vorheriger Aufrufe überladen ist, kann er nicht innerhalb des Zeitüberschreitung Antworten. Nach dem Antworten haben die Clients den Timeout Wert ermittelt, einen neuen Aufruf ausgegeben und die Antwort verworfen. Im ungünstigsten Fall wird der Server bis zum Neustart nicht wieder hergestellt. abhängig vom Client Zugriffsmuster wird die Wiederherstellung möglicherweise erst wieder hergestellt, wenn eine ausreichende Anzahl von Clients angehalten wurde.

> [!Note]  
> Aufruf Zeiten funktionieren nur in den HTTP [**-Protokoll Sequenzen ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_**](/windows/desktop/Midl/ncacn-http) .

 

 

 