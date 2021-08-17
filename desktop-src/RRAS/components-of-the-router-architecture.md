---
title: Komponenten der Routerarchitektur
description: In der Dokumentation zur Routerverwaltung wird häufig auf die folgenden Komponenten des Routers verwiesen.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- Router RRAS , Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f39f104e001db99076dcd29d9d5b603d5cf9f3c526d54cd16e1ed0e4d10c575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791594"
---
# <a name="components-of-the-router-architecture"></a>Komponenten der Routerarchitektur

In der Dokumentation zur Routerverwaltung wird häufig auf die folgenden Komponenten des Routers verwiesen.

Dynamic Interface Manager (DIM)

Alle Routerverwaltungsfunktionen passieren DIM. Je nach Art der Funktion kann DIM den Aufruf an einen der Router-Manager übergeben. Funktionen, die sich nur mit Schnittstellen befassen, werden von DIM verarbeitet. Wenn die Funktion Routingprotokolle beeinflusst, wird DIM den Router-Manager für den Transport aufrufen, der diesem Protokoll entspricht. Wenn die Funktion z. B. das OSPF-Protokoll (Open Shortest Path First) beeinflusst, wird von DIM der IP-Router-Manager aufgerufen, da OSPF ein IP-Routingprotokoll ist.

Router-Manager

Jeder routingfähige Transport, der in die Routerarchitektur passt, verfügt über einen eigenen Router-Manager. Derzeit sind Router-Manager für die IP- und IPX-Transporte vorhanden. Die Router-Manager verwalten Routerprotokolle und andere Typen von Routingclients, die auf Schnittstellen auf dem lokalen Computer ausgeführt werden.

Routingprotokolle und andere Clients

Clients sind Dienstanbieter, die innerhalb des Frameworks der Routerarchitektur funktionieren. Routingprotokolle sind ein Clienttyp, der vom Router unterstützt wird.

Clients sind spezifisch für einen bestimmten routingbaren Transport: IP oder IPX. Routingprotokolle für den IP-Transport umfassen Open Shortest Path First (OSPF) und Routing Information Protocol (RIP). Beispiele für IPX-Routingprotokolle sind Service Advertising Protocol (SAP) und RIP für IPX. Ein Beispiel für einen Client, der kein Routingprotokoll ist, ist die Netzwerkadressenübersetzung (Network Address Translation, NAT) für IP.

Die Schnittstelle zwischen dem Router-Manager und einem Client wird im Abschnitt [Routing protocol Interface (Routingprotokollschnittstelle) beschrieben.](about-routing-protocol-interface.md) Alle Clients entsprechen dieser Schnittstelle. Über diese Schnittstelle können Anbieter ihre eigenen Clients implementieren, die mit dem Router kompatibel sind.

[Schnittstellen](interfaces.md)

Eine Schnittstelle ist eine Verbindung mit einem externen Netzwerk. Jede Schnittstelle wird durch einen eindeutigen Schnittstellenindex *identifiziert.* Schnittstellen sind logische Entitäten. Routerclients wie NAT oder OSPF behandeln alle Schnittstellentypen auf ähnliche Weise. Im Hinblick auf die Implementierung kann eine Schnittstelle jedoch eine dedizierte Verbindung (z. B. mit einem Lan (Local Area Network) oder eine nicht dedizierte DFÜ-Verbindung (z. B. eine VERBINDUNG MIT EINEM WIDE AREA NETWORK (WAN)) darstellen.

Im Fall einer LAN-Schnittstelle entspricht die Schnittstelle einem tatsächlichen physischen Gerät auf dem Computer, einem LAN-Adapter. Im Fall einer WAN-Schnittstelle wird die Schnittstelle einem Port zugeordnet, wenn eine Verbindung hergestellt wird. Der Port kann ein COM-Port, ein paralleler Port oder ein virtueller Port (für Tunnel wie PPTP und L2TP) sein.

WAN-Schnittstellen haben die zusätzliche Qualität, dass sie in der Regel eine Netzwerkadresse nur zu dem Zeitpunkt erhalten, zu dem eine Verbindung hergestellt wird. Beispielsweise empfängt eine WAN-Schnittstelle mitHILFE von NOTE während des Verbindungsprozesses die Netzwerkschichtadresse vom Remote-Peer. Das Empfangen einer Netzwerkadresse im Rahmen des Verbindungsprozesses wird manchmal als *späte Bindung bezeichnet.*

 

 




