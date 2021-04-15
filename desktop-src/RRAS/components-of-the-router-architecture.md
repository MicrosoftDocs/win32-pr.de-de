---
title: Komponenten der routerarchitektur
description: In der Dokumentation zur Routerverwaltung wird häufig auf die folgenden Komponenten des Routers verwiesen.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- routerrras, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb0cc69de5402b03550873b3b052f6329b5238
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471268"
---
# <a name="components-of-the-router-architecture"></a>Komponenten der routerarchitektur

In der Dokumentation zur Routerverwaltung wird häufig auf die folgenden Komponenten des Routers verwiesen.

Dynamic Interface Manager (Dim)

Alle routerverwaltungfunktionen durchlaufen Dim. Abhängig von der Art der Funktion kann Dim den-Rückruf an einen der routermanager übergeben. Funktionen, die nur mit Schnittstellen behandelt werden, werden von Dim behandelt. Wenn sich die Funktion auf Routing Protokolle auswirkt, ruft Dim den routermanager für den Transport auf, der diesem Protokoll entspricht. Wenn sich die Funktion z. b. auf das OSPF-Protokoll (Open kürzeste Path First) auswirkt, ruft Dim den IP-routermanager auf, da OSPF ein IP-Routing Protokoll ist.

Routermanager

Jeder Routing fähige Transport, der in die routerarchitektur passt, verfügt über einen eigenen routermanager. Derzeit sind Router-Manager für die IP-und IPX-Transporte vorhanden. Die routermanager verwalten Routerprotokolle und andere Routing Client Typen, die auf den Schnittstellen auf dem lokalen Computer ausgeführt werden.

Routing Protokolle und andere Clients

Clients sind Dienstanbieter, die innerhalb des Frameworks der routerarchitektur funktionieren. Routing Protokolle sind eine Art von Client, der vom Router unterstützt wird.

Clients sind spezifisch für einen bestimmten Routing fähigen Transport: entweder IP oder IPX. Die Routing Protokolle für den IP-Transport umfassen Open kürzeste Path First (OSPF) und Routing Information Protocol (RIP). Beispiele für IPX-Routing Protokolle sind Service Advertising Protocol (SAP) und RIP für IPX. Ein Beispiel für einen Client, bei dem es sich nicht um ein Routing Protokoll handelt, ist Network Address Translation (NAT) für IP.

Die Schnittstelle zwischen dem routermanager und einem Client wird im Abschnitt [Routing Protokoll Schnittstelle](about-routing-protocol-interface.md)beschrieben. Alle Clients entsprechen dieser Schnittstelle. Mithilfe dieser Schnittstelle können Lieferanten eigene Clients implementieren, die mit dem Router kompatibel sind.

[Schnittstellen](interfaces.md)

Eine Schnittstelle ist eine Verbindung mit einem externen Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Schnittstellen *Index* identifiziert. Schnittstellen sind logische Entitäten. routerclients wie NAT oder OSPF befassen sich ähnlich mit allen Schnittstellentypen. Im Hinblick auf die Implementierung kann eine Schnittstelle jedoch eine dedizierte Verbindung (z. b. ein lokales Netzwerk (LAN)) oder eine nicht dedizierte DFÜ-Verbindung (z. b. eine PPP-Verbindung mit einem Wide Area Network (WAN)) darstellen.

Im Fall einer LAN-Schnittstelle entspricht die Schnittstelle einem tatsächlichen physischen Gerät des Computers, einem LAN-Adapter. Im Fall einer WAN-Schnittstelle wird die Schnittstelle einem Port zugeordnet, wenn eine Verbindung hergestellt wird. Der Port kann ein COM-Port, ein paralleler Anschluss oder ein virtueller Port (für Tunnel wie PPTP und L2TP) sein.

WAN-Schnittstellen haben die zusätzliche Qualität, dass Sie normalerweise nur zu dem Zeitpunkt, zu dem eine Verbindung hergestellt wird, eine Netzwerkadresse erhalten. Beispielsweise erhält eine WAN-Schnittstelle, die PPP verwendet, während des Verbindungs Vorgangs vom Remotepeer eine Netzwerkschicht Adresse. Das Empfangen einer Netzwerkadresse als Teil des Verbindungs Vorgangs wird manchmal als " *späte Bindung*" bezeichnet.

 

 




