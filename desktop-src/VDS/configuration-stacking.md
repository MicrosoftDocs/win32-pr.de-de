---
description: Konfigurations Stapel
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Konfigurations Stapel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554710"
---
# <a name="configuration-stacking"></a><span data-ttu-id="23a81-103">Konfigurations Stapel</span><span class="sxs-lookup"><span data-stu-id="23a81-103">Configuration Stacking</span></span>

<span data-ttu-id="23a81-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="23a81-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="23a81-105">Das Stapeln umfasst die Verkettung eines Satzes logischer Block Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="23a81-105">Stacking involves the concatenating of a set of logical block mappings.</span></span> <span data-ttu-id="23a81-106">Sie können mehrere LUNs aus demselben Subsystem in einer LUN stapeln.</span><span class="sxs-lookup"><span data-stu-id="23a81-106">You can stack multiple LUNs from the same subsystem under one LUN.</span></span> <span data-ttu-id="23a81-107">Sie können eine LUN mit Volumes aus demselben Paket unter einem Volume stapeln.</span><span class="sxs-lookup"><span data-stu-id="23a81-107">You can stack a LUN together with volumes from the same pack under one volume.</span></span> <span data-ttu-id="23a81-108">Außerdem können Sie mehrere LUNs Stapeln, die von heterogenen Subsystemen unter einem Volume angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="23a81-108">Further, you can stack multiple LUNs that are surfaced by heterogeneous subsystems under one volume.</span></span>

<span data-ttu-id="23a81-109">Wie in der folgenden Abbildung gezeigt, wird durch das Erstellen eines Volumes die vorhandene Bindung einer Beitragenden LUN nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="23a81-109">As the following illustration shows, the creating of a volume does not change the existing binding of a contributing LUN.</span></span> <span data-ttu-id="23a81-110">Ebenso wird durch die Bindung eines Volumes nicht die Bindung einer Beitragenden LUN aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="23a81-110">Similarly, the unbinding of a volume does not unbind a contributing LUN.</span></span> <span data-ttu-id="23a81-111">Die Abbildung zeigt die RAID 0 1 (0 + 1)-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="23a81-111">The illustration depicts the RAID 0 1 (0+1) configuration.</span></span> <span data-ttu-id="23a81-112">Diese bekannte Konfiguration kombiniert Striping (RAID 0) und Spiegelung (RAID 1), die den schnellen Datenzugriff von RAID 0 mit der Zuverlässigkeit von RAID 1 verbindet.</span><span class="sxs-lookup"><span data-stu-id="23a81-112">This well-known configuration combines striping (RAID 0) and mirroring (RAID 1), which pairs the fast data access of RAID 0 with the reliability of RAID 1.</span></span>

![Diagramm, das eine RAID 0 1 (0 + 1)-Konfiguration anzeigt.](images/vdsstacklunvolzeroplusone.png)

<span data-ttu-id="23a81-114">Beitragende LUNs können unterschiedliche Bindungs Typen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="23a81-114">Contributing LUNs can have different binding types.</span></span> <span data-ttu-id="23a81-115">Viele Konfigurationen sind mit VDS möglich, sind aber sehr unwahrscheinlich, wie z. b. in der nächsten Abbildung.</span><span class="sxs-lookup"><span data-stu-id="23a81-115">Many configurations are possible with VDS but are highly unlikely, such as the next illustration.</span></span> <span data-ttu-id="23a81-116">In diesem Beispiel ist ein Volume Plex eine stripesetlun und die andere eine drei-Wege-gespiegelte LUN.</span><span class="sxs-lookup"><span data-stu-id="23a81-116">In this example, one volume plex is a striped LUN and the other is a three-way mirrored LUN.</span></span>

![Diagramm, das eine VDS-Konfiguration anzeigt, bei der ein Volume Plex eine stripesetlun und die andere eine 3-Wege-gespiegelte LUN ist.](images/vdsstacklunvol.png)

<span data-ttu-id="23a81-118">Obwohl dieses Beispiel nicht praktikabel ist, wird ein wichtiger Aspekt beim Stapeln veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="23a81-118">Although impractical, this example illustrates an important aspect of stacking.</span></span> <span data-ttu-id="23a81-119">Da das Stapeln verkettet, fügt VDS die drei LUN-plexes den beiden volumeplexen für insgesamt fünf plexes hinzu.</span><span class="sxs-lookup"><span data-stu-id="23a81-119">Because stacking concatenates plexes, VDS adds the three LUN plexes to the two volume plexes for a total of five plexes.</span></span>

 

 
