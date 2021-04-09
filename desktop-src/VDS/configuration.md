---
description: Konfigurations Übersicht
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Konfigurations Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958860"
---
# <a name="configuration-overview"></a><span data-ttu-id="af77a-103">Konfigurations Übersicht</span><span class="sxs-lookup"><span data-stu-id="af77a-103">Configuration Overview</span></span>

<span data-ttu-id="af77a-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="af77a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="af77a-105">Wenn Sie mit den von VDS definierten Objekten nicht vertraut sind, lesen Sie das [VDS-Objektmodell](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="af77a-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="af77a-106">Die Konfigurations Komplexität eines virtuellen Datenträgers kann von sehr einfach bis fein optimiert reichen.</span><span class="sxs-lookup"><span data-stu-id="af77a-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="af77a-107">Die virtuellen Datenträger "keine Sorgfalt", "kostenlos" und "Enterprise" definieren drei typische Konfigurations Perspektiven.</span><span class="sxs-lookup"><span data-stu-id="af77a-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="af77a-108">Jede Perspektive weist etwas andere Anforderungen auf:</span><span class="sxs-lookup"><span data-stu-id="af77a-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="af77a-109">Virtuelle Datenträger ohne Sorgfalt sind leicht zu konfigurieren, vielleicht nur zur Automatisierung der Partitionierung und Formatierung neuer Datenträger oder zum vorübergehenden Erstellen eines gespiegelten Volumes für die Migration von Daten von einem Datenträger zu einem anderen ohne Ausfallzeiten.</span><span class="sxs-lookup"><span data-stu-id="af77a-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="af77a-110">Solche Datenträger eignen sich für Notebook-Computer und andere Systeme mit einem oder wenigen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="af77a-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="af77a-111">Virtuelle Datenträger mit freiem Speicherplatz bieten Speicher, der selbst konfigurierend, Selbstreparatur und verfügbar erscheint. verwendet Stripesetvolumes und LUNs, um eine bessere Leistung zu erzielen. verwendet gespiegelte Volumes und LUNs, um eine bessere Verfügbarkeit zu erzielen. und verwendet Pakete, um die Fehlermodi zu bereinigen und zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="af77a-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="af77a-112">Diese Konfigurations Ebene ist ideal, wenn Sie alte, kleine, langsame System Datenträger durch neue, große, schnelle Datenträger ersetzen.</span><span class="sxs-lookup"><span data-stu-id="af77a-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="af77a-113">Sie eignet sich außerdem ideal für die Spiegelung von Daten mit automatischem hotsparsam – mit einer einzelnen Ersatz Spindel können viele Spindeln geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="af77a-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="af77a-114">Weitere Informationen finden Sie unter [Hot sparsam](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="af77a-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="af77a-115">Kleine Sans sind abhängig von der Flexibilität und Automatisierung, die von dieser Konfigurations Ebene angeboten wird, wie NAS-Geräte (Network Attached Storage).</span><span class="sxs-lookup"><span data-stu-id="af77a-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="af77a-116">Virtuelle Datenträger ohne Datenträger vereinfachen die Konsolidierung des Anwendungs Speichers – z. b. den Speicher für SQL und Exchange – ohne die Server zu konsolidieren.</span><span class="sxs-lookup"><span data-stu-id="af77a-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="af77a-117">Virtuelle Enterprise-Datenträger enthalten sehr große oder komplexe Unternehmens Konfigurationen mit zusätzlichen standortspezifischen oder anwendungsspezifischen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="af77a-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="af77a-118">Administratoren optimieren das Speichersubsystem für eine einzelne Anwendung, die nur selten ausgeführt werden kann, z. b. ein monatlicher Batch Berichterstattungs Auftrag in einem Transaktionssystem, der die Bestellung übernimmt.</span><span class="sxs-lookup"><span data-stu-id="af77a-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="af77a-119">Virtuelle Enterprise-Datenträger müssen skaliert werden, die Echt Zeit Aktivität des Speicher Subsystems anzeigen und die Anforderungen von praktischen Administratoren erfüllen.</span><span class="sxs-lookup"><span data-stu-id="af77a-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="af77a-120">Weitere Informationen zu spiegeln, Streifen und anderen Konfigurationsoptionen in VDS finden Sie unter [Volume-und LUN-Bindung](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="af77a-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="af77a-121">Mit einer erweiterten Konfigurations Methode, die als Stapeln bezeichnet wird, können Sie die Konfigurationen kombinieren, die vorhandenen Volumes und LUNs zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af77a-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="af77a-122">Weitere Informationen finden Sie unter [Konfigurations Stapel](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="af77a-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af77a-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af77a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af77a-124">Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="af77a-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="af77a-125">VDS-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="af77a-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="af77a-126">Heiß sparsam</span><span class="sxs-lookup"><span data-stu-id="af77a-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="af77a-127">Volume- und LUN-Bindung</span><span class="sxs-lookup"><span data-stu-id="af77a-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="af77a-128">Konfigurations Stapel</span><span class="sxs-lookup"><span data-stu-id="af77a-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
