---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Der Datei Replikations Dienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360570"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="b3de7-103">Der Datei Replikations Dienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet</span><span class="sxs-lookup"><span data-stu-id="b3de7-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="b3de7-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="b3de7-104">Platform</span></span>

 <span data-ttu-id="b3de7-105">**Server:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3de7-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="b3de7-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="b3de7-106">Feature Impact</span></span>

 <span data-ttu-id="b3de7-107">**Schweregrad:** Hochrangiger</span><span class="sxs-lookup"><span data-stu-id="b3de7-107">**Severity -** High</span></span>  
<span data-ttu-id="b3de7-108">**Häufigkeit:** Hochrangiger</span><span class="sxs-lookup"><span data-stu-id="b3de7-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="b3de7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3de7-109">Description</span></span>

<span data-ttu-id="b3de7-110">In Windows Server 2008 R2 kann der Datei Replikations Dienst (File Replication Service, FRS) nicht zum Replizieren von verteiltes Dateisystem Ordner (DFS) oder benutzerdefinierten Daten (nicht-SYSVOL) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3de7-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="b3de7-111">Ein Windows Server 2008 R2-Domänen Controller kann weiterhin FRS zum Replizieren des Inhalts der SYSVOL-Freigabe in einer Domäne verwenden, die FRS zum Replizieren der SYSVOL-Freigabe zwischen Domänen Controllern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3de7-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="b3de7-112">Windows Server 2008 R2-Server können FRS jedoch nicht verwenden, um den Inhalt einer Replikat Gruppe außer der SYSVOL-Freigabe zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="b3de7-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="b3de7-113">Der DFS-Replikation-Dienst ist ein Ersatz für FRS und kann verwendet werden, um die Inhalte der SYSVOL-Freigabe, der DFS-Ordner und anderer benutzerdefinierter Daten (nicht-SYSVOL) zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="b3de7-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="b3de7-114">Migrieren Sie alle nicht-SYSVOL-FRS-Replikat Gruppen zu DFS-Replikation.</span><span class="sxs-lookup"><span data-stu-id="b3de7-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="b3de7-115">Außerdem wird dringend empfohlen, die Replikation der SYSVOL-Freigabe von FRS zu DFS-Replikation zu migrieren, da DFS-Replikation stabiler, skalierbar und eine bessere Replikations Leistung als FRS aufweist.</span><span class="sxs-lookup"><span data-stu-id="b3de7-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b3de7-116">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="b3de7-116">Manifestation</span></span>

<span data-ttu-id="b3de7-117">Die FRS-Replikation von benutzerdefinierten Daten wird bei einem direkten Upgrade unwiderruflich unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="b3de7-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="b3de7-118">Die einzige Möglichkeit, diese Situation zu beheben, besteht darin, ein älteres Betriebssystem auf dem Server neu zu installieren und die FRS-Replikation erneut zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b3de7-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="b3de7-119">Server, die auf Windows Server 2008 R2 aktualisiert wurden, dürfen nicht an vorhandenen FRS-Replikations Gruppen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="b3de7-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="b3de7-120">Minderung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="b3de7-120">Mitigation of Impact</span></span>

<span data-ttu-id="b3de7-121">Um Probleme zu vermeiden, die möglicherweise aufgrund dieser Änderungen auftreten, migrieren Sie benutzerdefinierte FRS-Replikations Gruppen zu DFS-Replikation.</span><span class="sxs-lookup"><span data-stu-id="b3de7-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="b3de7-122">Der DFS-Replikation-Dienst hat gegenüber FRS viele Vorteile, einschließlich verbesserter Verwaltungs Tools, höherer Leistung und Delegierter Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="b3de7-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b3de7-123">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b3de7-123">Links to Other Resources</span></span>

-   <span data-ttu-id="b3de7-124">[FRS (Übersicht)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="b3de7-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="b3de7-125">DFS-Replikation: Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="b3de7-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="b3de7-126">Anleitung zur SYSVOL-Replikationsmigration: FRS- zu DFS-Replikation</span><span class="sxs-lookup"><span data-stu-id="b3de7-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
