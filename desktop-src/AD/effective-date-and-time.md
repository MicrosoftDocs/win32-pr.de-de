---
title: Gültigkeitsdatum und Uhrzeit
description: Das Gültigkeitsdatum und die Uhrzeit sind eine Vermeidungsstrategie, die eine Versions Abweichung und partielle Updates verhindert, indem die effektiven Daten von Informationen zu einem späteren Zeitpunkt verzögert werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, dass Sie vollständig repliziert wird.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036378"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="4ef2e-103">Gültigkeitsdatum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="4ef2e-103">Effective Date and Time</span></span>

<span data-ttu-id="4ef2e-104">Das Gültigkeits *Datum und die Uhrzeit* sind eine Vermeidungsstrategie, die eine Versions Abweichung und partielle Updates verhindert, indem die effektiven Daten von Informationen zu einem späteren Zeitpunkt verzögert werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, dass Sie vollständig repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="4ef2e-105">Zum Implementieren von Gültigkeitsdatums Angaben müssen die Anwendungs Objekte einen Gültigkeitsdatum-Zeitstempel enthalten, der ausgefüllt wird, wenn das Objekt erstellt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="4ef2e-106">Consumer der Objekte überprüfen den Zeitstempel und verzögern die Verwendung der Objekte, bis das Datum und die Uhrzeit erreicht sind.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="4ef2e-107">Wichtige Hinweise:</span><span class="sxs-lookup"><span data-stu-id="4ef2e-107">Some important considerations:</span></span>

-   <span data-ttu-id="4ef2e-108">Anwendungen, die diesen Ansatz auswählen, müssen sicherstellen, dass es eine Reihe von anwendbaren Daten gibt, die verwendet werden können, bis die aktualisierten Objekte wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="4ef2e-109">Der verteilte Zeit Dienst in Windows NT 4,0 sorgt dafür, dass die Uhren der verbundenen Windows 2000 synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="4ef2e-110">Es ist jedoch kein Zeit-Dienst perfekt, es gibt also ein kleines Fenster für die Versions Neigung.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="4ef2e-111">Wenn Sie ein gutes Gültigkeitsdatum festlegen, werden die Gesamt Replikations Latenz für das betreffende verteilte System vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="4ef2e-112">Eine gute Faustregel für Gültigkeits Daten in einem stabilen Netzwerk ist die (Uhrzeit des Updates) + (2 \* (durchschnittliche Gesamt Latenz)).</span><span class="sxs-lookup"><span data-stu-id="4ef2e-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="4ef2e-113">Bei einem System, dessen Gesamt Latenz durchschnittlich 4 Stunden beträgt, ist also eine Verzögerung von 8 Stunden angemessen.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="4ef2e-114">In einem instabilen Netzwerk ist das Ermitteln eines "guten" Werts für effektive Datumsangaben sehr viel schwieriger, da die Latenz stark variabel sein kann.</span><span class="sxs-lookup"><span data-stu-id="4ef2e-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="4ef2e-115">Das Gültigkeitsdatum ist in einem instabilen Netzwerk in der Kombination mit anderen Vermeidungs-oder Erkennungs Strategien, wie z. b. Prüfsummen oder Konsistenz-GUIDs, die höchste Wirksamkeit</span><span class="sxs-lookup"><span data-stu-id="4ef2e-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="4ef2e-116">Weitere Informationen finden Sie unter [Prüfsummen und Objekt Anzahl](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="4ef2e-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




