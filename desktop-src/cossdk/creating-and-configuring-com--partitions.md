---
description: Administratoren können com+ verwenden, um COM+-Partitionen Programm gesteuert zu erstellen und zu konfigurieren.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Erstellen und Konfigurieren von COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523560"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="455e2-103">Erstellen und Konfigurieren von COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="455e2-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="455e2-104">Administratoren können com+ verwenden, um COM+-Partitionen Programm gesteuert zu erstellen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="455e2-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="455e2-105">Tatsächlich können alle Erstellungs-und Konfigurationsaufgaben, die ein Administrator aus den Komponenten Diensten oder den Active Directory Verwaltungs Tools für Benutzer und Computer ausführen kann, mithilfe von com+-Sammlungen,-Objekten und-Schnittstellen oder über die Active Directory System Schnittstelle (ADSI) durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="455e2-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="455e2-106">**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="455e2-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="455e2-107">Die globale Partition ist die einzige verfügbare com+-Partition.</span><span class="sxs-lookup"><span data-stu-id="455e2-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="455e2-108">\* \* Windows 2000: \* \* der com+-Partitions Dienst ist in Windows 2000 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="455e2-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="455e2-109">Der com+-Partitions Dienst ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="455e2-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="455e2-110">Um den com+-Partitions Dienst zu verwenden, müssen Sie ihn über das Verwaltungs Tool Komponenten Dienste oder durch Ändern der partitionsenabled-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung auf true aktivieren.</span><span class="sxs-lookup"><span data-stu-id="455e2-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="455e2-111">Zum Ausführen von Partitions bezogenen Aufgaben bietet com+ die folgenden Programmier Elemente:</span><span class="sxs-lookup"><span data-stu-id="455e2-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="455e2-112">Methoden und Eigenschaften der [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle in der [**comadmincatalog**](comadmincatalog.md) -Klasse:</span><span class="sxs-lookup"><span data-stu-id="455e2-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="455e2-113">[**Currentpartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="455e2-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="455e2-114">[**Currentpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="455e2-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="455e2-115">[**Currentpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="455e2-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="455e2-116">[**Flushpartitioncache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) -Methode.</span><span class="sxs-lookup"><span data-stu-id="455e2-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="455e2-117">[**Getpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="455e2-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="455e2-118">[**Getpartitionname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) -Methode.</span><span class="sxs-lookup"><span data-stu-id="455e2-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="455e2-119">[**Globalpartitionid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="455e2-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="455e2-120">Eine Reihe von COM+-Objekten zum Erstellen und Verwalten von Partitionen in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="455e2-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="455e2-121">Ein com+-Registrierungsschlüssel, **partitioncache**, zum Ändern der Partitions Cache Größe.</span><span class="sxs-lookup"><span data-stu-id="455e2-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="455e2-122">Eine Reihe von Partitions bezogenen [com+-Verwaltungs Sammlungen](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="455e2-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="455e2-123">[**Partitionen**](partitions.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="455e2-124">[**Partitionusers**](partitionusers.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="455e2-125">[**Rolesforpartition**](rolesforpartition.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="455e2-126">[**Usersinpartitionrole**](usersinpartitionrole.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="455e2-127">Eigenschaften anderer [com+-Verwaltungs Sammlungen](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="455e2-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="455e2-128">PartitionID-Eigenschaft für die [**ApplicationInstance**](applicationinstances.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="455e2-129">Apppartitionid-Eigenschaft in der [**Anwendungs**](applications.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="455e2-130">Die Eigenschaften partitiondescription, PartitionID und partitionName in der Auflistung [**filesforimport**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="455e2-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="455e2-131">Die Eigenschaften "dspartitionlookupabled", "localpartitionlookupabled" und "partitionsenabled" in der [**LocalComputer**](localcomputer.md) -Sammlung.</span><span class="sxs-lookup"><span data-stu-id="455e2-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="455e2-132">Die Eigenschaften "eventclasspartitionid" und "abonneaspartitionid" in der " [**abonptionsforcomponent**](subscriptionsforcomponent.md) "-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="455e2-133">Die Eigenschaften eventclasspartitionid und abonneaspartitionid in der [**transientabonnements**](transientsubscriptions.md) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="455e2-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="455e2-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="455e2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="455e2-135">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="455e2-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="455e2-136">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="455e2-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="455e2-137">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="455e2-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="455e2-138">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="455e2-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="455e2-139">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="455e2-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="455e2-140">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="455e2-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



