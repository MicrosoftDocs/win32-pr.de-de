---
title: Warum Active Directory Domain Services dieses Replikations Modell verwendet
description: In diesem Thema werden die Gründe für das frei Form System erläutert, das von Active Directory Domain Services für ein Replikations Modell verwendet wird.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Replikations Modell Active Directory, Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855372"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="eda68-104">Warum Active Directory Domain Services dieses Replikations Modell verwendet</span><span class="sxs-lookup"><span data-stu-id="eda68-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="eda68-105">In diesem Thema werden die Gründe für das frei Form System erläutert, das von Active Directory Domain Services für ein Replikations Modell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eda68-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="eda68-106">Active Directory Domain Services sind aus folgenden Gründen ein frei Form System:</span><span class="sxs-lookup"><span data-stu-id="eda68-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="eda68-107">Kunden benötigen eine hochgradig verteilte Lösung, bei der Teile des Verzeichnisses auf Ihre Netzwerke verteilt und lokal verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="eda68-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="eda68-108">Große Kunden wachsen häufig auf Millionen von Objekten, Hunderte oder Tausende von Replikaten oder beides.</span><span class="sxs-lookup"><span data-stu-id="eda68-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="eda68-109">Viele Kunden Netzwerke bieten nur zeitweilig eine Verbindung zu einigen Standorten. Beispielsweise werden remoteöl-drillingplattformen und-Systeme auf dem Meeres System ausgeliefert, damit das System teilweise verbundene oder getrennte Vorgänge tolerieren muss.</span><span class="sxs-lookup"><span data-stu-id="eda68-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="eda68-110">Es gibt keine Möglichkeit, eine umfassende Kenntnis des aktuellen oder zukünftigen Zustands eines verteilten Systems zu gewährleisten, weil Informationen zu Zustandsänderungen weitergegeben werden müssen und die Weitergabe Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="eda68-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="eda68-111">Eng gekoppelte Systeme behandeln die Unsicherheit, indem Sie versuchen, Sie auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="eda68-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="eda68-112">Dies erfolgt durch Einschränkungen bei Updates, die erfordern, dass alle Knoten oder die Mehrzahl der Knoten verfügbar sind, bevor Updates durchgeführt werden können, indem verteilte Sperr Schemas verwendet werden oder ein Single-Mastering für kritische Ressourcen verwendet wird. Dadurch werden alle Knoten auf eine gute Verbindung beschränkt oder eine Kombination dieser Techniken.</span><span class="sxs-lookup"><span data-stu-id="eda68-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="eda68-113">Je stärker die Computer Knoten in einem verteilten System gekoppelt sind, desto niedriger ist die Skalierungs Grenze.</span><span class="sxs-lookup"><span data-stu-id="eda68-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="eda68-114">Frei Formsysteme behandeln die Unsicherheit, indem Sie Sie tolerieren.</span><span class="sxs-lookup"><span data-stu-id="eda68-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="eda68-115">Mit einem frei Form System können die Knoten unterschiedliche Ansichten des gesamten Systemstatus aufweisen und Algorithmen zum Auflösen von Konflikten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eda68-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="eda68-116">Eng gekoppelte Lösungen wurden aufgrund der Anforderungen an die lokale Verwaltung, den getrennten Betrieb und die Skalierbarkeit einer sehr großen Anzahl von Knoten als ungeeignet für Active Directory Domain Services zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="eda68-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="eda68-117">Das lose gekoppelte Modell, das von der multimasterlose Datenkonsistenz mit Konvergenz gewählt wurde, erfüllt alle Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="eda68-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




