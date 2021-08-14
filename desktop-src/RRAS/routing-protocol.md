---
title: Routingprotokoll
description: Ein Routingprotokoll ist ein Clienttyp, der beim Routingtabellen-Manager registriert wird. Router verwenden Routingprotokolle, um Informationen zu Routen zu einem Ziel austauschen.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 879d540662db7d1a1603bf40818101d0e7f9cb6988d4c0065f922fdc8f73e381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977843"
---
# <a name="routing-protocol"></a>Routingprotokoll

Ein Routingprotokoll ist ein Clienttyp, der beim Routingtabellen-Manager registriert wird. Router verwenden Routingprotokolle, um Informationen zu Routen zu einem Ziel austauschen.

Routingprotokolle sind entweder Unicast oder Multicast. Routingprotokolle geben Routen für ein Ziel an.

Eine Unicastroute zu einem Ziel wird von einem Unicastroutingprotokoll zum Weiterleiten von Unicastdaten an dieses Ziel verwendet. Beispiele für Unicastroutingprotokolle sind: Routing Information Protocol (RIP), Open Shortest Path First (OSPF) und Border Gateway Protocol (BGP).

Eine Multicastroute zu einem Ziel wird von einigen Multicastroutingprotokollen verwendet, um die Informationen zu erstellen, die zum Weiterleiten von Multicastdaten von Hosts im Zielnetzwerk der Route verwendet werden (auch als Reversepfadweiterleitung bekannt). Beispiele für Multicastroutingprotokolle sind: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP) und Protocol Independent Multicast (PIM).

Der Routingtabellen-Manager unterstützt mehrere Instanzen desselben Protokolls (z. B. die Microsoft-Implementierung von OSPF und eines Drittanbieter-OSPF), die auf dem Router ausgeführt werden. Dadurch können Router die verschiedenen Funktionen der einzelnen Versionen verwenden. Diese Protokolle verfügen über unterschiedliche Protokollbezeichner.

Protokollbezeichner bestehen aus einem Anbieterbezeichner und einem protokollspezifischen Bezeichner. Der protokollspezifische Bezeichner ist für verschiedene Implementierungen des Protokolls identisch, z. B. die Microsoft-Implementierung von OSPF und eine Drittanbieterimplementierung von OSPF. Nur wenn hersteller- und protokollspezifische Bezeichner kombiniert werden, gibt es einen eindeutigen Bezeichner für ein Routingprotokoll.

Ein Protokoll mit demselben Protokollbezeichner (d. h. demselben Anbieterbezeichner und protokollspezifischen Bezeichner) kann mehrmals beim Routingtabellen-Manager registriert werden. Jedes Mal wird das Protokoll mit einem anderen Protokollinstanzbezeichner registriert. Beispielsweise kann eine Implementierung von OSPF von einem bestimmten Anbieter als Vendor-OSPF-1 und Vendor-OSPF-2 registriert werden. Dadurch kann eine bestimmte Protokollimplementierung die Informationen partitionieren, die in der Routingtabelle enthalten sind.

 

 




