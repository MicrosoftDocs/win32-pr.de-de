---
description: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088368"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="7142a-103">Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.</span><span class="sxs-lookup"><span data-stu-id="7142a-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="7142a-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="7142a-104">Platform</span></span>

 <span data-ttu-id="7142a-105">**Server :** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7142a-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="7142a-106">Auswirkungen auf Features</span><span class="sxs-lookup"><span data-stu-id="7142a-106">Feature Impact</span></span>

 <span data-ttu-id="7142a-107">**Schweregrad:** Hoch</span><span class="sxs-lookup"><span data-stu-id="7142a-107">**Severity -** High</span></span>  
<span data-ttu-id="7142a-108">**Häufigkeit:** Hoch</span><span class="sxs-lookup"><span data-stu-id="7142a-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="7142a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7142a-109">Description</span></span>

<span data-ttu-id="7142a-110">In Windows Server 2008 R2 kann der Dateireplikationsdienst (File Replication Service, FRS) nicht zum Replizieren von DFS-Ordnern (verteiltes Dateisystem) oder benutzerdefinierten Daten (nicht SYSVOL) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7142a-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="7142a-111">Ein Windows Server 2008 R2-Domänencontroller kann frs weiterhin verwenden, um den Inhalt der SYSVOL-Freigabe in einer Domäne zu replizieren, die FRS zum Replizieren der SYSVOL-Freigabe zwischen Domänencontrollern verwendet.</span><span class="sxs-lookup"><span data-stu-id="7142a-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="7142a-112">Windows Server 2008 R2-Server können frs jedoch nicht verwenden, um den Inhalt eines Replikats zu replizieren, das sich von der SYSVOL-Freigabe unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="7142a-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="7142a-113">Der DFS-Replikation Dienst ist ein Ersatz für FRS und kann verwendet werden, um den Inhalt der SYSVOL-Freigabe, der DFS-Ordner und anderer benutzerdefinierter Daten (nicht SYSVOL) zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="7142a-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="7142a-114">Migrieren Sie alle Nicht-SYSVOL FRS-Replikatgruppen zu DFS-Replikation.</span><span class="sxs-lookup"><span data-stu-id="7142a-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="7142a-115">Es wird außerdem dringend empfohlen, die Replikation der SYSVOL-Freigabe von FRS zu DFS-Replikation zu migrieren, da DFS-Replikation stabiler, skalierbarer und eine bessere Replikationsleistung als FRS bietet.</span><span class="sxs-lookup"><span data-stu-id="7142a-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7142a-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="7142a-116">Manifestation</span></span>

<span data-ttu-id="7142a-117">Die FRS-Replikation benutzerdefinierter Daten unterbricht nach einem unmittelbaren Upgrade unumkehrbar.</span><span class="sxs-lookup"><span data-stu-id="7142a-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="7142a-118">Die einzige Möglichkeit zur Wiederherstellung aus dieser Situation wäre die Neuinstallation eines älteren Betriebssystems auf dem Server und das erneute Initialisieren der FRS-Replikation.</span><span class="sxs-lookup"><span data-stu-id="7142a-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="7142a-119">Server, die auf Windows Server 2008 R2 aktualisiert wurden, dürfen nicht an vorhandenen FRS-Replikationsgruppen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="7142a-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="7142a-120">Entschärfung der Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="7142a-120">Mitigation of Impact</span></span>

<span data-ttu-id="7142a-121">Um Probleme zu vermeiden, die aufgrund dieser Änderungen auftreten können, migrieren Sie benutzerdefinierte FRS-Replikationssätze zu DFS-Replikation.</span><span class="sxs-lookup"><span data-stu-id="7142a-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="7142a-122">Der DFS-Replikation-Dienst bietet gegenüber FRS viele Vorteile, einschließlich verbesserter Verwaltungstools, höherer Leistung und delegierter Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="7142a-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7142a-123">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7142a-123">Links to Other Resources</span></span>

-   <span data-ttu-id="7142a-124">[ÜBERSICHT ÜBER FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="7142a-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="7142a-125">DFS-Replikation: Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="7142a-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="7142a-126">Anleitung zur SYSVOL-Replikationsmigration: FRS- zu DFS-Replikation</span><span class="sxs-lookup"><span data-stu-id="7142a-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
