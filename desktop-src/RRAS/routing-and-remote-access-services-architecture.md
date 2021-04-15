---
title: Architektur der Routing-und RAS-Dienste
description: Die folgende Abbildung zeigt eine allgemeine Architektur Ansicht des Windows 2000-Routers.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- RRAS-, Routing-und RAS-Dienst Architektur-RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471516"
---
# <a name="routing-and-remote-access-services-architecture"></a>Architektur der Routing-und RAS-Dienste

Die folgende Abbildung zeigt eine allgemeine Architektur Ansicht des Windows 2000-Routers.

Komponenten, die für die IP-Protokollfamilie spezifisch sind, werden hellgrau dargestellt. Komponenten, die für die IPX-Protokollfamilie spezifisch sind, werden in dunkelgrau dargestellt. Komponenten, die allgemein für alle Protokoll Familien gelten, sind schattiert.

Der Routing-und RAS-Dienst stellt APIs zum Verwalten und Konfigurieren des-Dienstanbieter bereit. Diese APIs enthalten SNMP-Agents sowohl für IP als auch für IPX.

RRAS umfasst Routing Protokolle sowohl für IP als auch für IPX. Bei IP stellt RRAS das Routing Information-Protokoll (RIP) und Open kürzeste Path First (OSPF)-Routing Protokolle bereit. Für IPX stellt RRAS das IPX-RIP-und Service Advertising-Protokoll (SAP) bereit.

RRAS verwendet einen Routing Tabellen-Manager (RTM) sowohl für IP als auch für IPX. Jede Protokollfamilie verfügt jedoch über einen eigenen routermanager. RRAS verfügt auch über eine separate Komponente zum Verwalten von Multicast Gruppen.

Die Schnittstellen von Dynamic Interface Manager (Dim) mit PPP-und TAPI-Diensten zur Verwaltung von PPP-Schnittstellen, die von einigen Routen verwendet werden.

![allgemeine Architektur Ansicht des Windows 2000-Routers](images/rtarch.png)

 

 




