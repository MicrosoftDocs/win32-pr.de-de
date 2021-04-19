---
description: Die com+-Partitions Funktion enthält einen Partitions Cache. Dieser Cache speichert Benutzer-zu-Partition-Zuordnungen und ist darauf ausgelegt, sich wiederholende Active Directory Zugriffe zu vermeiden.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Konfigurieren des Partitions Caches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346248"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="ec27b-104">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="ec27b-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="ec27b-105">Die com+-Partitions Funktion enthält einen Partitions Cache.</span><span class="sxs-lookup"><span data-stu-id="ec27b-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="ec27b-106">Dieser Cache speichert Benutzer-zu-Partition-Zuordnungen und ist darauf ausgelegt, sich wiederholende Active Directory Zugriffe zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ec27b-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="ec27b-107">Ändern der Cache Größe</span><span class="sxs-lookup"><span data-stu-id="ec27b-107">Changing Cache Size</span></span>

<span data-ttu-id="ec27b-108">Der Partitions Cache besteht aus drei Tabellen, deren Größe geändert werden kann, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ec27b-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="ec27b-109">Diese Tabellen bestehen aus der Anzahl der SID-Einträge im Cache, der Anzahl der OU-Einträge im Cache und der Anzahl der Partitions Einträge im Cache.</span><span class="sxs-lookup"><span data-stu-id="ec27b-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="ec27b-110">Um diese Tabellen Größen zu ändern, können Administratoren die Werte eines Registrierungsschlüssels ändern.</span><span class="sxs-lookup"><span data-stu-id="ec27b-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="ec27b-111">Der Registrierungsschlüssel und die zugehörigen Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ec27b-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="ec27b-112">**HKLM \\ Software \\ Microsoft \\ COM3 \\ partitioncache**</span><span class="sxs-lookup"><span data-stu-id="ec27b-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="ec27b-113">Schlüsselwerte</span><span class="sxs-lookup"><span data-stu-id="ec27b-113">Key values</span></span>                         | <span data-ttu-id="ec27b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec27b-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec27b-115">**Numsidentries**</span><span class="sxs-lookup"><span data-stu-id="ec27b-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="ec27b-116">Enthält den reg \_ DWORD-Wert für die Anzahl der SID-Einträge im Cache (Standardwert = 512).</span><span class="sxs-lookup"><span data-stu-id="ec27b-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="ec27b-117">Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl der eindeutigen Identitäten ist, die ein Computer im Zeitfenster für die Cache Invalidierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec27b-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="ec27b-118">**Numnameentries**</span><span class="sxs-lookup"><span data-stu-id="ec27b-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="ec27b-119">Enthält den reg \_ DWORD-Wert für die Anzahl der Organisationseinheiten-namens Einträge im Cache (Standard = 64).</span><span class="sxs-lookup"><span data-stu-id="ec27b-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="ec27b-120">Dieser Wert sollte auf einen Wert festgelegt werden, der größer als die Anzahl der eindeutigen Organisationseinheiten Namen ist, die ein Computer im Zeitfenster für die Cache Invalidierung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ec27b-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="ec27b-121">**Numpartitionentries**</span><span class="sxs-lookup"><span data-stu-id="ec27b-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="ec27b-122">Enthält den reg \_ DWORD-Wert für die Anzahl der Partitions Einträge im Cache (Standardwert = 1024).</span><span class="sxs-lookup"><span data-stu-id="ec27b-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="ec27b-123">Im Zeitfenster für die Cache Validierung sollte der DWORD-Wert auf eine Zahl festgelegt werden, die größer als die Anzahl der eindeutigen Partitionen ist, die von einem Computer gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="ec27b-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="ec27b-124">Dies liegt daran, dass der Kontext einer Komponente eine Partitions-ID für eine Partition enthalten kann, die nicht auf diesem Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ec27b-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="ec27b-125">**Entryablauf**</span><span class="sxs-lookup"><span data-stu-id="ec27b-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="ec27b-126">Enthält den reg \_ DWORD-Wert für die Tick-Anzahl (jedes Tick = ~ 7 Minuten), bis ein Cache Eintrag ungültig wird (Standardwert = 4 (~ 28 Minuten)).</span><span class="sxs-lookup"><span data-stu-id="ec27b-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="ec27b-127">Leeren des Caches</span><span class="sxs-lookup"><span data-stu-id="ec27b-127">Flushing the Cache</span></span>

<span data-ttu-id="ec27b-128">Da com+ die Standard Partition für Benutzer zwischenspeichert, können Sie diese Methode nach dem Ändern der Standard Partition für einen Benutzer im Active Directory abrufen.</span><span class="sxs-lookup"><span data-stu-id="ec27b-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="ec27b-129">Administratoren können dies Programm gesteuert durch Aufrufen der [**flushpartitioncache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) -Methode durchführen.</span><span class="sxs-lookup"><span data-stu-id="ec27b-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec27b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec27b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec27b-131">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="ec27b-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="ec27b-132">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="ec27b-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="ec27b-133">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="ec27b-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="ec27b-134">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec27b-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="ec27b-135">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="ec27b-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




