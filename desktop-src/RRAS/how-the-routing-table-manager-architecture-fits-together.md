---
title: Wie die Routingtabellen-Manager-Architektur zusammenpasst
description: Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1637eed71a89a6de4fa7dad6a4fea4a5918366f69ee05a490824699605a117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791384"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Wie die Routingtabellen-Manager-Architektur zusammenpasst

Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.

![Beziehung zwischen Routerkomponenten](images/rtsrvarch.png)

Beim Bootstrapping des Routers wird der Router-Manager-Dienst sowie mindestens ein Routingprotokoll gestartet. Routingprotokolle werden den verschiedenen Schnittstellen auf dem Router zugeordnet. Der Router-Manager startet auch den Routingtabellen-Manager.

Die folgende Abbildung zeigt die Beziehung zwischen Clients und den verschiedenen Komponenten des Routingtabellen-Managers.

![Beziehung zwischen Clients und Komponenten des Routingtabellen-Managers](images/rtmentrel.png)

Der Router-Manager startet eine oder mehrere Instanzen des Routingtabellen-Managers. Wenn mehrere Instanzen des Routingtabellen-Managers gestartet werden, wurde der Router so konfiguriert, dass er als ein oder mehrere virtuelle Router fungiert. Jede Instanz des Routingtabellen-Managers besitzt mindestens eine Schnittstelle. Jede Schnittstelle kann sich nur im Besitz einer Instanz des Routingtabellen-Managers befinden.

Jede Instanz des Routingtabellen-Managers ist unabhängig von den anderen. zwischen den Instanzen werden keine Informationen ausgetauscht.

Jede Instanz des Routingtabellen-Managers enthält mindestens eine Routingtabelle. Jede Routingtabelle ist einer Adressfamilie zugeordnet.

Jede Routingtabelle enthält eine oder mehrere Ansichten. In diesem Beispiel wird die Routingtabelle mit einer Unicast- und Multicastansicht angezeigt. Jede Sicht ist eine Teilmenge der Routingtabelle.

Die folgende Abbildung zeigt die Beziehung zwischen Clients und mehreren Instanzen des Routingtabellen-Managers, routingtabellen und sichten.

![Beziehungsclients, Routingtabellen-Manager, Routingtabellen, Sichten](images/multrtabrel.png)

Eine Instanz des Clients kann mehrmals bei einer Instanz des Routingtabellen-Managers registriert werden – einmal pro Adressfamilie. Ein Client kann sich bei jeder Instanz des Routingtabellen-Managers registrieren.

Die folgende Abbildung zeigt, wie die Routingtabelleneinträge verknüpft sind. Weitere Informationen zu Routingtabelleneinträgen finden Sie unter [Routingtabelleneinträge.](routing-table-entries.md)

![Beziehung zwischen Routingtabelleneinträgen](images/nexthop.png)

Die Routingtabelle enthält Ziele. Jedes Ziel bezieht sich auf eine oder mehrere Routen. Jede Route weist null, einen oder mehrere Zeiger auf die nächsten Hops auf, die der Route zugeordnet sind. Jeder Zeiger bezieht sich auf den tatsächlichen nächsten Hop in der Liste der nächsten Hops. Jeder Client, der sich beim Routingtabellen-Manager registriert, erstellt eine Liste der nächsten Hops, die der Client besitzt.

Routen können nur Zeiger auf die Liste des nächsten Hops enthalten, die dem Client zugeordnet ist, der die Route besitzt.

 

 




