---
description: Gruppieren von Anwendungen in Partitionen
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Gruppieren von Anwendungen in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346461"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="f48f7-103">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="f48f7-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="f48f7-104">Bei der Entscheidung, wie Anwendungen in Partitionen gruppiert werden sollen, müssen Administratoren bestimmte Regeln und Einschränkungen beachten, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="f48f7-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="f48f7-105">Eine Anwendung kann in einer oder mehreren Partitionen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f48f7-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="f48f7-106">In einer Anwendung kann nur eine Instanz einer bestimmten Komponente vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f48f7-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="f48f7-107">Öffentliche und private Komponenten</span><span class="sxs-lookup"><span data-stu-id="f48f7-107">Public and Private Components</span></span>

<span data-ttu-id="f48f7-108">Bei der Entscheidung, wie COM+-Anwendungen gruppiert werden sollen, gibt es weitere Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f48f7-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="f48f7-109">Diese Einschränkungen beziehen sich auf öffentliche und private Komponenten innerhalb einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f48f7-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="f48f7-110">Anwendungskomponenten können im Allgemeinen entweder öffentlich oder privat sein.</span><span class="sxs-lookup"><span data-stu-id="f48f7-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="f48f7-111">Wenn Sie jedoch Anwendungen in Partitionen gruppieren, sollten Administratoren einige Einschränkungen bei den öffentlichen und privaten Komponenten beachten.</span><span class="sxs-lookup"><span data-stu-id="f48f7-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="f48f7-112">In der folgenden Tabelle sind diese Einschränkungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f48f7-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="f48f7-113">Wenn eine Anwendung:</span><span class="sxs-lookup"><span data-stu-id="f48f7-113">If an application is:</span></span>              | <span data-ttu-id="f48f7-114">Die Komponenten in einer Partition können folgende sein:</span><span class="sxs-lookup"><span data-stu-id="f48f7-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48f7-115">Eine Serveranwendung</span><span class="sxs-lookup"><span data-stu-id="f48f7-115">A server application</span></span><br/>    | <span data-ttu-id="f48f7-116">Öffentlich und privat.</span><span class="sxs-lookup"><span data-stu-id="f48f7-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="f48f7-117">Eine Bibliotheks Anwendung</span><span class="sxs-lookup"><span data-stu-id="f48f7-117">A library application</span></span><br/>   | <span data-ttu-id="f48f7-118">Nur öffentlich.</span><span class="sxs-lookup"><span data-stu-id="f48f7-118">Public only.</span></span> <span data-ttu-id="f48f7-119">Andernfalls könnte die aufruferanwendung die gleichen Komponenten aufweisen, was zu Mehrdeutigkeit führen würde.</span><span class="sxs-lookup"><span data-stu-id="f48f7-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="f48f7-120">In der globalen Partition</span><span class="sxs-lookup"><span data-stu-id="f48f7-120">In the global partition</span></span><br/> | <span data-ttu-id="f48f7-121">Nur öffentlich.</span><span class="sxs-lookup"><span data-stu-id="f48f7-121">Public only.</span></span> <span data-ttu-id="f48f7-122">Dadurch wird die Abwärtskompatibilität sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="f48f7-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="f48f7-123">Anwendungs-IDs</span><span class="sxs-lookup"><span data-stu-id="f48f7-123">Application IDs</span></span>

<span data-ttu-id="f48f7-124">Jede auf einem Computer installierte COM+-Anwendung verfügt über eine eindeutige Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f48f7-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="f48f7-125">Anwendungsnamen müssen jedoch nur innerhalb einer einzelnen Partition und nicht auf dem gesamten Computer eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f48f7-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="f48f7-126">In der folgenden Tabelle wird gezeigt, was mit der Anwendungs-ID geschieht, wenn eine Anwendung in eine Partition importiert oder aus einer Partition exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="f48f7-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="f48f7-127">Wenn eine Anwendung:</span><span class="sxs-lookup"><span data-stu-id="f48f7-127">If an application is:</span></span>                                              | <span data-ttu-id="f48f7-128">Dann die Anwendungs-ID:</span><span class="sxs-lookup"><span data-stu-id="f48f7-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="f48f7-129">In die globale Partition importiert</span><span class="sxs-lookup"><span data-stu-id="f48f7-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="f48f7-130">Bleibt unverändert</span><span class="sxs-lookup"><span data-stu-id="f48f7-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="f48f7-131">Wird in eine andere Partition als die globale Partition importiert.</span><span class="sxs-lookup"><span data-stu-id="f48f7-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="f48f7-132">Wurde geändert</span><span class="sxs-lookup"><span data-stu-id="f48f7-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="f48f7-133">Exportiert</span><span class="sxs-lookup"><span data-stu-id="f48f7-133">Exported</span></span><br/>                                                | <span data-ttu-id="f48f7-134">Ist in der exportierten Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="f48f7-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f48f7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f48f7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f48f7-136">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="f48f7-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="f48f7-137">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="f48f7-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="f48f7-138">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="f48f7-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="f48f7-139">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="f48f7-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="f48f7-140">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="f48f7-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




