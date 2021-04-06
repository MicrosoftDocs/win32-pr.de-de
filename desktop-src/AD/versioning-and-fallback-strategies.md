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
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="a9917-104">Versionierung und Fall Back Strategien</span><span class="sxs-lookup"><span data-stu-id="a9917-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="a9917-105">Wenn eine Anwendung eine partielle Aktualisierung mithilfe eines der oben genannten Verfahren erkennt oder einen Satz von Objekten liest, deren Gültigkeitsdatum noch nicht erreicht wurde, muss die Anwendung die Situation ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="a9917-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="a9917-106">Bei manchen Anwendungen ist die ordnungsgemäße Reaktion auf eine frühere Version der fraglichen Objekte.</span><span class="sxs-lookup"><span data-stu-id="a9917-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="a9917-107">Active Directory Domain Services keine Funktionen zur Versionsverwaltung bereitstellen – Anwendungen, die diese Funktion verwenden möchten, müssen Sie selbst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a9917-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="a9917-108">Zu den Ansätzen bei der Versionsverwaltung gehört das lokale beibehalten der "zuletzt bekannten guten" Werte, die lokal zwischengespeichert sind, und das Speichern mehrerer Objekt Sätze im Verzeichnis, z. b. in "alten", "aktuellen" und "neuen" Containern.</span><span class="sxs-lookup"><span data-stu-id="a9917-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="a9917-109">Viele andere Schemas sind möglich.</span><span class="sxs-lookup"><span data-stu-id="a9917-109">Many other schemes are possible.</span></span>

<span data-ttu-id="a9917-110">Implementierungen müssen darauf achten, unbeabsichtigte Folgen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a9917-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="a9917-111">Eine frühere Version von Objekten sollte nur verwendet werden, wenn ein Teil Update erkannt wird oder die neuen Objekte noch nicht "wirksam" sind.</span><span class="sxs-lookup"><span data-stu-id="a9917-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="a9917-112">Ein Fallback, da etwas in der Anwendung nicht funktioniert, kann die Absicht eines Administrators umgehen.</span><span class="sxs-lookup"><span data-stu-id="a9917-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="a9917-113">Beispielsweise kann es vorkommen, dass zwei Computer, die zuvor kommunizieren konnten, aufgrund einer Änderung der IPSec-Richtlinie (Internet Protocol Security, Internet Protokoll Sicherheit) dies möglicherweise nicht möglich war.</span><span class="sxs-lookup"><span data-stu-id="a9917-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="a9917-114">Wenn dies auf dem Administrator Administrator beabsichtigt ist, sollten die betroffenen Systeme nicht auf die Richtlinie zurückgreifen, die Ihnen die Kommunikation gestattet, da dies eine Sicherheitsverletzung wäre.</span><span class="sxs-lookup"><span data-stu-id="a9917-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




