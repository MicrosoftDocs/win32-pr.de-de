---
description: Transport fähige Schatten Kopien können verwendet werden, um eine schnelle Wiederherstellung zu ermöglichen.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363400"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="9cb34-103">Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes</span><span class="sxs-lookup"><span data-stu-id="9cb34-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="9cb34-104">[*Transport fähige Schatten Kopien*](vssgloss-t.md) können verwendet werden, um eine *schnelle Wiederherstellung* zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9cb34-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="9cb34-105">Die schnelle Wiederherstellung kann verwendet werden, um schnell zu einer früheren Schatten Kopie zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="9cb34-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="9cb34-106">Hierzu sind folgende Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="9cb34-106">The steps involved are:</span></span>

1.  <span data-ttu-id="9cb34-107">Erstellen Sie die austauschen-Schatten Kopie der entsprechenden LUNs.</span><span class="sxs-lookup"><span data-stu-id="9cb34-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="9cb34-108">Die Schatten Kopie kann entweder [*persistent*](vssgloss-p.md) oder nicht persistent sein.</span><span class="sxs-lookup"><span data-stu-id="9cb34-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="9cb34-109">Entfernen der ursprünglichen LUNs</span><span class="sxs-lookup"><span data-stu-id="9cb34-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="9cb34-110">Wenn sich der Computer in einem Cluster befindet, markieren Sie die betroffenen Datenträger Ressourcen als offline, oder aktivieren Sie den [Wartungsmodus](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) für diese Datenträger Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9cb34-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="9cb34-111">Maskieren Sie die betroffenen LUNs von diesem Computer (und allen anderen Knoten, wenn sich der Computer in einem Cluster befindet).</span><span class="sxs-lookup"><span data-stu-id="9cb34-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="9cb34-112">Importieren Sie die Schatten Kopie mithilfe der [**IVssBackupComponents:: importshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9cb34-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="9cb34-113">Unterbrechen Sie die Schatten Kopie mithilfe der [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9cb34-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="9cb34-114">Markieren Sie die neuen Schattenkopievolumes als Lese-/Schreib.</span><span class="sxs-lookup"><span data-stu-id="9cb34-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="9cb34-115">Wenn sich der Computer in einem Cluster befindet, machen Sie die neuen schattenkopieluns als ursprüngliche LUNs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cb34-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="9cb34-116">Aufheben der Maskierung der schattenkopieluns auf den anderen Knoten im Cluster.</span><span class="sxs-lookup"><span data-stu-id="9cb34-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="9cb34-117">Markieren Sie die Ressourcen, die zuvor als offline markiert waren, oder deaktivieren Sie den Wartungsmodus für diese Datenträger Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9cb34-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="9cb34-118">Transport fähige Schatten Kopien in einem Cluster werden vor Windows Server 2003 mit Service Pack 1 (SP1) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9cb34-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="9cb34-119">Dies wird nur mit kompatiblen LUNs unterstützt, die mindestens eine SCSI-VPD (Vital Product Data)-Seite 0x83 \_ -Speicher Bezeichner vom Typ 1, 2 oder 8 und Association 0 aufweisen, und die LUNs müssen einen Basis Datenträger mit MBR-Partitionierung verwalten.</span><span class="sxs-lookup"><span data-stu-id="9cb34-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
