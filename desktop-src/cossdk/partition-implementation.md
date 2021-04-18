---
description: Bei der Installation auf einem Anwendungsserver erstellt com+ automatisch eine Partition, die als globale Partition bezeichnet wird.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Partitions Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343998"
---
# <a name="partition-implementation"></a><span data-ttu-id="5eae7-103">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="5eae7-103">Partition Implementation</span></span>

<span data-ttu-id="5eae7-104">Bei der Installation auf einem Anwendungsserver erstellt com+ automatisch eine Partition, die als *globale Partition* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5eae7-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="5eae7-105">Die globale Partition enthält einen Standardsatz von com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5eae7-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="5eae7-106">Com+-Anwendungen, die in der globalen Partition installiert werden, sind automatisch für alle Benutzer auf dem Server verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5eae7-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="5eae7-107">Wenn Sie andere com+-Anwendungen haben, die Sie allen Benutzern auf dem Server zur Verfügung stellen möchten, können Sie Sie der globalen Partition hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5eae7-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="5eae7-108">Neben der globalen Partition können Sie auch andere Partitionen für Benutzer auf diesem Server oder für Benutzer in der gesamten Domäne erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eae7-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="5eae7-109">Wenn Sie zusätzliche Partitionen erstellen und mehrere Konfigurationen einer COM+-Anwendung installieren, können die Benutzer diese Anwendungs Konfigurationen gleichzeitig auf demselben Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="5eae7-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="5eae7-110">Außerdem können Sie den Benutzer Zugriff auf diese Anwendungen steuern, indem Sie com+-Anwendungen in einer anderen Partition als der globalen Partition installieren.</span><span class="sxs-lookup"><span data-stu-id="5eae7-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="5eae7-111">**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5eae7-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="5eae7-112">Die globale Partition ist die einzige verfügbare com+-Partition.</span><span class="sxs-lookup"><span data-stu-id="5eae7-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="5eae7-113">Weitere Informationen zu lokalen Partitionen und Partitionen, die in Active Directory definiert sind, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5eae7-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="5eae7-114">Lokale Partitionen</span><span class="sxs-lookup"><span data-stu-id="5eae7-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="5eae7-115">Partitionen und Active Directory</span><span class="sxs-lookup"><span data-stu-id="5eae7-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="5eae7-116">Standard Partitionen</span><span class="sxs-lookup"><span data-stu-id="5eae7-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="5eae7-117">Die globale Partition</span><span class="sxs-lookup"><span data-stu-id="5eae7-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="5eae7-118">Partitions Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5eae7-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="5eae7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5eae7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eae7-120">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="5eae7-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="5eae7-121">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5eae7-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="5eae7-122">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="5eae7-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="5eae7-123">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="5eae7-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



