---
description: Standard Partitionen
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Standard Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214286"
---
# <a name="default-partitions"></a><span data-ttu-id="53ff7-103">Standard Partitionen</span><span class="sxs-lookup"><span data-stu-id="53ff7-103">Default Partitions</span></span>

<span data-ttu-id="53ff7-104">Wenn einem Benutzer eine Standard Partition zugewiesen wird, versucht com+ zunächst, Komponenten in dieser Partition zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="53ff7-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="53ff7-105">Wenn die Aktivierung fehlschlägt, durchsucht com+ die globale Partition nach der zu aktivierbaren Komponente.</span><span class="sxs-lookup"><span data-stu-id="53ff7-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="53ff7-106">Eine Ausnahme zu diesem Vorgang tritt auf, wenn die COM+-Komponente einen partitionmoniker enthält, der explizit die Partition angibt, in der sich die Komponente befindet.</span><span class="sxs-lookup"><span data-stu-id="53ff7-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="53ff7-107">In diesem Fall hat der partitionsmoniker Vorrang vor jeder standardmäßigen Partitions Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="53ff7-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="53ff7-108">Wenn Sie lokale Partitionen verwenden, wird die Standard Partition Benutzern mithilfe des Ordners " **com+-Partitions Benutzer** " im Verwaltungs Programm "Komponenten Dienste" auf dem Anwendungsserver zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="53ff7-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="53ff7-109">Bei der Verwendung von Partitions Sätzen im Active Directory wird die Standard Partition des Benutzers durch den Partitions Satz des Benutzers bestimmt.</span><span class="sxs-lookup"><span data-stu-id="53ff7-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53ff7-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53ff7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ff7-111">Lokale Partitionen</span><span class="sxs-lookup"><span data-stu-id="53ff7-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="53ff7-112">Partitions Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53ff7-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="53ff7-113">Partitionen und Active Directory</span><span class="sxs-lookup"><span data-stu-id="53ff7-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="53ff7-114">Die globale Partition</span><span class="sxs-lookup"><span data-stu-id="53ff7-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



