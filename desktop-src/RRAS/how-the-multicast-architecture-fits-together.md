---
title: Kombinieren der Multicast Architektur
description: In diesem Abschnitt wird eine Beispielkonfiguration und die Kombinieren der Hauptkomponenten beschrieben.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207003"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Kombinieren der Multicast Architektur

In diesem Abschnitt wird eine Beispielkonfiguration und die Kombinieren der Hauptkomponenten beschrieben.

Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.

![Beziehung zwischen Komponenten des Windows 2000-Routers](images/mrarch1.png)

Der Multicast-Gruppen-Manager ist Teil des RRAS-Dienstanbieter, der auf einem Server ausgeführt wird, der als Router betrieben wird.

Der angezeigte Router verfügt über drei Multicast Routing Protokolle (Protokoll 1, Protokoll 2, Protokoll 3), die darauf ausgeführt werden. Jedes Protokoll kann eine oder mehrere Schnittstellen besitzen (in dieser Abbildung besitzt Protokoll 1 Schnittstelle 1, Protokoll 2 besitzt Schnittstelle 2, und Protokoll 3 besitzt Schnittstelle 3). Jede Schnittstelle kann nur im Besitz eines Routing Protokolls sein (zusätzlich zu IGMP, was ein Sonderfall ist).

Der Multicast-Gruppen-Manager wird auf dem Router ausgeführt und koordiniert die Verteilung der Gruppeninformationen zwischen den Routing Protokollen.

Die folgende Abbildung zeigt die Beziehung zwischen zwei Routern in einer Multicast Architektur.

![Beziehung zwischen zwei Routern in der Multicast Architektur](images/mrarch2.png)

In der vorherigen Abbildung sendet Router 2 eine Multicast Nachricht an Netzwerk 2 an Schnittstelle 3. Router 1 empfängt die Multicast Nachricht von Netzwerk 2 an Schnittstelle 3. Auf beiden Routern besitzt Protokoll 3 die jeweilige Schnittstelle 3.

Die folgende Abbildung zeigt den Pfad einer Nachricht von einer Multicast Quelle (an eine Multicast Gruppe), um den Host zu erreichen, der der Multicast Gruppe beigetreten ist. Die Router in der Abbildung verwenden die gleiche Konfiguration wie vorherige Abbildungen. die Schnittstellen-und Protokoll Details werden jedoch nicht angezeigt, um die Abbildung einfach zu halten.

![der Pfad der Nachricht von der Multicast Quelle zum Zielhost.](images/mrarch3.png)

Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn ein Host einer Multicast Gruppe Beitritt. Informationen zu den Beziehungen zwischen den verschiedenen Entitäten finden Sie in der vorherigen Abbildung.

1.  Host 1 wird der Multicast Gruppe G in Netzwerk 3 beitreten.
2.  Router 3 erfährt ungefähr G über IGMP.
3.  Der Multicast-Gruppen-Manager auf Router 3 benachrichtigt Protokoll 3 auf Router 3, dass neue Empfänger für G vorhanden sind.
4.  Protokoll 3 auf Router 3 benachrichtigt dann Protokoll 3 auf Router 1 über G.
5.  Das Protokoll 3 auf Router 1 benachrichtigt wiederum den Multicast-Gruppen-Manager auf Router 1 über G.
6.  Der Multicast-Gruppen-Manager auf Router 1 benachrichtigt dann Protokoll 1 und Protokoll 2 über G.
7.  In Protokoll 2 kann Router 2 über G informiert werden, wenn das Protokoll dafür konzipiert ist.

Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn eine Nachricht an eine Multicast Gruppe gesendet wird. Informationen zu den Beziehungen zwischen den verschiedenen Entitäten finden Sie in der vorherigen Abbildung.

1.  Eine Quelle in Netzwerk 1 sendet eine Nachricht an die Gruppe G.
2.  Die von Quelldateien gesendete Nachricht wechselt zunächst zu Router 2, der Sie dann mithilfe von Schnittstelle 2 an Router 1 weiterleitet (da Router 2 von Protokoll 2 informiert wurde, dass Empfänger nach dem downstreamvorhanden sind).
3.  Router 1 leitet die Nachricht an Router 3 weiter (da Router 1 von Protokoll 2 informiert wurde, dass die Empfänger nach dem Downstreamdienst vorhanden sind).
4.  Router 3 leitet die Nachricht an Netzwerk 3 weiter und wird daher bei Host 1 eintreffen.

Weitere Informationen zur Multicast Routing Protokoll-Interaktion finden Sie unter [RFC 2715](routing-protocols-request-for-comments.md), Interoperabilitäts Regeln für Multicast Routing Protokolle.

 

 




