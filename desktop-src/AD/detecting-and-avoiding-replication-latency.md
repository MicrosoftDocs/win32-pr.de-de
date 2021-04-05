---
title: Erkennen und vermeiden von Replikations Latenz
description: Die Replikations Latenz ist ein Fakt in einem locker gekoppelten verteilten System.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707721"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Erkennen und vermeiden von Replikations Latenz

Die Replikations Latenz ist ein Fakt in einem locker gekoppelten verteilten System. Anwendungen müssen dies aufnehmen. Die beste Möglichkeit für die Replikations Latenz ist das Entwerfen von Anwendungen, um die Auswirkungen zu minimieren. Die ideale, Verzeichnis aktivierte Anwendung:

-   Hat keine Unterscheidung zu Versions Schiefe.
-   Hängt nicht von Beziehungen zwischen mehreren Objekten ab.
-   Verfügt über keine internen oder Objekt übergreifenden Konsistenz Anforderungen.

Anwendungen und Dienste, die diesem Profil entsprechen, müssen sich nicht mit der Replikations Latenz beschäftigen. Andere Anwendungen müssen im Hinblick auf die Replikations Wartezeit entworfen werden. Der Schlüssel zum Erfolg beim Entwerfen einer solchen Anwendung ist das Bewusstsein des Replikations Prozesses. Schritte zur Entwurfszeit zum Reduzieren von Objekt übergreifenden Abhängigkeiten und minimieren von Teil Update Fenstern werden zur Laufzeit große Dividenden bezahlen. Ansätze zum Umgang mit Replikations Latenz sind in zwei Klassen unterteilt – Vermeidungsstrategien, die die Auswirkungen von Latenz und Erkennungs Strategien verringern, die es einer Anwendung ermöglichen, von der Latenz verursachende Zustände zu erkennen.

 

 




