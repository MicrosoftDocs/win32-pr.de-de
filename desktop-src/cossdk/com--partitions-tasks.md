---
description: Aufgaben für COM+-Partitionen
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Aufgaben für COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214091"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="50695-103">Aufgaben für COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="50695-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="50695-104">Die folgenden Themen in diesem Abschnitt enthalten Schritt-für-Schritt-Anleitungen für die Verwendung von COM+-Partitionen.</span><span class="sxs-lookup"><span data-stu-id="50695-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="50695-105">**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50695-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="50695-106">Die globale Partition ist die einzige verfügbare com+-Partition.</span><span class="sxs-lookup"><span data-stu-id="50695-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="50695-107">\* \* Windows 2000: \* \* der com+-Partitions Dienst ist in Windows 2000 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50695-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="50695-108">Thema</span><span class="sxs-lookup"><span data-stu-id="50695-108">Topic</span></span>                                                                                                         | <span data-ttu-id="50695-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50695-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50695-110">Erstellen und Konfigurieren von COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="50695-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="50695-111">Hier wird beschrieben, wie eine COM+-Partition erstellt und konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="50695-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="50695-112">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="50695-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="50695-113">Beschreibt, wie COM+-Partitionen verwaltet werden, die nicht in Active Directory vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="50695-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="50695-114">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="50695-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="50695-115">Beschreibt, wie COM+-Partitionen verwaltet werden, die in Active Directory angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50695-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="50695-116">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="50695-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="50695-117">Beschreibt, wie Sicherheits Privilegien für eine COM+-Partition festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="50695-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="50695-118">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="50695-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="50695-119">Beschreibt, wie COM+-Anwendungen für eine COM+-Partition konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="50695-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="50695-120">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="50695-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="50695-121">Beschreibt, wie Daten zu COM+-Partitionen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="50695-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="50695-122">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="50695-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="50695-123">Hier wird beschrieben, wie Sie den com+-Partitions Cache konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="50695-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="50695-124">Der com+-Partitions Dienst ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="50695-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="50695-125">Um den com+-Partitions Dienst zu verwenden, müssen Sie ihn über das Verwaltungs Tool Komponenten Dienste oder durch Ändern der partitionsenabled-Eigenschaft in der [**LocalComputer**](localcomputer.md) -Sammlung auf true aktivieren.</span><span class="sxs-lookup"><span data-stu-id="50695-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="50695-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50695-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50695-127">Konzepte der COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="50695-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




