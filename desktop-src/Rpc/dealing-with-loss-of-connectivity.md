---
title: Umgang mit Konnektivitätsverlust
description: Umgang mit Konnektivitätsverlust
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eac02c4440cb2e31a29e810d78dfd51764be3ba0ed5a6dc32f8c3e10824bd70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101680"
---
# <a name="dealing-with-loss-of-connectivity"></a>Umgang mit Konnektivitätsverlust

Nach Abschluss eines RPC-Aufrufs wird die Verbindung nicht geschlossen. sie ist als "free" gekennzeichnet. Daher kann der Server ausfallen oder die Netzwerkkonnektivität während oder zwischen Aufrufen unterbrochen werden, während sich eine Verbindung im Pool befindet. Richtlinienbedingt versucht die RPC-Laufzeit diese Aufrufe nur dann erneut, wenn die folgenden beiden Bedingungen erfüllt sind:

-   Der Server kann den Aufruf möglicherweise nicht ausführen, oder der Aufruf ist idempotent.
-   Der Client kann Wiederholungen leistungseffizient implementieren.

In den folgenden Absätzen werden die beiden Bedingungen erweitert und verdeutlicht.

Ein idempotenter Aufruf ist ein Aufruf, der mehr als einmal auf dem Server ohne unerwünschte Nebeneffekte ausgeführt werden kann. Beispielsweise ist ein RPC-Aufruf, der das Guthaben in der Bank für ein bestimmtes Konto abfragt, idempotent. Wenn dieser Aufruf aufgrund eines Verbindungsverlusts zweimal ausgeführt wird, wird kein Schaden angerichtet. Ein weiteres Beispiel für einen idempotenten Anruf ist das Ändern der Adresse eines Kunden in einer Datenbank. Die zweimalige Ausführung ist in Ordnung, da die zweite Ausführung einfach die bereits aktuelle Adresse durch die gleiche Adresse ersetzt. Ein Vorgang wie "Subtrahieren von Hunderten Dollar vom Konto xyz" ist nicht idempotent. Der Verlust der Netzwerkkonnektivität sollte nicht zu mehreren Ausführungen eines solchen Aufrufs führen.

Um sicher zu sein, behandelt die RPC-Laufzeit alle Aufrufe als nicht idempotent. Das \[ idempotente \] Attribut wird für [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)nicht unterstützt und ignoriert. Daher wird die erste Bedingung in der vorherigen Liste auf *den Server reduziert, der den Aufruf von nicht ausführen kann.*

In vielen Fällen kann die RPC-Laufzeit nicht eindeutig bestimmen, ob der Aufruf nicht bereits auf dem Server ausgeführt wurde. In solchen Fällen versucht der Client nicht, den Aufruf erneut auszuführen.

Die folgenden Beispiele veranschaulichen, wann die RPC-Laufzeit einen Aufruf erneut versucht oder nicht:

-   Ein Server wird neu gestartet.

    Ein einfacher, sicherheitsfreier RPC-Aufruf erfolgt auf einer Schnittstelle, für die nach dem Neustart kein vorheriger Aufruf erfolgt ist. Da für diese Schnittstelle keine Aufrufe durchgeführt wurden, versucht die RPC-Laufzeit zunächst, die Verwendung der Schnittstelle auszuhandeln. Es sendet ein Paket mithilfe einer Verbindung im Pool. Da der Server neu gestartet wurde und die Verbindung nicht mehr gültig ist, wird ein Fehler zurückgegeben. Da die clientseitige RPC-Laufzeit noch nicht mit dem Senden der Daten für den tatsächlichen Aufruf begonnen hat, stellt der Client fest, dass der Server für diese Daten möglicherweise nicht ausgeführt werden konnte. Daher wird die Verbindung geschlossen und nach einer anderen Verbindung im Pool gesucht. Wenn eine Verbindung nicht gefunden werden kann, wird eine neue Verbindung geöffnet, und es wird versucht, die Verwendung der -Schnittstelle erneut auszuhandeln. Wenn dies erfolgreich ist, wird der Aufruf ausgeführt (d.b. wird ein Wiederholungsversuch ausgeführt, da der Fehler vor dem Starten des Aufrufs erkannt wurde).

-   Ein RPC-Aufruf mit Sicherheit auf Datenschutzebene (Verschlüsselung) erfolgt bei einer Verbindung mit einem bereits ausgehandelten Sicherheitskontext.

    Um eine effiziente Leistung sicherzustellen, verschlüsselt die RPC-Laufzeit das gemarshallte Paket inline (über die Klartextdaten). Wenn beim Versuch, die Daten zu senden, ein Fehler auftritt, kann die RPC-Laufzeit den Aufruf nicht wiederholen, da die Klartextdaten mit den verschlüsselten Daten überschrieben wurden und die Daten nicht mit einem neuen Sicherheitskontext erneut verschlüsselt werden können. Aus diesem Grund wird kein Wiederholungsversuch durchgeführt.

-   Das Senden eines nicht ersten Fragments schlägt fehl.

    Eine Wiederholung wird nicht durchgeführt, da die RPC-Laufzeit möglicherweise den Inhalt des ersten Fragments verwirft, sobald es abgeschlossen ist, und keine Möglichkeit hat, erneut zu versuchen, das erste Fragment zu senden.

-   Die RPC-Anforderung wird gesendet.

    Der Server bricht die Verbindung ab. Es wird kein Wiederholungsversuch unternommen, da RPC nicht erkennen kann, ob der Server den Aufruf empfangen und mit der Ausführung begonnen hat.

Wenn der Server einen dynamischen Endpunkt verwendet, löst RPC den Endpunkt bei Wiederholungsversuche nicht erneut auf. Dies bedeutet, dass sich ein Server, wenn er heruntergefahren und wieder hochgefahren wird, möglicherweise auf einem anderen Endpunkt befindet, und RPC den Endpunkt nicht transparent wieder auflöst, wenn ein Aufruf wiederholt wird. Um eine erneute Auflösung des Endpunkts zu erzwingen, sollte der RPC-Client [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) aufrufen, bevor er einen Aufruf erneut versucht.

Wenn ein RPC-Client in vielen dieser Fälle ermitteln kann, ob ein Aufruf idempotent ist, oder wenn er Daten beibehält, die RPC verwirft, kann er einen Wiederholungsmechanismus über RPC erstellen.

> [!Note]  
> Wenn der Server ein Cluster ist und die verschiedenen Knoten des Clusters unterschiedliche Versionen der Serversoftware ausführen, kann eine RPC-Wiederholung den Aufruf bei einem Failover auf einem anderen Knoten des Clusters und möglicherweise auf einer anderen Version des Servers landen. Stellen Sie in solchen Bereitstellungsszenarien sicher, dass der Client nicht von einer bestimmten Version der Serversoftware abhängig ist, um einen bestimmten Aufruf auszuführen. In diesem Falle sollte der Client einen Mechanismus auf der Grundlage von RPC erstellen, der solche Bedingungen erkennt und behandelt.

 

 

 