---
title: Kombinieren der Architektur des Routing Tabellen-Managers
description: Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311592"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Kombinieren der Architektur des Routing Tabellen-Managers

Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.

![Beziehung zwischen Routerkomponenten](images/rtsrvarch.png)

Wenn der Router bootstrapped ist, wird der routermanager-Dienst sowie ein oder mehrere Routing Protokolle gestartet. Routing Protokolle werden den verschiedenen Schnittstellen auf dem Router zugeordnet. Der routermanager startet auch den Routing Tabellen-Manager.

Die folgende Abbildung zeigt die Beziehung zwischen Clients und den verschiedenen Komponenten des Routing Tabellen-Managers.

![Beziehung zwischen Clients und Komponenten des Routing Tabellen-Managers](images/rtmentrel.png)

Der routermanager startet eine oder mehrere Instanzen des Routing Tabellen-Managers. Wenn mehrere Instanzen des Routing Tabellen-Managers gestartet werden, wurde der Router so konfiguriert, dass er als ein oder mehrere virtuelle Router fungiert. Jede Instanz des Routing Tabellen-Managers besitzt mindestens eine Schnittstelle. jede Schnittstelle kann nur einer Instanz des Routing Tabellen-Managers gehören.

Jede Instanz des Routing Tabellen-Managers ist unabhängig von den anderen. zwischen den Instanzen werden keine Informationen ausgetauscht.

Jede Instanz des Routing Tabellen-Managers enthält eine oder mehrere Routing Tabellen. Jede Routing Tabelle ist einer Adressfamilie zugeordnet.

Jede Routing Tabelle enthält eine oder mehrere Ansichten. In diesem Beispiel wird die Routing Tabelle mit einer Unicast-und Multicast Ansicht angezeigt. Jede Ansicht ist eine Teilmenge der Routing Tabelle.

Die folgende Abbildung zeigt die Beziehung zwischen Clients und mehreren Instanzen des Routing Tabellen-Managers, Routing Tabellen und Sichten.

![Beziehungs Clients, Routing Tabellen-Manager, Routing Tabellen, Sichten](images/multrtabrel.png)

Eine Instanz des Clients kann mehrmals bei einer Instanz des Routing Tabellen-Managers registriert werden – einmal pro Adressfamilie. Ein Client kann sich bei jeder Instanz des Routing Tabellen-Managers registrieren.

In der folgenden Abbildung wird gezeigt, wie die Routing Tabelleneinträge verknüpft sind. Weitere Informationen zu Routing Tabellen Einträgen finden Sie unter [Routing Table Entries](routing-table-entries.md).

![Beziehung zwischen Routing Tabellen Einträgen](images/nexthop.png)

Die Routing Tabelle enthält Ziele. Jedes Ziel bezieht sich auf eine oder mehrere Routen. Jede Route verfügt über NULL, einen oder mehrere Zeiger auf die nächsten Hops, die der Route zugeordnet sind. Jeder Zeiger verweist auf den eigentlichen nächsten Hop in der Liste der nächsten Hops. Jeder Client, der beim Routing Tabellen-Manager registriert wird, erstellt eine Liste der nächsten Hops, die der Client besitzt.

Routen können nur Zeiger auf die Liste der nächsten Hops enthalten, die dem Client zugeordnet ist, der die Route besitzt.

 

 




