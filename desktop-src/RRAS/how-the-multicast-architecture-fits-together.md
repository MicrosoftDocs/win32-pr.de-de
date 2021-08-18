---
title: Wie die Multicastarchitektur zusammenpasst
description: In diesem Abschnitt werden eine Beispielkonfiguration und die Zusammenpassung der Hauptkomponenten beschrieben.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94f4ca79b9fdd6b2e2fd9e75dc61d780af4380ed958a491f69231f7d541f0aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791318"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Wie die Multicastarchitektur zusammenpasst

In diesem Abschnitt werden eine Beispielkonfiguration und die Zusammenpassung der Hauptkomponenten beschrieben.

Die folgende Abbildung zeigt die Beziehung zwischen den verschiedenen Komponenten eines Routers.

![Beziehung zwischen Komponenten des Windows 2000-Routers](images/mrarch1.png)

Der Multicastgruppen-Manager ist Teil des RRAS-Diensts, der auf einem Server ausgeführt wird, der als Router ausgeführt wird.

Auf dem angezeigten Router werden drei Multicastroutingprotokolle (Protokoll 1, Protokoll 2, Protokoll 3) ausgeführt. Jedes Protokoll kann eine oder mehrere Schnittstellen besitzen (in dieser Abbildung besitzt Protokoll 1 Schnittstelle 1, Protokoll 2 besitzt Schnittstelle 2 und Protokoll 3 besitzt Schnittstelle 3). Jede Schnittstelle kann nur einem Routingprotokoll gehören (zusätzlich zu IGMP, was ein Sonderfall ist).

Der Multicastgruppen-Manager wird auf dem Router ausgeführt und koordiniert die Verteilung von Gruppeninformationen zwischen den Routingprotokollen.

Die folgende Abbildung zeigt die Beziehung zwischen zwei Routern in einer Multicastarchitektur.

![Beziehung zwischen zwei Routern in der Multicastarchitektur](images/mrarch2.png)

In der vorherigen Abbildung sendet Router 2 eine Multicastnachricht an Netzwerk 2 an Schnittstelle 3. Router 1 empfängt die Multicastnachricht von Netzwerk 2 an Schnittstelle 3. Auf beiden Routern besitzt Protokoll 3 die entsprechende Schnittstelle 3.

Die folgende Abbildung zeigt den Pfad, den eine Nachricht von einer Multicastquelle (zu einer Multicastgruppe) nimmt, um den Host zu erreichen, der der Multicastgruppe beigetreten ist. Die Router in der Abbildung verwenden die gleiche Konfiguration wie vorherige Abbildungen. Die Schnittstellen- und Protokolldetails werden jedoch nicht angezeigt, um die Abbildung einfach zu halten.

![Pfad der Nachricht von der Multicastquelle zum Zielhost](images/mrarch3.png)

Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn ein Host einer Multicastgruppe beitritt. In der vorherigen Abbildung finden Sie Beziehungen zwischen den verschiedenen Entitäten.

1.  Host 1 tritt der Multicastgruppe G in Netzwerk 3 bei.
2.  Router 3 lernt über G über IGMP.
3.  Der Multicastgruppen-Manager auf Router 3 benachrichtigt Protokoll 3 auf Router 3, dass es neue Empfänger für G gibt.
4.  Protokoll 3 auf Router 3 benachrichtigt dann Protokoll 3 auf Router 1 über G.
5.  Im Gegenzug benachrichtigt Protokoll 3 auf Router 1 den Multicastgruppen-Manager auf Router 1 über G.
6.  Der Multicastgruppen-Manager auf Router 1 benachrichtigt dann Protokoll 1 und Protokoll 2 über G.
7.  Protokoll 2 informiert Router 2 möglicherweise über G, wenn das Protokoll dafür konzipiert ist.

Im folgenden Szenario werden die Ereignisse beschrieben, die stattfinden, wenn eine Nachricht an eine Multicastgruppe gesendet wird. Informationen zu den Beziehungen zwischen den verschiedenen Entitäten finden Sie in der vorherigen Abbildung.

1.  Eine Quelle in Netzwerk 1 sendet eine Nachricht an Gruppe G.
2.  Die von Quelle S gesendete Nachricht wird zuerst an Router 2 gesendet, der sie dann über Schnittstelle 2 an Router 1 weitersandt (da Router 2 durch Protokoll 2 darüber informiert wurde, dass Empfänger nachgeschaltet sind).
3.  Router 1 weitergeleitet die Nachricht an Router 3 (da Router 1 durch Protokoll 2 darüber informiert wurde, dass Empfänger nachgeschaltet sind).
4.  Router 3 gibt die Nachricht an Netzwerk 3 weiter und trifft daher auf Host 1 ein.

Weitere Informationen zur Multicastroutingprotokollinteraktion finden Sie unter [RFC 2715](routing-protocols-request-for-comments.md), Interoperabilitätsregeln für Multicastroutingprotokolle.

 

 




