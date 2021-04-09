---
title: Routing Protokoll
description: Bei einem Routing Protokoll handelt es sich um einen Clienttyp, der beim Routing Tabellen-Manager registriert wird. Router verwenden Routing Protokolle zum Austauschen von Informationen zu Routen zu einem Ziel.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036867"
---
# <a name="routing-protocol"></a>Routing Protokoll

Bei einem Routing Protokoll handelt es sich um einen Clienttyp, der beim Routing Tabellen-Manager registriert wird. Router verwenden Routing Protokolle zum Austauschen von Informationen zu Routen zu einem Ziel.

Routing Protokolle sind entweder Unicast oder Multicast. Routing Protokolle ankündigen Routen zu einem Ziel.

Eine unicastroute zu einem Ziel wird von einem Unicastrouting-Protokoll verwendet, um Unicastdaten an dieses Ziel weiterzuleiten. Beispiele für Unicast-Routing Protokolle sind: Routing Information Protocol (RIP), Open kürzeste Path First (OSPF) und Border Gateway Protocol (BGP).

Eine Multicast Route zu einem Ziel wird von einigen Multicast Routing Protokollen verwendet, um die Informationen zu erstellen, die zum Weiterleiten von Multicast Daten von Hosts im Zielnetzwerk der Route verwendet werden (als umgekehrte Pfad Weiterleitung bezeichnet). Beispiele für Multicast-Routing Protokolle: Multicast Open kürzeste Path First (MUF), Distance Vector Multicast Routing Protocol (DVMRP) und Protocol Independent Multicast (PIM).

Der Routing Tabellen-Manager unterstützt mehrere Instanzen desselben Protokolls (z. b. die Implementierung von OSPF von Microsoft und eine OSPF eines Drittanbieters), die auf dem Router ausgeführt werden. Dadurch können Router die verschiedenen Funktionen jeder Version verwenden. Diese Protokolle verfügen über unterschiedliche Protokoll Bezeichner.

Protokoll Bezeichner bestehen aus einer Hersteller-ID und einem Protokoll spezifischen Bezeichner. Der Protokoll spezifische Bezeichner ist für verschiedene Implementierungen des Protokolls identisch, wie z. b. die Implementierung von OSPF von Microsoft und die Implementierung von OSPF von Drittanbietern. Nur wenn der Anbieter und die Protokoll spezifischen Bezeichner kombiniert werden, gibt es einen eindeutigen Bezeichner für ein Routing Protokoll.

Ein Protokoll mit der gleichen Protokoll Kennung (d. h. dem gleichen Hersteller Bezeichner und Protokoll spezifischen Bezeichner) kann mehrmals beim Routing Tabellen-Manager registriert werden. Jedes Mal wird das Protokoll mithilfe eines anderen protokollinstanzbezeichners registriert. Beispielsweise kann eine Implementierung von OSPF von einem bestimmten Hersteller als "Vendor-OSPF-1" und "Vendor-OSPF-2" registriert werden. Dies ermöglicht einer bestimmten Protokoll Implementierung, die in der Routing Tabelle beibehaltenen Informationen zu partitionieren.

 

 




