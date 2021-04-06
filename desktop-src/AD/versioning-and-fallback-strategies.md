---
title: Versionierung und Fall Back Strategien
description: Wenn eine Anwendung eine partielle Aktualisierung mithilfe eines der oben genannten Verfahren erkennt oder einen Satz von Objekten liest, deren Gültigkeitsdatum noch nicht erreicht wurde, muss die Anwendung die Situation ordnungsgemäß behandeln.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Versionsverwaltung und Fall Back Strategien AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855379"
---
# <a name="versioning-and-fallback-strategies"></a>Versionierung und Fall Back Strategien

Wenn eine Anwendung eine partielle Aktualisierung mithilfe eines der oben genannten Verfahren erkennt oder einen Satz von Objekten liest, deren Gültigkeitsdatum noch nicht erreicht wurde, muss die Anwendung die Situation ordnungsgemäß behandeln. Bei manchen Anwendungen ist die ordnungsgemäße Reaktion auf eine frühere Version der fraglichen Objekte. Active Directory Domain Services keine Funktionen zur Versionsverwaltung bereitstellen – Anwendungen, die diese Funktion verwenden möchten, müssen Sie selbst bereitstellen. Zu den Ansätzen bei der Versionsverwaltung gehört das lokale beibehalten der "zuletzt bekannten guten" Werte, die lokal zwischengespeichert sind, und das Speichern mehrerer Objekt Sätze im Verzeichnis, z. b. in "alten", "aktuellen" und "neuen" Containern. Viele andere Schemas sind möglich.

Implementierungen müssen darauf achten, unbeabsichtigte Folgen zu vermeiden. Eine frühere Version von Objekten sollte nur verwendet werden, wenn ein Teil Update erkannt wird oder die neuen Objekte noch nicht "wirksam" sind. Ein Fallback, da etwas in der Anwendung nicht funktioniert, kann die Absicht eines Administrators umgehen. Beispielsweise kann es vorkommen, dass zwei Computer, die zuvor kommunizieren konnten, aufgrund einer Änderung der IPSec-Richtlinie (Internet Protocol Security, Internet Protokoll Sicherheit) dies möglicherweise nicht möglich war. Wenn dies auf dem Administrator Administrator beabsichtigt ist, sollten die betroffenen Systeme nicht auf die Richtlinie zurückgreifen, die Ihnen die Kommunikation gestattet, da dies eine Sicherheitsverletzung wäre.

 

 




