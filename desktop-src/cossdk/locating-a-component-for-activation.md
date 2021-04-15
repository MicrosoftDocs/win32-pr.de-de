---
description: Suchen einer Komponente zur Aktivierung
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Suchen einer Komponente zur Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561179"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="128af-103">Suchen einer Komponente zur Aktivierung</span><span class="sxs-lookup"><span data-stu-id="128af-103">Locating a Component for Activation</span></span>

<span data-ttu-id="128af-104">Wenn com+ die richtige Partition gefunden hat – über den standardmäßigen Partitions Satz der Benutzeridentität, einen partitionmoniker oder die Partitions-ID im Kontext des Objekts – com + muss dann die richtige Komponente innerhalb dieser Partition suchen.</span><span class="sxs-lookup"><span data-stu-id="128af-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="128af-105">In der folgenden Abbildung wird gezeigt, wie eine Komponente gefunden und aktiviert wird, wenn sich diese Komponente in einer Partition befindet.</span><span class="sxs-lookup"><span data-stu-id="128af-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="128af-106">Vor der Aktivierung einer Komponente führt com+ eine Validierung durch, um zu überprüfen, ob die Benutzeridentität, die versucht, die Komponente zu aktivieren, über Zugriffsrechte für den Partitions Satz verfügt, in dem sich die Komponente befindet.</span><span class="sxs-lookup"><span data-stu-id="128af-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Diagramm, das eine Problem Behandlungs Struktur zum Auffinden einer Komponente zur Aktivierung anzeigt.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="128af-108">Die vorherige Abbildung zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="128af-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="128af-109">Wenn sich die aufgerufene Komponente in einer Partition befindet und sich in der gleichen Anwendung wie die aufrufende Komponente befindet, wird die Komponente aktiviert, unabhängig davon, ob die aufgerufene Komponente als öffentlich oder privat gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="128af-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="128af-110">Wenn sich die aufgerufene Komponente in einer Partition befindet, aber nicht in der gleichen Anwendung wie die aufrufende Komponente vorhanden ist, prüft com+, ob die Komponente als öffentlich markiert ist.</span><span class="sxs-lookup"><span data-stu-id="128af-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="128af-111">Wenn keine öffentliche Version gefunden wird, durchsucht com+ die globale Partition, um nach einer öffentlichen Version der Komponente zu suchen.</span><span class="sxs-lookup"><span data-stu-id="128af-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="128af-112">Wenn keine öffentliche Version der Komponente in der globalen Partition gefunden wird oder die Benutzeridentität keine Berechtigungen für die Partition hat, tritt bei der Aktivierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="128af-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="128af-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="128af-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128af-114">Suchen von Partitionen während der Aktivierung</span><span class="sxs-lookup"><span data-stu-id="128af-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



