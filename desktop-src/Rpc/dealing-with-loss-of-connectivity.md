---
title: Umgang mit Verbindungsverlust
description: Umgang mit Verbindungsverlust
ms.assetid: a90fcb5a-773e-4c21-bf6c-c3519ec13a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8e7a8088cfe09a4c4026c16cc3dc5ea36b3430
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728865"
---
# <a name="dealing-with-loss-of-connectivity"></a>Umgang mit Verbindungsverlust

Nachdem ein RPC-Aufruf abgeschlossen wurde, wird die Verbindung nicht geschlossen. Er ist als frei markiert. Der Server kann daher ausgefallen sein, oder die Netzwerk Konnektivität kann während oder zwischen Aufrufen unterbrochen werden, während sich eine Verbindung im Pool befindet. Bei der Richtlinie werden diese Aufrufe von der RPC-Laufzeit nur dann erneut versucht, wenn die folgenden beiden Bedingungen erfüllt sind:

-   Der Server kann den Aufruf nicht ausführen, oder der Aufruf ist idempotent.
-   Der Client kann Wiederholungs Versuche auf Leistungs effiziente Weise implementieren.

In den folgenden Abschnitten werden die beiden Bedingungen erweitert und verdeutlicht.

Bei einem idempotenten Aufruf handelt es sich um einen Aufruf, der auf dem Server mehrmals ausgeführt werden kann, ohne dass unerwünschte Nebeneffekte auftreten. Beispielsweise ist ein RPC-Aufruf, der den Saldo der Bank für ein bestimmtes Konto abfragt, idempotent. Wenn dieser Befehl aufgrund eines Verlusts der Konnektivität zweimal ausgeführt wird, erfolgt keine Beschädigung. Ein weiteres Beispiel für einen idempotenten Aufruf besteht darin, die Adresse eines Kunden in einer Datenbank zu ändern. Die doppelte Ausführung ist in Ordnung, da die zweite Ausführung einfach die bereits aktuelle Adresse durch dieselbe Adresse ersetzt. Ein Vorgang wie "Subtrahieren von 50 Dollar von Konto XYZ" ist nicht idempotent. Der Verlust der Netzwerk Konnektivität sollte nicht zu mehreren Ausführungen eines solchen Aufrufes führen.

Um sicher zu sein, werden alle Aufrufe von der RPC-Laufzeit als nicht idempotent behandelt. Das \[ idempotente \] -Attribut wird nicht für [**ncacn \_ -IP- \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp)unterstützt und wird ignoriert. Daher wird die erste Bedingung in der vorangehenden Liste auf den Server reduziert, der den-Befehl *nicht ausführen kann*.

In vielen Fällen kann die RPC-Laufzeit nicht endgültig ermitteln, ob der Aufruf nicht bereits auf dem Server ausgeführt wurde. In solchen Fällen wird vom Client nicht erneut versucht, den-Befehl auszuführen.

In den folgenden Beispielen wird veranschaulicht, wann die RPC-Laufzeit einen Aufruf durchführt oder nicht erneut versucht:

-   Ein Server wird neu gestartet.

    Ein einfacher RPC-Aufruf ohne Sicherheit wird an einer Schnittstelle vorgenommen, auf der nach dem Neustart kein vorheriger Aufruf erfolgt ist. Da keine Aufrufe an dieser Schnittstelle durchgeführt wurden, versucht die RPC-Laufzeit zunächst, die Verwendung der Schnittstelle auszuhandeln. Er sendet ein Paket mithilfe einer Verbindung im Pool. Da der Server neu gestartet wurde und die Verbindung nicht mehr gültig ist, wird ein Fehler zurückgegeben. Da die Client seitige RPC-Laufzeit noch nicht mit dem Senden der Daten für den eigentlichen Aufruf begonnen hat, ermittelt der Client, dass der Server möglicherweise nicht für diese Daten ausgeführt wurde. Daher wird die Verbindung geschlossen, und es wird nach einer anderen Verbindung im Pool gesucht. Wenn keine Verbindung gefunden werden kann, wird eine neue Verbindung geöffnet, und es wird versucht, die Verwendung der Schnittstelle erneut auszuhandeln. Wenn dies erfolgreich ist, wird der-Vorgang ausgeführt (d. h., es wird eine Wiederholung durchgeführt, da der Fehler vor dem Start des Aufrufes erkannt wurde).

-   Ein RPC-Aufruf mit Sicherheit auf Datenschutzebene (Verschlüsselung) erfolgt bei einer Verbindung mit einem bereits ausgehandelten Sicherheitskontext.

    Um eine effiziente Leistung sicherzustellen, verschlüsselt die RPC-Laufzeit das gemarshallte Paket Inline (über die Klartext-Daten). Tritt beim Versuch, die Daten zu senden, ein Fehler auf, kann die RPC-Laufzeit den Aufruf nicht wiederholen, da die Klartext-Daten mit den verschlüsselten Daten überschrieben wurden und die Daten nicht erneut mit einem neuen Sicherheitskontext verschlüsselt werden können. Daher wird keine Wiederholung durchgeführt.

-   Das Senden eines nicht ersten Fragments schlägt fehl.

    Es wird keine Wiederholung durchgeführt, da die RPC-Laufzeit den Inhalt des ersten Fragments nach Abschluss verwerfen kann und keine Möglichkeit hat, das erste Fragment erneut zu senden.

-   Die RPC-Anforderung wird gesendet.

    Der Server bricht die Verbindung ab. Es wurde kein Wiederholungsversuch unternommen, da RPC nicht ermitteln kann, ob der Server den Aufruf empfangen und die Ausführung gestartet hat.

Wenn vom Server ein dynamischer Endpunkt verwendet wird, löst RPC den Endpunkt bei Wiederholungs versuchen nicht erneut auf. Dies bedeutet Folgendes: Wenn ein Server heruntergefahren und wieder hochgefahren wird, befindet er sich möglicherweise auf einem anderen Endpunkt, und RPC löst den Endpunkt nicht transparent erneut aus, wenn ein Aufruf wiederholt wird. Um das erneute Auflösen des Endpunkts zu erzwingen, sollte der RPC-Client [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) aufrufen, bevor ein Aufruf wiederholt wird.

In vielen Fällen kann es vorkommen, dass ein RPC-Client einen Wiederholungs Mechanismus zusätzlich zu RPC erstellt, wenn ein RPC-Client ermitteln kann, ob es sich um einen idempotenten Aufruf handelt, oder wenn er Daten beibehält.

> [!Note]  
> Wenn es sich bei dem Server um einen Cluster handelt und die verschiedenen Knoten des Clusters verschiedene Versionen der Server Software ausführen, kann ein RPC-Wiederholungsversuch den Aufruf auf einem anderen Knoten des Clusters im Falle eines Failovers und potenziell auf einer anderen Version des Servers durchführen. Stellen Sie in solchen Bereitstellungs Szenarien sicher, dass der Client nicht von einer bestimmten Version der Server Software abhängig ist, um einen bestimmten-Befehl auszuführen. Wenn dies der Fall ist, sollte der Client einen Mechanismus zusätzlich zu RPC erstellen, der solche Bedingungen erkennt und behandelt.

 

 

 